# Course-project-Itra
Условие курсового проекта (.NET/Java/Front).

УСЛОВИЕ КУРСОВОГО ПРОЕКТА
.NET, Core, C#, ASP.NET в любой реинкарнации, Entity Framework, SQL Server, *опционально* React
Java, Spring, Hibernate, MySQL, *опционально* React
Front, TypeScript/JavaSсript, React (по отдельной договоренности можно Angular), Node.js, Express, MySQL или MongoDB

ВНИМАНИЕ: условие проекта для направления iOS выдаст Ольга.

Требуется разработать сайт для управления личными коллекциями (книги, марки, значки, виски, etc. — далее в тексте то, из чего состоит коллекция, называется айтемами).

Неаутентифицированным пользователи доступен только режим read-only (доступен поиск, недоступно создание коллекций и айтемов, недоступны комментарии и лайки).

Аутентифицированные пользователи имеют доступ ко всему, кроме админки.

Админка позволяет управлять пользователями (просматривать, блокировать, удалять, назначать других админами). Администратор видит каждую страницу пользователя и каждую коллекцию как ее создатель-владелец (например, может отредактировать или создать от имени пользователя с его страницы новую коллекцию или добавить айтем и т.п.). Пояснение: для админа не нужно делать отдельные вьюшки (кроме "админки", конечно).

Только владелец или админ может управлять коллекцией (редактировать/добавлять/удалять).

Требуется поддерживать вход через социальные сети (не менее двух).

На каждой странице доступен полнотекстовый поиск по сайту (результаты поиска - всегда айтемы, например, если текст найден в описании коллекции или комментарии, что должно быть возможно, то выводится ссылка на айтем). Отображение для результатов поиска — айтемы.

У каждого пользователя есть его личная страница, на которой он управляет списком своих коллекий (можно добавить, удалить или отредактировать) и из которой можно перейти на страницу коллекции (там таблица с фильтраций и сортировками, возможность создать/удалить/редактировать айтем).

Каждая коллекция состоит из: название, краткое описание с поддержкой форматирования markdown, "тема" (из фиксированного набора, например, "Alcohol", "Books" и проч.), опционального изображения (хранится в облаке, загружается drag-n-drop-ом). Помимо этого, у коллекции есть возможность указать поля, которые будут у каждого айтема в ней (есть фиксированные поля - id, название и тэги, можно "добавить-включить" некоторые из следующих - три числовых поля, три однострочных поля, три текстовых поля, три даты, три булевских чек-бокса). Например, можно указать, что в моей коллекции книг у каждого айтема есть (помимо id, названия и тэгов) строковое поле "Автор", текстовое поле "Комментарий", поле-дата "Год издания". Текстовое поле — поле с форматирование markdown. Поля характеризуются названием. Поля отображаются в списке айтемов - в списке необходима поддержка переключающихся сортировок и фильтров. Пояснение: у всех айтемов в базе сразу есть все возможные поля и есть еще одно дополнительное поле (например, битовая маска), которое задаёт, какие поля отображаются.

Каждый айтем имеет тэги (вводится несколько тэгов, необходимо автодополнение - когда пользователь начинает вводить тэг, выпадает список с вариантами слов, которые уже вводились ранее на сайте)

На главной странице отображаются: последние добавленные айтемы, коллекции с самым большим числом айтемов, облако тэгов (при клике результат - список ссылок на айтемы, аналогично результатам поиска, по сути это может быть одна вьюшка).

При открытии айтема в режиме чтения автором или просто другими пользователями, в конце отображаются комментарии. Комментарии линейные, нельзя комментировать комментарий, новый добавляется только "в хвост". Необходимо реализовать автоматическую подгрузку комментариев - если у меня открыта страница с комментариями и кто-то другой добавляет новый, он у меня автомагически появляется (возможна задержка в 2-5 секунд).

У айтема должны быть лайки (не более одного от одного пользователя на айтем).

Сайт должен поддерживать два языка: русский и английский (пользователь выбирает и выбор сохраняется). Сайт должен поддерживать два оформления (темы): светлое и темное (пользователь выбирает и выбор сохраняется).

Обязательно: Bootstrap (или любой другой CSS-фреймворк), поддержка разных разрешений (в том числе телефон), ORM для доступа к данным (Hibernate, EF, что угодно), движок для полнотекстового поиска (или средствами базы, или отдельный движок — НЕ ПОЛНОЕ СКАНИРОВАНИЕ селектами).

Требования со звездочкой (лишь опционально, на 10/10, после реализации остальных требований):
* Добавить возможность полей в айтемах, которые являются "выбором из списка", с возможностью задания значений.

* Добавить возможность поддержки произвольного числа кастомных полей, а не только по три одного из пяти видов.

* Добавить возможность экспорта коллекции в CSV-файл.

*** Добавить механизм продажи - виртуальные кошельки, пользователей, пополнение кошельков, цены, выставление на продажу, покупка рекламы на главной странице.

ВАЖНО: не копируйте из кодо-помоек всякую фигню. Лучше сделайте меньше, но сами разбиритесь, чтобы уметь ответить как на лету что-то поменять/добавить. Кураторы принимают огромное количество однотипных проектов и видели, вероятно, большинство выложенной фигни на тему.
