![alt text](/Languages/JSON/image/image10.png)

## Оглавление:

- [Синтаксис JSON и типы данных](#синтаксис-json-и-типы-данных)
- [Как работает JSON](#как-работает-json)
- [Правила наименования json объектов](#правила-наименования-json-объектов)
- [Альтернативы JSON](#альтернативы-json)
- [Резюме](#резюме)


JavaScript Object Notation (JSON) - это стандартный формат файлов, используемый для обмена данными. Объекты данных хранятся и передаются с помощью пар ключ-значение и типов данных массивов.

JSON имеет синтаксическое сходство с JavaScript, поскольку JSON основан на синтаксисе объектной нотации JavaScript. Но формат JSON - это только текст, что делает его легко читаемым и используемым с любым языком программирования.

# Синтаксис JSON и типы данных

Правила записи данных в формате JSON аналогичны JavaScript Object Literals.

Вкратце они сводятся к следующему:

1. Все данные JSON записываются внутри фигурных скобок
2. Данные JSON представлены в виде пар ключ-значение
3. Ключ всегда должен быть заключен в двойные кавычки
4. Всегда разделяйте ключ и значение двоеточием (`:`)
5. Значения должны быть записаны соответствующим образом; для строк следует использовать двойные кавычки, а для чисел, булевых кавычек не должно быть.
6. Для разделения данных следует использовать запятые (,)
7. Для квадратных скобок массивов и объектов следует использовать фигурные скобки

Пример, чтобы понять, что означают приведенные выше правила:

![alt text](/Languages/JSON/image/image1.png)

Данные JSON не слишком гибко реагируют на эти правила. Небольшое нарушение этих правил может привести к поломке вашего кода. Обязательно проверяйте данные JSON с помощью любых онлайн валидаторов JSON.

Для представления данных в JSON используются объекты или массивы (как показано в примере выше). Эти данные содержат значения (ключи), которые могут быть следующих форматов -

1. Число (целое или десятичное)
2. Строка (должна быть заключена в двойные кавычки)
3. Булево (т.е. истина или ложь)
4. Null
5. Объекты (Object)
6. Массивы (Arrays)

Объект - это коллекция пар ключ-значение, определяющая набор данных, а массив - это упорядоченный список значений. Объекты JSON могут содержать несколько массивов JSON и наоборот.

**Объявление массива JSON**

[

    "test 1", "test 2", "test3"
    
]

**Объявление объекта JSON**

{

"id": 54d56a2c4,

"Name": "Perovich.tuta",

"Contact": "test@mailtu.com",

"careerPrograms": ["Crio Launch", "Crio Accelerate"]

}

Соблюдение указанного выше отступа при написании JSON не обязательно, но это делает его более читабельным.

Вы можете располагать пары ключ-значение как угодно, поскольку JSON игнорирует пробелы между своими элементами.

# Как работает JSON

Теперь вы, возможно, задаетесь вопросом о "сложном" механизме, который JSON использует для передачи этих данных. Оказывается, процесс не такой уж и сложный. Он использует вычислительный метод под названием **Serialization**.

Рассмотрим приложение, работающее на определенной физической машине. Если оно хочет отправить какие-то данные другому приложению на той же или другой машине, оно может передать их с помощью какого-то подходящего сетевого протокола. Но вот в чем загвоздка. Данные не могут быть отправлены как они есть, то есть как один большой кусок данных, который машина низкого уровня не может понять. Чтобы две машины могли понять данные, они должны быть представлены в виде битов, то есть 0 и 1.

Другими словами, передача данных должна происходить в виде битов/байтов. Именно это и делает сериализация.

**Serialization** - это механизм, который преобразует состояние объекта данных в строку битов, называемую потоком байтов (или байтовой строкой). И как только другая машина получает этот поток байтов, ей необходимо "десериализовать" поток байтов обратно в исходное состояние объекта данных, чтобы его можно было комфортно использовать в дальнейшем.

Этот механизм сериализации-дерегуляции обеспечивает постоянство объектов данных в различных приложениях.

Формат JSON кодирует объекты в строку. Однако при передаче или хранении данных в файле они должны быть байтовыми строками. Это не обычный формат сложных объектов.

Сериализация преобразует эти сложные объекты в байтовые строки для такого использования. Это и есть механизм работы JSON.

Преимущество этого метода в том, что он не потребляет много памяти, а значит, делает JSON легким инструментом (как уже говорилось) и идеальным для передачи данных.

![alt text](/Languages/JSON/image/image2.png)

Итак, кто именно выполняет сериализацию-дезериализацию? Этим занимается язык программирования, который вы используете.


# Правила наименования json объектов

При именовании объектов JSON важно следовать определенным соглашениям и лучшим практикам, чтобы обеспечить ясность, удобство обслуживания и совместимость. Вот некоторые ключевые правила и рекомендации:

1. Используйте описательные имена
   - Выбирайте имена, которые четко описывают данные, которые они представляют. Например, используйте userProfile вместо просто profile.

2. Верблюжий или змеиный регистр
   - Верблюжий регистр: Используйте camelCase (например, firstName, lastName) для JavaScript и многих других языков.
   - Змеиный регистр: Используйте snake_case (например, first_name, last_name), если он лучше согласуется с концепцией вашего проекта.

3. Избегайте специальных символов
   - Придерживайтесь буквенно-цифровых символов и знаков подчеркивания. Избегайте пробелов, знаков препинания и специальных символов.

4. Начинайте с буквы
   - Имена должны начинаться с буквы (a-z, A-Z). Это помогает избежать проблем в некоторых средах программирования.

5. Будьте проще
   - Избегайте слишком сложных имен. Пусть они будут краткими и в то же время описательными.

6. Последовательность - это ключ
   - Будьте последовательны в своих соглашениях об именовании во всей структуре JSON. Если вы начали с camelCase, продолжайте использовать его.

7. Уместно использовать множественное число
   - Используйте имена во множественном числе для массивов (например, users для массива объектов user) и в единственном числе для одиночных объектов (например, user).

8. Избегайте зарезервированных ключевых слов
   - Избегайте использования зарезервированных ключевых слов из языков программирования (таких как class, function и т. д.) в качестве имен.

9. Учитывайте типы данных
   - При необходимости называйте свойства в соответствии с их типами данных (например, isActive для булевого значения).

10. Документируйте структуру
       - Если структура JSON сложная, задокументируйте ее, чтобы прояснить назначение каждого объекта и свойства.


# Альтернативы JSON

- **YAML** - это ведущая альтернатива JSON. Это надмножество формата, имеющее более человекочитаемое представление, пользовательские типы данных и поддержку ссылок. Он призван решить большинство проблем с удобством использования, связанных с JSON.
  
YAML получил широкое распространение в файлах конфигурации и в инструментах DevOps, IaC и observability. Реже он используется в качестве формата обмена данными для API. Относительная сложность YAML делает его менее доступным для новичков. Небольшие синтаксические ошибки могут привести к сбоям при разборе.

- **Protocol buffers (protobufs)** - еще один новый соперник JSON, предназначенный для сериализации структурированных данных. **protobufs** имеют объявления типов данных, обязательные поля и поддерживают большинство основных языков программирования. Эта система набирает популярность как более эффективный способ передачи данных по сетям.




# Резюме
**JSON** - это текстовый формат представления данных, который может кодировать шесть различных типов данных. JSON стал неотъемлемой частью экосистемы разработки программного обеспечения; он поддерживается всеми основными языками программирования и стал выбором по умолчанию для большинства REST API, разработанных за последние пару десятилетий.

Хотя простота JSON является частью его популярности, она также накладывает ограничения на то, чего вы можете достичь с помощью этого формата. Отсутствие поддержки схем, комментариев, объектных ссылок и пользовательских типов данных означает, что некоторые приложения перерастут возможности JSON. Более молодые альтернативы, такие как **YAML** и **Protobuf**, помогли решить эти проблемы, в то время как **XML** остается претендентом для приложений, которые хотят определить схему данных и не возражают против многословности.

