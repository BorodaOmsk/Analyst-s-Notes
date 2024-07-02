
## Пример cоздание Swagger-документации

## Оглавление:

- [Шаг 1: Установите Swagger Tools](#шаг-1-установите-swagger-tools)
- [Шаг 2: Создайте базовый файл Swagger](#шаг-2-создайте-базовый-файл-swagger)
- [Шаг 3: Определите путь для вашего эндпоинта](#шаг-3-определите-путь-для-вашего-эндпоинта)
- [Шаг 4: Определите схемы данных](#шаг-4-определите-схемы-данных)
- [Шаг 5: Проверка и использование](#шаг-5-проверка-и-использование)
      - [Использование Swagger Editor](#использование-swagger-editor)
      - [Локальное использование Swagger UI](#локальное-использование-swagger-ui)

Создание Swagger-документации для отдельной API-постановки, такой как **GET** `/admin/realms/{realm}/users`, включает несколько шагов. Вот пошаговая инструкция:

# Шаг 1: Установите Swagger Tools
Для начала установим необходимые инструменты для работы со Swagger. Если вы используете Node.js, можно установить Swagger UI и Swagger Editor через npm:


    npm install swagger-ui swagger-editor


# Шаг 2: Создайте базовый файл Swagger
Создайте файл swagger.yaml или swagger.json, который будет содержать базовую информацию о вашем API.


    openapi: 3.0.3
    info:
      title: Example API
      description: API для управления пользователями
      version: 1.0.0
    servers:
    - url: http://localhost:8080/api


# Шаг 3: Определите путь для вашего эндпоинта
Теперь добавим информацию о вашем эндпоинте GET /admin/realms/{realm}/users.


    paths:
      /admin/realms/{realm}/users:
        get:
          summary: Получить список пользователей
          description: Возвращает список всех пользователей в указанном realm.
          parameters:
          - name: realm
              in: path
              required: true
              description: Уникальный идентификатор realm.
              schema:
               type: string
          responses:
           '200':
             description: Успешный ответ
              content:
                application/json:
                  schema:
                    type: array
                    items:
                      $ref: '#/components/schemas/User'
            '400':
              description: Неверный запрос
            '404':
              description: Realm не найден


# Шаг 4: Определите схемы данных
Добавьте схему данных для ресурса User, который возвращается в ответе.


    components:
      schemas:
        User:
          type: object
         properties:
            id:
              type: string
            username:
              type: string
            email:
              type: string
            firstName:
              type: string
           lastName:
              type: string


# Шаг 5: Проверка и использование
Теперь, когда ваш `swagger.yaml` файл готов, вы можете проверить его с помощью **Swagger Editor** или **Swagger UI**.

#### Использование Swagger Editor
1. Откройте Swagger Editor: [https://editor.swagger.io/](https://editor.swagger.io/)
2. Вставьте содержимое вашего swagger.yaml в редактор.
3. Проверьте на наличие ошибок и убедитесь, что всё отображается корректно.

#### Локальное использование Swagger UI
Создайте простой HTML-файл для отображения вашего Swagger-документа:


    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <title>Swagger UI</title>
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/swagger-ui/3.52.5/swagger-ui.css" >
    </head>
    <body>
    <div id="swagger-ui"></div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/swagger-ui/3.52.5/swagger-ui-bundle.js"></script>
    <script>
        window.onload = function() {
        const ui = SwaggerUIBundle({
            url: "path/to/your/swagger.yaml",
            dom_id: '#swagger-ui',
        })
        }
    </script>
    </body>
    </html>


Замените `"path/to/your/swagger.yaml"` на путь к вашему файлу. Откройте этот HTML-файл в браузере, и вы увидите визуализацию вашего API.

Теперь у вас есть полная документация для эндпоинта **GET** `/admin/realms/{realm}/users` с использованием Swagger!