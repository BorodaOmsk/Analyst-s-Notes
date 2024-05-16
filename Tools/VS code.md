**VS Code для системного аналатика**

![alt text](/Tools/image/image10.png)

**Содержание**:

- [Установка VS Code](#установка-vs-code)
- [Установка плагинов](#установка-плагинов)
  - [1 способ на странице Marketplace](#1-способ-на-странице-marketplace)
  - [2 способ из VS code](#2-способ-из-vs-code)
- [Рекомендуемые плагины](#рекомендуемые-плагины)
  - [1. Thunder Client](#1-thunder-client)
  - [2. Auto Close Tag](#2-auto-close-tag)
  - [3. Comment Translate](#3-comment-translate)
  - [4. `Draw.io Integration`](#4-drawio-integration)
  - [5. Json](#5-json)
  - [6. Log File Highlighter](#6-log-file-highlighter)
  - [7. Markdown Preview Enhanced](#7-markdown-preview-enhanced)
  - [8. OpenAPI (Swagger) Editor](#8-openapi-swagger-editor)
  - [9. PlantUML](#9-plantuml)
  - [10. PostgreSQL](#10-postgresql)
  - [11. YAML](#11-yaml)
  - [12. Remote Development](#12-remote-development)
  - [13. Russian Language Pack for Visual Studio Code](#13-russian-language-pack-for-visual-studio-code)

**VS code** = **Швейцарский нож** для системного аналитика и сейчас расскажу почему

![alt text](/Tools/image/image1.png)

В большинство компании от системного аналитика требуется очень много навыков, и он может совмещать роли (системный аналитик, бизнес аналитик и т.д.) 

![alt text](/Tools/image/image2.png)

и как правило он использует очень много инструментов, а что, если можно значительно уменьшить их количество, ведь намного удобнее работать в одном инструменте. Вот для этого как раз подходит **VS Code**.

# Установка VS Code

Скачайте и установите c офиального сайта [VS Code](https://code.visualstudio.com/download/)

# Установка плагинов 

в [Marketplace](https://marketplace.visualstudio.com/) для **VS Code** есть плагины практическии для любых задач.

## 1 способ на странице Marketplace

Непосредственно с [Marketplace](https://marketplace.visualstudio.com/), находим нужный плагин, можно воспользоватся поиском или выбрать из предложенных 

![alt text](/Tools/image/image3.png)

Что бы установить плагин выбираем нужный нам, нажимаем кнопку **"Install"**, в браузере откроится окно с предложением открыть VS code, подтверждаем открытие

![alt text](/Tools/image/image4.png)

Окроется VS code с вкладкой с описанием плагина, на которой нам нужно нажать кнопку установить 

## 2 способ из VS code 

На панели действии нажимаем значок **Расширения**, можно воспользоватся строкой поиска так и выбрать из рекомендуемых, для установки от нас тебуется только нажать кнопку **Установить**. Иногда **VS code** может запросить перезапуск после установки плагина.

![alt text](/Tools/image/image5.png)

# Рекомендуемые плагины 

## 1. Thunder Client

[ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client)

Клиентское расширение Rest API, замена тежеловесному Postman

![alt text](/Tools/image/image6.png)

**Основные характеристики:**

- Легкий и простой в использовании клиент REST API.
- Поддерживает **коллекций и переменные среды**.
- **Тестирование без сценариев**. Легко тестируйте ответы API с помощью графического интерфейса.
- **Локальное хранилище**: расширение сохраняет все данные локально на устройстве пользователя.
- **Git Sync**: сохраняйте данные запросов в своем репозитории Git для совместной работы в команде.
- **CLI**: CLI поддерживает интеграцию CI и CD и генерирует отчеты.


## 2. Auto Close Tag
 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

Автоматически добавляет закрывающий тег HTML/XML

Если вы часто работает с HTML/XML это незаменимый помошник.

**Основные характеристики:**

- Автоматически добавлять закрывающий тег при вводе закрывающей скобки открывающего тега.
- После вставки закрывающего тега курсор находится между открывающим и закрывающим тегом.
- Настраиваемый список тегов, который не будет автоматически закрываться
- Автоматически закрывать самозакрывающийся тег
- Поддержка тега автоматического закрытия
- Используйте сочетание клавиш или палитру команд, чтобы добавить закрывающий тег вручную.

## 3. Comment Translate
 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=intellsmi.comment-translate)

Этот плагин использует API Google Translate для перевода комментариев.

## 4. `Draw.io Integration`
 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)

Создаём **`Draw.io`** диаграммы, блок-схемы, прототипы, инфографику прямо в **VS code**

**Основные характеристики:**

- Редактируйте файлы .drawio, .dio, .drawio.svg или .drawio.png в редакторе Draw.io.
  - Чтобы создать новую диаграмму, просто создайте пустой файл *.drawio, *.drawio.svg или *.drawio.png и откройте его.
  - .drawio.svg - это действительные файлы .svg, которые можно вставлять в файлы readme на Github! Экспорт не требуется.
  - .drawio.png - это действительные файлы в формате .png! Экспорт не требуется. Однако при любой возможности следует использовать .svg - они выглядят гораздо лучше!
  - Для преобразования между различными форматами используйте команду Draw.io: Convert To....
- По умолчанию используется автономная версия Draw.io.
- Доступно несколько тем для Draw.io.
- Используйте Liveshare для совместного редактирования диаграммы с другими пользователями.

## 5. Json
 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=ZainChen.json)

 Все мы любим json но когда файл большой это боль, вот для этого есть плагин **Json**

 ![alt text](/Tools/image/image7.png)


## 6. Log File Highlighter

 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=emilast.LogFileHighlighter)

 Иногда нам требуется посмотреть логи которые вам прислали, для этого в VS Code есть плагин **Log File Highlighter**

  ![alt text](/Tools/image/image8.png)

## 7. Markdown Preview Enhanced

 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)

Предварительный просмотр Markdown файлов 

## 8. OpenAPI (Swagger) Editor

 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=42Crunch.vscode-openapi)

 Этот плагин VS Code добавляет широкую поддержку спецификации OpenAPI (OAS) (ранее известной как спецификация Swagger). Плагин поддерживает навигацию по коду, анализ, предварительный просмотр SwaggerUI или ReDoc, IntelliSense, принудительное применение и генерацию схемы, ссылки на определение схемы, фрагменты.

![alt text](/Tools/image/image9.png)


## 9. PlantUML

 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)

 поддержка PlantUML в VS Code

 **Основные характеристики:**

- **Предварительный просмотр диаграммы**.  
  - Нажмите Alt + D, чтобы запустить предварительный просмотр PlantUML (вариант + D в MacOS).
  - Автоматическое обновление.
  - Поддержка масштабирования и прокрутки.
  - Поддержка многостраничных диаграмм.
  - Мгновенный предварительный просмотр, если диаграмма была экспортирована.
  - С локального или серверного.
  - Привязка к границе
- **Экспорт диаграмм**
  - У курсора, в текущем файле, во всей рабочей области, в выбранной рабочей области.
  - Параллельный экспорт.
  - Генерируйте URL-адреса.
  - Поддержка многостраничных диаграмм.
  - С локального или серверного.
  - Поддержка карты изображений (cmapx).
- **Поддержка редактирования диаграмм**

## 10. PostgreSQL

 [ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=ckolkman.vscode-postgres)

Плагин для запросов к базам данных PostgreSQL. Несмотря на наличие проводника базы данных, он **НЕ предназначен** для создания/удаления баз данных или таблиц. Проводник - это визуальный инструмент, помогающий составлять запросы.
 
 **Основные характеристики:**

- Управление соединениями PostgreSQL базами
- Список Серверов/Баз данных/Функции/Таблиц/Колонок (первичный ключ/тип)
- Quickly select top * (with limit) of a table
- Выполнение запросов
  
  - Все запросы в файле pgsql (; с разделителями)
  - Выбранный запрос в файле pgsql
  - Выбранный запрос в ЛЮБОМ файле (через контекстное меню или палитру команд)
- Отдельные редакторы могут иметь различные соединения
- Быстрое изменение базы данных подключения с помощью щелчка на DB в строке состояния
- Подсветка синтаксиса
- Завершение кода с учетом подключения (ключевые слова, функции, таблицы и поля)
- Встроенное обнаружение ошибок с помощью EXPLAIN (одна ошибка на запрос в редакторе)

## 11. YAML

[ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

поддержка YAML language

## 12. Remote Development

[ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

Пакет расширений для удаленной разработки в VS Code:

- **Remote - SSH**- Работайте с исходным кодом в любом месте, открывая папки на удаленной машине/VM с помощью SSH. Поддерживает x86_64, ARMv7l (AArch32) и ARMv8l (AArch64) glibc-based Linux, Windows 10/Server (1803+) и macOS 10.14+ (Mojave) SSH-хосты.
- **Remote - Tunnels** - Работайте с исходным кодом в любом месте, открывая папки на удаленной машине/VM с помощью VS Code Tunnel (а не SSH).
- **Dev Containers** - работайте с отдельным инструментарием или приложением на основе контейнера, открывая любую папку, смонтированную в контейнере или внутри него.
- **WSL** - откройте любую папку в подсистеме Windows для Linux, чтобы получить опыт разработки под Linux, не выходя из Windows.

## 13. Russian Language Pack for Visual Studio Code

[ссылка на Marketplace](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ru)

Переводит интерфейс VS Code на Русский язык

Это лишь малая часть плагинов которую я использую, для работы, ваш список может быть намного больше.




