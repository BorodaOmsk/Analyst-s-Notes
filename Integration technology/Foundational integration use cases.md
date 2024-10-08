## Основополагающие примеры использования интеграции

![alt text](/Integration%20technology/image/image10.png)

## Оглавление:

- [Агрегирование данных](#агрегирование-данных)
- [Streaming data ingestion](#streaming-data-ingestion)
- [Синхронизация данных между несколькими приложениями](#синхронизация-данных-между-несколькими-приложениями)
- [Обмен данными с внешними партнерами](#обмен-данными-с-внешними-партнерами)
- [Трансляция событий](#трансляция-событий)
- [Массовое или пакетное перемещение данных](#массовое-или-пакетное-перемещение-данных)
- [Синхронная передача данных или триггеры процессов](#синхронная-передача-данных-или-триггеры-процессов)
- [Асинхронная передача данных или триггеры процессов](#асинхронная-передача-данных-или-триггеры-процессов)
- [Оркестровка и обработка данных](#оркестровка-и-обработка-данных)
- [Интеграция пользовательского интерфейса](#интеграция-пользовательского-интерфейса)
- [Выполнение сквозных бизнес-процессов / сценариев использования](#выполнение-сквозных-бизнес-процессов--сценариев-использования)



Хотя существует множество бизнес-сценариев для интеграции приложений и данных, я считаю, что каждый бизнес-сценарий можно разбить на следующие уникальные и фундаментальные сценарии использования интеграции. Эти сценарии являются строительными блоками и могут быть объединены для разработки более сложных сценариев.


# Агрегирование данных

Предприятия консолидируют данные из нескольких источников для обеспечения семантической полноты и контекстуализации. В таких случаях данные из нескольких приложений копируются в центральное место для дальнейшего анализа и обработки, например, в хранилища данных, озера данных.

![alt text](/Integration%20technology/image/image9.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Создание единого представления о клиенте 
- Миграция данных из локальных приложений в облачное хранилище данных 
- Консолидация данных датчиков и данных ERP для расширенной аналитики моделей использования 

# Streaming data ingestion

В большинстве организаций имеются современные устройства и объекты, способные генерировать данные, отражающие текущее или прошлое состояние устройства. Эти данные жизненно важны для деятельности организации и должны поступать в платформу для последующего потребления и использования. Как правило, такие устройства могут генерировать данные как в медленном темпе (каждую минуту или час), так и в быстром (субмиллисекунды).

![alt text](/Integration%20technology/image/image8.png)

Среди распространенных примеров бизнес-сценариев: 

- Обработка данных датчиков IoT на периферии в режиме реального времени для консолидации данных о запасах в магазинах 
- Консолидация данных о кликах пользователей на веб-сайтах розничных компаний 
- Сбор и анализ данных о вибрации машин для прогнозирования отказов

# Синхронизация данных между несколькими приложениями

Для определенного фрагмента данных обычно существует четко определенная система записи, в которой осуществляется управление их жизненным циклом. Однако эти данные часто требуются в других системах для выполнения бизнес-операций в этих приложениях. Данные быстрее меняются в системе записи и требуются в приложениях-потребителях практически в режиме реального времени. Потребительские приложения могут дополнительно обогащать или обновлять определенную информацию. Чаще всего эти потребляющие системы не должны выступать в качестве систем записи.

![alt text](/Integration%20technology/image/image7.png)

Некоторые из распространенных примеров бизнес-сценариев: 

- Создание новой учетной записи клиента, синхронизация данных о ней с ERP, CRM и финансовыми приложениями. 
- Обновления учетных записей клиентов могут быть сделаны в приложениях CRM, и эти обновления отправляются обратно в систему учета. 
- Синхронизация данных о клиентах с приложениями поддержки клиентов, чтобы ваши операторы могли лучше обслуживать клиентов.
  
# Обмен данными с внешними партнерами

Любая организация, как правило, работает с множеством внешних бизнес-партнеров, таких как поставщики, подрядчики, государственные учреждения и т. д. Эти деловые партнеры представляют собой самостоятельные организации с различными системами, процессами и приложениями. Однако обмен данными между вашей организацией и организацией-партнером имеет решающее значение для выполнения деловых операций.

![alt text](/Integration%20technology/image/image6.png)

Среди распространенных примеров бизнес-сценариев:

- Обмен заказами на закупку с вашими поставщиками
- Передача счетов-фактур для оплаты вашим поставщикам
- Отправка налоговых данных


# Трансляция событий

События в организации происходят постоянно. Новые сотрудники, остановка или поломка оборудования, утверждение расходов, проблемы с оплатой, превышение трафиком веб-сайта определенного порога - все это классические примеры значимых событий, которые оказывают влияние на последующую деятельность и требуют дальнейших действий. Идентификация, захват и уведомление о таких событиях нижестоящих потребителей - критически важные аспекты в этих сценариях использования.

![alt text](/Integration%20technology/image/image5.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Отслеживание статуса отправления груза
- Отправка уведомлений о статусе выполнения заказов клиентов
- Отслеживание обновления запасов в режиме реального времени
- Сбой на сайте розничной сети после резкого увеличения числа кликов пользователей

# Массовое или пакетное перемещение данных

Потребность в получении данных как можно быстрее постоянно растет, однако существуют сценарии, в которых задержки в представлении информации допустимы или представление информации в режиме реального времени не требуется. Такие сценарии оптимизируют и обеспечивают более эффективное использование ресурсов таким образом, что постоянная или онлайн доступность вычислительных ресурсов не требуется.

![alt text](/Integration%20technology/image/image4.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Единовременный перенос учетных записей клиентов из старой CRM
- Периодическая миграция счетов-фактур из ERP в платежные системы
- Ночная сверка и анализ финансовых операций из нескольких приложений
- Ежедневное подведение итогов операций по отгрузке и приемке

# Синхронная передача данных или триггеры процессов

Синхронная передача данных - это сценарий, в котором получатель информации делает запрос на передачу данных и ждет, пока отправитель не передаст запрошенную информацию. В то время, пока данные не получены, любая дальнейшая обработка на получателе приостанавливается. Такие сценарии актуальны при наличии сильных зависимостей между запрашиваемыми данными и последующими операциями на приемнике.

![alt text](/Integration%20technology/image/image3.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Получение отчета о продажах за прошлый год из CRM-системы
- Поиск счета клиента в ERP-системе
- Проверка баланса для SIM-карты мобильного телефона

# Асинхронная передача данных или триггеры процессов

Асинхронная передача данных или триггеры процессов - это сценарии, в которых данные отправляются на цель без ожидания подтверждения или подтверждения от источника об успехе или неудаче передачи или триггера процесса. Источник продолжает последующую деятельность, отправляя данные или команду для запуска процесса. Потребители исходных приложений не испытывают никакого времени ожидания в результате передачи данных для обработки.

![alt text](/Integration%20technology/image/image2.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Рассылка рекламных текстов или электронных писем потенциальным клиентам
- Запуск рабочего процесса утверждения расходов

# Оркестровка и обработка данных

Значительная семантическая ясность достигается при объединении и оркестровке данных из нескольких источников. Оркестровка данных обеспечивает дополнительный контекст или ясность. В этом случае между источником и целью создается слой абстракции, в который встраивается более глубокая бизнес-логика. Часто сценарии использования оркестровки сильно привязаны и специфичны для базовых бизнес-доменов.

![alt text](/Integration%20technology/image/image11.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Активация учетной записи клиента - проверка кредитоспособности, проверка биографии, подтверждение занятости и т.д.
- Обработка нового сотрудника - настройка зарплатного счета, предоставление ИТ-активов, рабочих мест и т.д.

# Интеграция пользовательского интерфейса

Интеграция часто рассматривается как передача данных между приложениями для потребления на машинном уровне, как описано в предыдущих примерах использования, однако представление информации в консолидированном формате для потребления человеком является широко известным примером использования. Информация агрегируется в центральном месте для потребления человеком.

![alt text](/Integration%20technology/image/image12.png)

Среди распространенных примеров бизнес-сценариев можно назвать следующие:

- Порталы, интранет
- Публичные веб-сайты
- Мобильные приложения


# Выполнение сквозных бизнес-процессов / сценариев использования

Варианты использования базовой интеграции, описанные в предыдущем разделе, не исключают друг друга. Напротив, мы часто видим, что они дополняют друг друга и служат примитивными строительными блоками для создания более сложных бизнес-решений. Эти сценарии использования часто объединяются в цепочку, чтобы создать общее комплексное бизнес-решение или процесс.


Например

- Отправка заказа на поставку внешнему поставщику после утверждения руководством.

![alt text](/Integration%20technology/image/image13.png)

- Поиск данных о клиенте в CRM и последующая организация маркетинговой информации, адаптированной к клиенту

![alt text](/Integration%20technology/image/image14.png)
