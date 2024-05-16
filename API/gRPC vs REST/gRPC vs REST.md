## gRPC против REST: различия между архитектурными стилями API

![alt text](/API/gRPC%20vs%20REST/image/image10.png)

## Оглавление:

- [Что такое RPC?](#что-такое-rpc)
- [Что такое REST?](#что-такое-rest)
- [Что такое gRPC?](#что-такое-grpc)
- [gRPC и REST: сравнение](#grpc-и-rest-сравнение)
  - [HTTP 1.1 против HTTP 2](#http-11-против-http-2)
  - [Поддержка браузеров](#поддержка-браузеров)
  - [Структура данных полезной нагрузки](#структура-данных-полезной-нагрузки)
  - [Особенности генерации кода](#особенности-генерации-кода)
- [gRPC и REST: сравнительная таблица](#grpc-и-rest-сравнительная-таблица)
- [Когда использовать gRPC а когда REST?](#когда-использовать-grpc-а-когда-rest)
- [Лучше ли gRPC, чем REST API?](#лучше-ли-grpc-чем-rest-api)


# Что такое RPC?

RPC использует модель клиент-сервер. Запрашивающий сервер (другими словами, клиент) запрашивает сообщение, которое переводится RPC и отправляется на другой сервер. Получив запрос, сервер отправляет ответ обратно клиенту. Пока сервер обрабатывает этот вызов, клиент блокируется, а внутренняя передача сообщений внутри серверов скрыта.

Кроме того, RPC позволяет клиенту запросить функцию в определенном формате и получить ответ в точно таком же формате. Тем не менее, способ отправки вызова с помощью RPC API содержится в URL. RPC поддерживает удаленные вызовы процедур как в локальных, так и в распределенных средах.

Как и REST API, RPC также устанавливает правила взаимодействия и то, как пользователь может отправлять "вызовы" (запросы) для вызова методов, обеспечивающих связь и взаимодействие с сервисом.

# Что такое REST?

При использовании REST API ответ от внутренних данных передается клиентам (или пользователям) через формат сообщений JSON или XML. Эта архитектурная модель, как правило, следует протоколу HTTP. Однако нередко RPC-проекты также заимствуют несколько идей из HTTP, сохраняя при этом модель RPC. На самом деле, большинство современных API реализуются путем привязки API к одному и тому же протоколу HTTP, несмотря на используемую модель (RPC или REST).

Когда REST API находится в открытом доступе, каждый сервис, объединяющий микросервисное приложение, может быть представлен пользователю/клиенту как ресурс, доступ к которому можно получить с помощью следующих HTTP-команд: **GET**, **DELETE**, **POST** и **PUT**.

# Что такое gRPC?

gRPC расшифровывается как Google Remote Procedure Call и представляет собой вариант, основанный на архитектуре RPC. Эта технология повторяет реализацию RPC API, которая использует протокол HTTP 2.0, но HTTP не представляется ни разработчику API, ни серверу. Таким образом, нет необходимости беспокоиться о том, как концепции RPC отображаются на HTTP, что снижает сложность.

В целом gRPC призван ускорить передачу данных между микросервисами. В его основе лежит подход, заключающийся в определении сервиса, создании методов и соответствующих параметров для удаленного вызова и типов возврата.

Более того, он выражает модель API RPC на языке IDL (язык описания интерфейсов), который предлагает более прямой путь к определению удаленных процедур. По умолчанию IDL использует буферы протоколов (но возможны и другие альтернативы) для описания интерфейса сервиса, а также структуры сообщений полезной нагрузки.

# gRPC и REST: сравнение

Теперь, когда мы получили общее представление о gRPC и REST, давайте рассмотрим их основные различия.

## HTTP 1.1 против HTTP 2
REST API используют модель взаимодействия "запрос-ответ", которая обычно строится на основе HTTP 1.1. К сожалению, это означает, что если микросервис получает несколько запросов от нескольких клиентов, то модель должна обрабатывать каждый запрос за раз, что, соответственно, замедляет работу всей системы. Однако REST API также могут быть построены на HTTP 2, но модель взаимодействия "запрос-ответ" остается прежней, что не позволяет REST API максимально использовать преимущества HTTP 2, такие как потоковое взаимодействие и двунаправленная поддержка.

gRPC не сталкивается с подобными препятствиями. Он построен на базе HTTP 2 и вместо этого использует модель связи "клиент-ответ". Эти условия поддерживают двунаправленную связь и потоковое взаимодействие благодаря способности gRPC получать несколько запросов от нескольких клиентов и обрабатывать эти запросы одновременно, постоянно передавая информацию. Кроме того, gRPC может обрабатывать "унарные" взаимодействия, подобные тем, что построены на HTTP 1.1.

В общем, gRPC способен обрабатывать унарные взаимодействия и различные типы потоковой передачи данных:

- **Unary**: когда клиент отправляет один запрос и получает один ответ.
- **Server-streaming**: когда сервер отвечает потоком сообщений на запрос клиента. После отправки всех данных сервер дополнительно доставляет сообщение о состоянии для завершения процесса.
- **Client-streaming**: когда клиент отправляет поток сообщений и, в свою очередь, получает от сервера одно ответное сообщение.
- **Bidirectional-streaming**: два потока (клиент и сервер) независимы, а это означает, что они оба могут передавать сообщения в любом порядке. Клиент — это тот, кто инициирует и завершает двунаправленную потоковую передачу.


![alt text](/API/gRPC%20vs%20REST/image/image1.png)

## Поддержка браузеров

Этот аспект, пожалуй, является одним из главных преимуществ REST API перед gRPC. С одной стороны, REST полностью поддерживается всеми браузерами. С другой стороны, gRPC все еще довольно ограничен, когда дело доходит до поддержки браузеров. К сожалению, для выполнения преобразований между HTTP 1.1 и HTTP 2 требуется gRPC-web и прокси-слой. Поэтому gRPC в основном используется для внутренних/частных систем (API-программы в рамках бэкэнд-функционала данных и приложений конкретной организации).

## Структура данных полезной нагрузки

Как уже говорилось, по умолчанию gRPC использует Protocol Buffer для сериализации данных полезной нагрузки. Это решение является более удобным, поскольку позволяет использовать сжатый формат и уменьшает размер сообщений. Кроме того, Protobuf (или Protocol Buffer) является бинарным, поэтому он сериализует и десериализует структурированные данные для их передачи. Другими словами, сообщения с сильной типизацией могут быть автоматически преобразованы из Protobuf в язык программирования клиента и сервера.

В отличие от этого, REST в основном использует форматы JSON или XML для отправки и получения данных. Несмотря на то, что формат JSON не предусматривает никакой структуры, он является наиболее популярным благодаря своей гибкости и возможности отправлять динамические данные, не придерживаясь строгой структуры. Еще одним существенным преимуществом использования JSON является его человекочитаемость, с которой Protobuf пока не может конкурировать.

Тем не менее, JSON не так легок и быстр, когда речь идет о передаче данных. Причина этого кроется в том, что при использовании REST JSON (или другие форматы) должны быть сериализованы и преобразованы в язык программирования, используемый как на стороне клиента, так и на стороне сервера. Это добавляет дополнительный шаг к процессу передачи данных, что, как следствие, может снизить производительность и открыть возможность для ошибок.

## Особенности генерации кода

В отличие от gRPC, REST API не предоставляет встроенных функций генерации кода, что означает, что разработчики должны использовать сторонние инструменты, такие как Swagger или Postman, для создания кода для API-запросов.

В отличие от этого, gRPC имеет встроенные функции генерации кода благодаря компилятору protoc, который совместим с несколькими языками программирования. Это особенно полезно для систем микросервисов, объединяющих различные сервисы, разработанные на разных языках и платформах. В целом, встроенный генератор кода также облегчает создание SDK (Software Development Kit).

# gRPC и REST: сравнительная таблица

| Features                           | gRPC                                                                                                                                                               | REST                                                                                                                         |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| HTTP 1.1 против HTTP 2             | Модель взаимодействия "клиент-ответ" построена на базе HTTP 2, что позволяет осуществлять потоковое взаимодействие и поддерживать двунаправленную передачу данных. | Следуют модели взаимодействия "запрос-ответ" и обычно строятся на основе HTTP 1.1.                                           |
| Поддержка браузеров                | Ограниченная поддержка браузеров. gRPC требует gRPC-web и прокси-слой для выполнения преобразований между HTTP 1.1 и HTTP 2.                                       | Универсальная поддержка браузеров.                                                                                           |
| Структура данных полезной нагрузки | По умолчанию gRPC использует Protocol Buffer для сериализации данных полезной нагрузки.                                                                            | Для отправки и получения данных REST в основном использует форматы JSON или XML.                                             |
| Особенности генерации кода         | gRPC имеет встроенные функции генерации кода.                                                                                                                      | Разработчики должны использовать сторонние инструменты, такие как Swagger или Postman, чтобы создавать код для API-запросов. |

# Когда использовать gRPC а когда REST?

Как уже говорилось, несмотря на многочисленные преимущества gRPC, у него есть одно серьезное препятствие: низкая совместимость с браузерами. Следовательно, gRPC немного ограничен внутренними/частными системами.

Напротив, API REST, как мы уже говорили, могут иметь свои недостатки, но они остаются наиболее известными API для подключения систем на базе микросервисов. Кроме того, REST следует стандартизации протокола HTTP и предлагает универсальную поддержку, что делает этот архитектурный стиль API лучшим вариантом для разработки веб-сервисов, а также интеграции приложений и микросервисов. Однако это не означает, что мы должны пренебрегать возможностями применения gRPC.

Архитектурный стиль gRPC обладает многообещающими возможностями, которые можно (и нужно) исследовать. Это отличный вариант для работы с мультиязычными системами, потоковой передачи данных в реальном времени, а также, например, при эксплуатации IoT-систем, требующих легкой передачи сообщений, как это позволяют делать сериализованные сообщения Protobuf. Более того, gRPC следует рассматривать и для мобильных приложений, поскольку они не нуждаются в браузере и могут воспользоваться преимуществами более компактных сообщений, сохраняя скорость процессоров мобильных устройств.

# Лучше ли gRPC, чем REST API?

**Лучше ли gRPC, чем REST API? И gRPC, и REST API имеют свои преимущества в использовании. gRPC отлично подходит для высокопроизводительных сред, поддерживает двунаправленную потоковую передачу и использует буферы протоколов для эффективной сериализации. REST API проще, гибче и лучше подходит для использования в веб-приложениях или при взаимодействии с несколькими языками программирования.**
