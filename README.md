# [Russian Speaking] Scala User Group

Можно задавать любые вопросы по теме, от совсем базовых, до требующих многолетних исследований. Но если постите примеры кода, то делайте его компилируемым. Шансы на помощь возрастают многократно. Подойдут сервисы https://scastie.scala-lang.org, https://scalafiddle.io. В крайнем случае gist, там хотя бы история и комменты есть. Игнорирование просьб выложить код в текстовом виде, может привести к запрету постить медиа файлы.

## Telegram
* Russian chat: https://t.me/scala_ru (правила - https://gist.github.com/fomkin/5ff77f44ddbdc54ef149b16ee8515b25)
* English chat: https://t.me/scala_en
* Jobs chat [En]: https://t.me/scala_jobs_en
* Flood and Jobs chat [Ru]: https://t.me/scala_jobs
* Jobs channel (without flood): https://t.me/scala_jobs_feed
* Чат для новичков, где любые вопросы по Scala - нестыдные: https://t.me/scala_learn
* Отдельный чат про ToFu: https://t.me/tofu_ru
* Канал с полезняшками: https://t.me/scala_channel_ru
* Канал Дениса Михайлова aka @notxcain: https://t.me/notxcain_tech_feed
* Газетка участников ПОНВа. https://t.me/daily_ponv
* Чат по теоркату: https://t.me/ru_catheory
* Хацкеллевый чат (если вы чувствуете себя как Фоммил или Моррис): https://t.me/haskellru
* Зав. типы и идрис в частности (когда и скалы и хацкелля мало, делать нечего и хочется по лезвию еще не отполированного ножа ходить): https://t.me/joinchat/Ai4h2D9SWO_RDx2jMUbzqw
## Gitter
* От сообщества dev-ua: https://gitter.im/dev-ua/scala
* От телеграмовского сообщества: https://gitter.im/scala-russian/Lobby
* ПОНВ (отщепенцы, дорвавшиеся до TeX): https://gitter.im/scala-russian/ponv
## Meetup
* https://www.meetup.com/Scala-Moscow/
* https://www.meetup.com/ScalaSpb/
## Media
* Подкаст "Скалалаз" https://scalalaz.ru
  * Все материалы, публикуемые на сайте, лежат в открытом доступе тут https://github.com/scalalaz-podcast/scalalaz-gen/
  * Любая помощь по улучшению сайта (дизайн, опечатки, улучшение генерации, и т.п.) в виде пулл реквестов - привествуется (не стесняйтесь!)
    * Если нет никакой возможности помочь пулл реквестами - то в чате (https://t.me/scala_ru) можно (и нужно) писать и спрашивать как по техническими вопросам так и по содержанию выпусков.
* Англоязычный подкаст "Скалалав" https://scala.love/hello-scala/ от неугомонной @oli_kitty
## Youtube
* https://www.youtube.com/channel/UCR4iuvbk9DCuieR1ADIi0-Q
## Образование
* Ставший классикой курс https://courseware.epfl.ch/courses/course-v1:EPFL+progfun1+2018_T1/about (раньше жил на курсере)
* Проект fp speedrun. Веб занятия со студентами, желающими освоить функциональной программирование и средства для него в scala. https://github.com/scala-russian/fpspeedrun/wiki
* Основы языка на русском от одного из Олегов https://stepik.org/course/16243
* Подборки "Как вкатиться в скалу?" - https://gist.github.com/d1egoaz/2180cbbf7d373a0c5575f9a62466e5e1, https://stackoverflow.com/tags/scala/info
* Путь Олега: "для популярных языков общего назначения в первую очередь я пишу хелловорлд, потом пишу какие-то олимпиадные задачки, потом ищу самую хайповую на текущий момент хттп либу и пишу в ней что-то".
* Кружок изучающих Proof Theory под руководством @clayrat 
** https://t.me/proof_theory
** https://www.youtube.com/channel/UC8reF8xuw05LOYLeWNRV0pg
** https://github.com/sequents
## Символика и искусство
* https://github.com/angel608/pero_scala_art - исходный арт геральдики сообщества
* http://scalarussiafeather.printdirect.ru/ - сразу заказать
* https://github.com/scala-russian/scala_ru_stickers - подборка стикеров от Вадима Челышева
* https://impurepics.com - Работы наскального художника @Zelenya (https://twitter.com/impurepics)
* https://drive.google.com/drive/folders/1ZyYWvbs6TKa5U7dKsGlS6ru3t7QGp3gL -  его же шаурма-cat

## FAQ
* Что за TF все упоминают? Tagless Final - подход для создания EDSL, альтернатива Free и просто модно в 2018. Почитать стоит http://okmij.org/ftp/tagless-final/course/lecture.pdf и славянофильское https://habr.com/post/325874/
* А как сделать вот такую хитрую вещь? - возможно ответ есть в https://github.com/Odomontois/manatki
* Нужно ли изучать хацкелль, чтоб писать на скалке с котами и прочими крутыми штуками? Нет.
* Нужно ли изучать теорию категорию и прочий функан (с), чтобы писать на скалке с котами и прочими крутыми штуками? Нет. Хотя может дать некоторую интуицию и разочарование в происходящем, предварительно пожрав время. (Спойлер. Для хацкелля ответ такой же.)
* Что не так с Future? 
  - Комбинация только с помощью имплиситного экзекьютора. Можно сломать фор-компрехеншен случайным импортом
  - Почти каждая операция требует запуска как минимум одного Runnable. Т.е. синхронизация стейта пулов на каждый шаг. Это действительно сильно аффектит производительность реальных конкурентных приложений
  - eager by default. Ничего не мешает воспользовать тем же трейт, чтобы реализовать запуск by need, но это сломает большую часть утилит,  они часто исходят из предположения о немедленном запуске
  - Стандартные реализации фьючи мутабельные. Сильно. Утилитарный код может порождать множество гейзенбагов, если не учёл все особенности комплита и линка и не перепроверил что-то дважды\не синхронизировался.
  - Ручное управление конкаренси. Отличие параллельного от последовательного запуска обычно - это отличие в def vs val. Маленькая ошибка может превратить асинхронный стрим в мемори лик.
  - Отсутствие cancelation во встроенной реализации. И не самый простой способ использовать в twitter. Случайно не выполненный вызов сайдэффектящего метода в твиттер приводит к неотменяемости. 
  - Предыдущее также сильно затруднаяет финализацию ресурсов в конкуретном коде
  - Стандартный способ интеграции - промис. И отсутствие встроенного набора конкурентных данных как в  cats-effect\zio принуждает пользоваться им довольно часто. Намеренно незавершённый промис - это не отмена, а утечки памяти и нефинализированных ресурсов.
  - При написании АПИ, если нужно принять асинхронный процесс в качестве параметра, каждый способ сделать это чем-то плох. Приём by name (=> Future[A]) кажется самым прямым аналогом получения IO[A], однако постоянно ломается при доработках, в особенности новичками. Где-то лишний вал - и фьюча запустилась
