**Как написать критерии приемки: Определение, форматы, примеры**

![alt text](Image/image15.png)

**Оглавление:**
- [Что такое критерии приемки?](#что-такое-критерии-приемки)
- [Почему важны критерии приемки?](#почему-важны-критерии-приемки)
- [Критерии приемки в методологиях agile](#критерии-приемки-в-методологиях-agile)
- [Как написать критерии приемки (7 шагов)](#как-написать-критерии-приемки-7-шагов)
- [Лучшие практики написания критериев приемки](#лучшие-практики-написания-критериев-приемки)
- [Пример критериев приемки](#пример-критериев-приемки)
- [Предписывающие и направляющие критерии приемки](#предписывающие-и-направляющие-критерии-приемки)
  - [Предписывающие критерии приемки](#предписывающие-критерии-приемки)
    - [Цель предписывающих критериев приемки](#цель-предписывающих-критериев-приемки)
- [Руководящие критерии приемки](#руководящие-критерии-приемки)
  - [Пример руководящих критериев приемки](#пример-руководящих-критериев-приемки)
- [Сочетание руководящих и предписывающих критериев приемки](#сочетание-руководящих-и-предписывающих-критериев-приемки)
- [Критерии приемки в сравнении с определением выполненной работы](#критерии-приемки-в-сравнении-с-определением-выполненной-работы)
- [Дано - Когда - Тогда(Given-When-Then)](#дано---когда---тогдаgiven-when-then)
- [Gherkin  язык и его использование при написании критериев приемки](#gherkin--язык-и-его-использование-при-написании-критериев-приемки)
- [Заключение](#заключение)

## Что такое критерии приемки?

Критерии приемлемости - это набор заранее определенных условий, которым должен соответствовать продукт или функция, чтобы быть принятым заказчиком, заинтересованными сторонами проекта или командой управления продуктом. Они служат важным руководством для разработчиков в процессе разработки и помогают убедиться, что конечный продукт соответствует предполагаемым потребностям пользователей и бизнес-целям.

Заблаговременное определение критериев приемки позволяет командам лучше управлять ожиданиями, упростить коммуникацию и снизить вероятность неправильного толкования на протяжении всего жизненного цикла разработки продукта.

## Почему важны критерии приемки?

Критерии приемки играют важную роль в управлении продуктом, потому что они:

**Обеспечьте четкие рекомендации** - критерии приемки описывают, что ожидается от продукта или функции. Такая ясность помогает объединить все заинтересованные стороны, включая разработчиков, тестировщиков и бизнес-заказчику, в понимании того, что должно быть достигнуто


**Облегчение и понимание в командах** - четко определив ожидаемый результат функции или продукта, каждый знает, к чему стремиться и что будет считаться успехом, что, в свою очередь, сводит к минимуму возможность недопонимания.

**Основа для тестирования** - тестировщики могут использовать критерии приемки, чтобы определить, работает ли продукт или функция так, как задумано. Если разработанная функция соответствует всем описанным условиям, ее можно пометить как завершенную

**Помощь в управлении ожиданиями клиентов и повышении удовлетворенности** - когда клиенты участвуют в определении критериев приемки, они лучше понимают, чего ожидать от конечного продукта, что приводит к повышению удовлетворенности, когда эти ожидания оправдываются.

## Критерии приемки в методологиях agile

Критерии приемки играют незаменимую роль, направляя команды agile-разработчиков на достижение конечной цели: предоставление пользователям высококачественного программного обеспечения.

Agile-практики подчеркивают важность сотрудничества, гибкости и удовлетворенности клиентов. Критерии приемки поддерживают эти ценности, обеспечивая понимание всеми членами команды того, что должно быть сделано и как будет измеряться успех. Они обеспечивают общее понимание требований и предотвращают поползновения к увеличению объема, удерживая внимание на том, что действительно важно: эффективном и качественном удовлетворении потребностей пользователей.

Кроме того, четко сформулированные критерии приемки обеспечивают эффективные процессы тестирования в agile-командах. Заранее установив четкие ожидания, тестировщики могут разрабатывать более точные тестовые примеры, которые соответствуют желаемым результатам.

## Как написать критерии приемки (7 шагов)

Критерии приемки служат важнейшей дорожной картой для менеджеров по продукту, направляя процесс разработки и задавая четкие ожидания того, как должен выглядеть готовый продукт или функция.

Вот пошаговое руководство по созданию четких, лаконичных критериев приемки, которые способствуют успешной разработке продукта:

1. **Определите user story** - начните с определения user story, для которой предназначена ваша функция или продукт. User story описывает действие или цель с точки зрения пользователя, например, "Как читатель блога, я хочу иметь возможность сохранять статьи, чтобы прочитать их позже".
2. **Определите желаемый результат** - после того как вы определили историю пользователя, пришло время определить, как выглядит успех. Здесь вы описываете желаемый результат в четких и конкретных терминах. Например, "Читатель блога может легко сохранить любую статью и позже получить к ней доступ из своего личного списка для чтения".
3. **Детализация требований** - далее подробно опишите все требования, которые должны быть выполнены для достижения результата. Сюда могут входить технические спецификации, элементы дизайна или другие факторы, способствующие достижению желаемого результата
4. **Создание сценариев** - сценарии представляют собой конкретные примеры того, как пользователи могут взаимодействовать с вашим продуктом или функцией. Создавая такие сценарии, вы сможете лучше понять, как ваши критерии приемки будут работать в реальных ситуациях.
5. **Обеспечьте ясность и простоту** - критерии приемлемости должны быть простыми и понятными для всех участников проекта, от разработчиков и дизайнеров до заинтересованных сторон и конечных пользователей.
6. **Обращайтесь за обратной связью** - Прежде чем окончательно сформулировать критерии приемки, запросите отзывы у всех заинтересованных сторон. Это поможет убедиться в том, что критерии приемки являются всеобъемлющими и соответствуют ожиданиям каждого.
7. **Регулярный пересмотр** - по мере продвижения работы над продуктом или функцией регулярно пересматривайте критерии приемки, чтобы убедиться, что они по-прежнему актуальны и полезны.

## Лучшие практики написания критериев приемки

Написание эффективных критериев приемки - важнейшая часть жизненного цикла управления продуктом, и вам следует позаботиться о том, чтобы они были написаны с четкой конечной целью. Ниже приведены некоторые советы и лучшие практики по написанию четких и понятных критериев приемки для ваших пользовательских историй:

- **Начните с конца** - прежде чем приступить к написанию критериев приемки, необходимо четко понимать, чего вы хотите добиться с помощью вашей функции или продукта. Как выглядит успех? Что должно произойти, чтобы продукт или функция считались завершенными?
- **Будьте конкретны и лаконичны** - избегайте расплывчатых формулировок и убедитесь, что каждый критерий точен и прост для понимания. Каждый критерий должен описывать конкретный аспект функциональности
- **Используйте простой язык** - ваши критерии приемки должны быть понятны всем членам вашей команды, независимо от их технических знаний.
- **Сосредоточьтесь на пользователе** - помните, что критерии приемки - это определение того, что удовлетворит потребности пользователя и решит его проблемы. Держите пользователя в центре вашего процесса написания
- **Сотрудничайте со своей командой** - написание критериев приемки не должно происходить в одиночку. Привлеките к этому процессу свою команду, поскольку они могут дать ценную информацию и помочь убедиться, что все находятся на одной волне в отношении того, что должно быть достигнуто
- **Проверяемые условия** - убедитесь, что каждый критерий описывает условие, которое можно протестировать после завершения разработки.
- **Включите как функциональные, так и нефункциональные требования** - в то время как функциональные требования описывают, что делает продукт, нефункциональные требования касаются того, насколько хорошо он выполняет определенные функции, или его качеств, таких как безопасность, производительность, дизайн и т.д.

## Пример критериев приемки

Понимание и эффективное использование критериев приемки может стать решающим фактором. Эти важнейшие рекомендации служат дорожной картой для команд разработчиков, определяя, как должен выглядеть готовый продукт или функция с технической и пользовательской точек зрения.

Вот пример, показывающий, как критерии приемки могут выглядеть на практике. Описанные ниже критерии призваны улучшить коммуникацию в вашей команде, оптимизировать процессы тестирования, лучше управлять ожиданиями клиентов и в конечном итоге повысить их удовлетворенность конечным продуктом или функцией.

Допустим, вы управляете функцией регистрации в приложении. Приведенные ниже критерии приемки описывают опыт пользователя при регистрации с использованием его электронной почты:

- Пользователи должны иметь возможность зарегистрироваться, используя адрес электронной почты
- Регистрационная форма должна содержать поля для ввода имени, фамилии, адреса электронной почты, пароля и подтверждения пароля
- Поле пароля должно иметь правила проверки - минимум восемь символов, как минимум одна заглавная буква, одна строчная буква, одна цифра и один специальный символ
- Перед входом в систему пользователи должны подтвердить свой адрес электронной почты
- После успешной регистрации пользователи должны получить подтверждение по электронной почте
- Если пользователи пытаются зарегистрироваться с уже зарегистрированным адресом электронной почты, они должны получить сообщение об ошибке
- Каждый шаг при создании этих критериев приемки был направлен на ясность и удобство использования как с точки зрения разработчика (который будет использовать их в качестве руководства для создания функций), так и с точки зрения пользователя (который будет взаимодействовать с этими функциями).

## Предписывающие и направляющие критерии приемки

Существует два основных подхода к разработке критериев приемки: предписывающий и направляющий. Понимание того, нужны ли вашему проекту предписывающие или направляющие критерии приемки, в конечном итоге зависит от таких факторов, как динамика команды, сложность проекта и организационная культура.

Предписывающий подход, как правило, является более детальным и конкретным, точно определяя, как должна функционировать или выглядеть та или иная функция. С другой стороны, направляющие критерии приемки дают более широкий взгляд, предоставляя разработчикам большую свободу в поиске решений, но при этом не нарушая общей цели.

В таблице ниже приведены основные различия между двумя подходами:

| Предписывающие критерии приемки                                             | Направляющие критерии приемки                                     |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------|
| Конкретные детали того, как функция должна функционировать или выглядеть    | Высокоуровневое представление о том, что должно быть достигнуто   |
| Ограничивает творческий потенциал разработчика, определяя точные требования | Способствует творческому решению проблем в установленных границах |
| Снижает риски двусмысленности и неправильного толкования                    | Требуется активная коммуникация, чтобы избежать недопонимания     |
| Это может привести к увеличению времени разработки из-за строгих правил     | Можно ускорить время разработки за счет повышения гибкости        |

Давайте рассмотрим оба подхода подробнее:

### Предписывающие критерии приемки

Когда кто-то говорит о критериях приемки, он обычно имеет в виду предписывающие критерии приемки.

Предписывающие критерии можно рассматривать в двух аспектах:

- Они служат в качестве подробного списка требований.
- Вы можете использовать их как пользовательские истории, разбитые на более мелкие части

![alt text](Image/image1.png)


**Пример предписывающих критериев приемки**

Давайте рассмотрим пример предписывающих критериев приемки.

**История**: Передача премиальных баллов

**Критерии приемки**:

- Кнопка  с текстом о **переводе баллов** на главной странице

- Когда пользователь нажимает на кнопку, он видит модальное окно **перевода баллов**, которое включает в себя:
    
    - Выпадающий список друзей (обязательно)
    - Кнопка **добавления друга**.
    - Поле для количества баллов (обязательно)
    - Кнопка "**Отправить**"
    - Кнопка **"Отмена"**
- Пользователь выбирает друга из выпадающего списка
- Пользователи могут ввести в поле от 100 до 1000 баллов
- Если у них недостаточно баллов, показать модальное окно с ошибкой
- Если они введут слишком мало или слишком много баллов, показать модальное окно ошибки
- Когда Пользователь нажмёт кнопку "Отправить", проверьте правильность заполнения всех полей.
    
    - Если нет, выдает стандартную ошибку проверки
    - Если да, покажите еще один модальный экран "Вы уверены?
       
       - Нажатие кнопки "Да" завершает передачу
       - При нажатии кнопки "Нет" пользователь возвращается к окну перевода баллов*.
    - После завершения перевода добавьте транзакцию в историю отправителя и получателя с заголовком: Points transfer: {amount} от {userID} к {userID}


#### Цель предписывающих критериев приемки

Существует множество причин для использования критериев приемки в процессе разработки продукта. Наиболее распространенные из них включают:

- Управление ожиданиями
- Управление объемом работ
- Служит основой для оценки

**Managing expectations**

Критерии приемки помогают управлять ожиданиями как между PM и командой разработчиков продукта, так и между командой и заинтересованными сторонами.

Они точно определяют, как будет работать та или иная функция. Если в пользовательской истории "Я хочу войти в систему" в критериях приемки есть опция "Войти через Google", это формирует четкие ожидания, что пользователи смогут войти в систему через Google, но, возможно, не обязательно через Facebook.

Хорошие критерии приемки не оставляют места для неверного толкования.

**Управление объемом работ**

Кому никогда не приходилось сокращать объем работ, чтобы уложиться в срок?

Критерии приемки помогают руководителям в определении объема работ, как при добавлении, так и при исключении объема из инициативы. В конце концов, вы, вероятно, не можете удалить пользовательскую историю "Я хочу войти в систему", но вы можете убрать ее из причудливых критериев приемки и оставить только основы.

Критерии приемки помогут вам управлять объемом с более высокой точностью, как скальпель.

**Служит основой для оценки**

Чем более расплывчатым является объект оценки, тем более расплывчатой будет оценка. Критерии приемки предоставляют столь необходимые детали, чтобы сделать оценку разработки более точной. В конце концов, можно потратить час или неделю на работу над историей "Я хочу войти в систему", в зависимости от точных деталей процесса входа.

**Служат в качестве исходных данных для планов тестирования**

Критерии приемки служат ценным вкладом в работу команды QA, когда речь идет о подготовке тестовых примеров. При правильно написанных критериях приемки они точно знают, что тестировать и как должна работать та или иная функциональность. В противном случае им, вероятно, пришлось бы постоянно задавать команде вопросы типа "это ошибка или фича?".

## Руководящие критерии приемки

На определенном уровне зрелости команды разработчиков подробные описания решений не только не нужны, но и зачастую сильно ограничивают возможности.

В таких случаях разумнее написать критерии приемки в виде общих целей высокого уровня.

Речь идет о том, чтобы задать команде высокоуровневое направление и позволить ей самой додумать остальное.

### Пример руководящих критериев приемки

**История**: Перевод премиальных баллов

**Критерии приемки**:
- Пользователь должен иметь возможность перевести до 1000 баллов на счет друга
- Процесс должен быть простым и удобным для пользователя
- Не усложняйте. Давайте попробуем сделать MVP за один спринт
- Включите механизмы, предотвращающие случайную передачу баллов
- Документируйте и храните все переводы

Такое описание дает достаточно деталей, чтобы определить границы инициативы, но в то же время дает команде право самой определять точные детали. В конце концов, продуктовые команды лучше всего подходят для определения фактического решения, и менеджеры по продуктам должны сделать все возможное, чтобы дать им такую возможность.

## Сочетание руководящих и предписывающих критериев приемки

Различные типы критериев приемки имеют разное назначение для команды разработчиков.

Руководящие критерии приемки хорошо работают как форма высокоуровневых границ. Донесите проблему до команды, позвольте им найти потенциальные решения, а когда вы определитесь с направлением, установите границы для решения, основываясь на потребностях и ограничениях бизнеса.

Затем, когда команда определит детали решения (иногда консультируясь с менеджерами продукта, иногда самостоятельно), позвольте им написать более подробные, предписывающие критерии приемки, которые помогут им управлять ожиданиями и объемом.

![alt text](Image/image2.png)

В конечном счете, это не руководящие и не предписывающие критерии приемки. И те, и другие служат разным целям на разных этапах разработки решения.

## Критерии приемки в сравнении с определением выполненной работы

Одна из распространенных путаниц - разница между критериями приемки и определением "сделано".

Хотя они служат схожей цели, есть одно большое различие. Определение выполненного является общим для всех пользовательских историй, в то время как критерии приемки зависят от конкретной истории.

![alt text](Image/image3.png)

Кроме того, критерии приемки обычно работают как контрольный список разработки, а определение выполненного - как контрольный список целостного процесса.

Другими словами, критерии приемки включают в себя то, что должно быть создано как часть функции, например, функции "войти в Google" и "отправить мне волшебную ссылку".

В то же время определение "сделано" описывает весь путь пользовательской истории (например, разработку, тестирование, написание документации, проведение стресс-тестов и все, что входит в определение "сделано").

Только когда выполнены и критерии приемки, и определение done, история считается полностью завершенной.

## Дано - Когда - Тогда(Given-When-Then)

Дано - Когда - Тогда (GWT) - это полуструктурированный формат для написания тестовых примеров. Для менеджеров по продукту это популярный метод определения критериев приемки.

Этот подход, также известный как разработка, ориентированная на поведение (BDD), позволяет менеджерам по продукту четко выразить ожидаемое поведение функции или продукта.

Структура Given-When-Then работает следующим образом:

- **Дано** некоторые исходные условия, ...
- **Когда** происходит событие, ...
- **Тогда** обеспечить определенные результаты.

Например, рассмотрим простую историю пользователя: "Как читатель блога, я хочу иметь возможность сохранять статьи, чтобы читать их позже". Критерии приемки, использующие формат Given-When-Then, могут выглядеть следующим образом:

---

**Дано** я зарегистрированный пользователь и вошел в систему, **Когда** я нажимаю на кнопку "Сохранить статью", **Тогда** статья должна быть добавлена в мой список сохраненных статей.

---

Такой формат обеспечивает ясность и позволяет всем участникам проекта, от разработчиков до заинтересованных сторон, понять, чего необходимо достичь.

## Gherkin  язык и его использование при написании критериев приемки

Gherkin - это язык, специфичный для конкретной области, используемый для определения приемочных тестов в BDD. По умолчанию он использует обычный английский язык, но поддерживает несколько языков, что делает его доступным для непрограммистов, участвующих в проектах по разработке программного обеспечения.

Структура Gherkin похожа на структуру формата Given-When-Then. Типичный сценарий Gherkin состоит из:

- Заголовок, поясняющий, что именно тестируется
Шаг "**Дано**" или шаги, задающие условия
Шаг "**Когда**", описывающий ключевое действие
Шаг "**Тогда**" или шаги, определяющие ожидаемый результат

Вот как может выглядеть наш предыдущий пример, написанный на языке Gherkin:

---

Сценарий: Сохранение статьи

**Дано**, что я зарегистрированный пользователь и вошел в систему, **когда** я нажимаю на кнопку "Сохранить статью", **тогда** статья должна быть добавлена в список моих сохраненных статей

---

Использование языка Gherkin при написании критериев приемки позволит вам предоставить команде легкие для понимания рекомендации, которые помогут оптимизировать процессы разработки и тестирования.


## Заключение
Существует два типа критериев приемки. Руководящие критерии приемки служат высокоуровневым направлением и границами для команды разработчиков. Предписывающие критерии приемки служат более подробным контрольным списком, который помогает управлять ожиданиями и объемом, оценивать билеты и планировать тестовые случаи.

Менее зрелые команды обычно получают требования с заранее определенным набором критериев приемки. Но когда команда становится зрелой, она пишет свои собственные критерии приемки, основываясь на решаемой проблеме и высокоуровневых руководящих критериях приемки.

Хотя критерии приемки похожи по концепции на определение "сделано", в то время как первые относятся к форме конкретной истории, вторые определяют путь, который должна пройти каждая пользовательская история в рамках процесса разработки.