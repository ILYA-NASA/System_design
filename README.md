## Архитектура программного обеспечения 
совокупность важнейших решений об организации программной системы. 

### Архитектура включает:
* выбор структурных элементов и их интерфейсов, с помощью которых составлена система, а также их поведения в рамках сотрудничества структурных элементов;
* соединение выбранных элементов структуры и поведения во всё более крупные системы;
* архитектурный стиль, который направляет всю организацию — все элементы, их интерфейсы, их сотрудничество и их соединение.

### [Пример проектирования ПО](https://github.com/ILYA-NASA/System_design/tree/main/Software_architecture/ModelElements)

------------------------------------------

## Парадигмы программирования
совокупность идей и понятий, определяющих стиль написания компьютерных программ (подход к программированию).   
Это способ концептуализации, определяющий организацию вычислений и структурирование работы, выполняемой компьютером.

![Парадигмы](https://user-images.githubusercontent.com/99810114/213172963-478fbf66-4953-4875-99fa-86372459f132.jpg)

------------------------------------------

### [От процедурного программирования к ООП](https://github.com/ILYA-NASA/OOP/tree/main/Object-oriented)

## Объектно-ориентированное программирование 
это методология
программирования, основанная на представлении программы в виде
совокупности объектов, каждый из которых служит экземпляром
определённого класса, а классы образуют иерархию наследования.

### Объект 
это нечто, имеющее чётко определённые границы. Однако этого
недостаточно, чтобы отделить один объект от другого или дать оценку
качества абстракции. Объект обладает состоянием, поведением и
идентичностью. Структура и поведение похожих объектов определяет общий
для них класс.

### Класс  
это множество объектов, обладающих общей структурой, поведением
и семантикой. Класс представляет лишь абстракцию существенных свойств
объекта.

### Экземпляр класса 
это описание конкретного объекта в памяти.
Состояние объекта характеризуется перечнем (обычно статическим) всех
свойств этого объекта и текущими (обычно динамическими) значениями
каждого из этих свойств. Например, торговый автомат имеет свойство:
способность принимать монеты, этому свойству соответствует динамическое
значение — количество принятых монет.   

В объектно-ориентированном подходе основная категория объектной модели
— класс — объединяет в себе на элементарном уровне как данные, так и
операции, которые над ними выполняются (методы). Именно с этой точки
зрения, изменения, связанные с переходом от структурного к
объектно-ориентированному подходу, считаются наиболее заметными.
Принципы ООП

### Объектно-ориентированное программирование обладает рядом принципов:

1. **Наследование** — это наличие у разных классов, образующих иерархию, общих
атрибутов и операций. Суперкласс задаёт наиболее общую информацию,
которую затем уточняют его подклассы. Каждый подкласс соединяет в себе,
наследует, все черты его суперкласса, к которым добавляет собственные
уникальные черты. Подклассам необязательно воспроизводить все черты
суперкласса.
2. **Инкапсуляция**, или сокрытие информации, состоит в отделении внешних
аспектов объектов, доступных другим объектам, от деталей внутренней
реализации, которые от других объектов скрываются. Она (инкапсуляция)
исключает возникновение взаимозависимостей участков программы, из-за
которых небольшие изменения приводят к значительным непредвиденным
последствиям.
3. **Полиморфизм** означает, что одна и та же операция может подразумевать
разное поведение в разных классах.
4. **Абстракция** означает сосредоточение на важнейших аспектах приложения и
игнорирование остальных. Сначала принимается решение, что представляет
собой объект и что он делает, а уже затем подбирается способ его реализации.

### [Прогресс создания консольной игры в стиле Turn-Based Strategy ](https://github.com/ILYA-NASA/OOP/tree/main/ChroniclesOfGame)

--------------------------------------------------

## SOLID 
акроним пяти важных принципов проектирования при выполнении ООП (объектно-ориентированного программирования).   
Они связаны с проектированием и сопровождением программных систем.

### [Практические примеры принципов SOLID](https://github.com/ILYA-NASA/System_design/tree/main/SOLID/Lecture_06) 

-------------------------------------------

## Компоненты 
это единицы развёртывания. Они представляют наименьшие
сущности, развёртываемые в составе системы.

Компонент представляет собой структурную единицу программной системы,
обладающую чётко определённым интерфейсом, который полностью описывает
её зависимости от окружения. Такой компонент может быть независимо
поставлен или не поставлен, добавлен в состав некоторой системы или удалён из
неё, в том числе может включаться в системы других поставщиков.

![Компоненты](https://user-images.githubusercontent.com/99810114/213170256-9a8a91e4-aa90-4cb5-9e9c-719f80c2316f.jpg)

### [Проект ПО из компонентов](https://github.com/ILYA-NASA/System_design/tree/main/Software_architecture/UML)

-------------------------------------------------

## Слоёная архитектура
### Слои и срезы 
это следующий уровень абстракции после компонентов.
1. Горизонтальные слои связаны с назначением слоя в коде системы.
Например, есть слой базы данных и бизнес-логики.

2. Вертикальные срезы связаны с тем, что делает система, с её функциями
(сценарии использования). Сценарии использования меняются по разным
причинам, друг от друга независимым. Поэтому важно защищать их друг от
друга.

Систему всегда можно разделить на горизонтальные уровни:

● пользовательский интерфейс;

● бизнес-правила, характерные для приложения;

● бизнес-правила, не зависящие от приложения;

● слой базы данных.

![Слои 2](https://user-images.githubusercontent.com/99810114/213171973-c51dd0ea-4c69-4fe4-b562-9c9665fc2593.jpg)

**Слои** обеспечивают логический уровень разделения в приложении. Если
логика приложения при этом физически распределяется между несколькими
серверами или процессами, такие раздельные физические целевые объекты
развёртывания называются **уровнями**.   

### Пользовательский интерфейс 
интерфейс, обеспечивающий передачу
информации между пользователем-человеком и программно-аппаратными
компонентами компьютерной системы.
### Бизнес-правила 
совокупность правил, принципов, зависимостей
поведения объектов предметной области. Последнее — область человеческой
деятельности, которую поддерживает система.
### База данных 
это организованная структура, предназначенная для
хранения, изменения и обработки взаимосвязанной информации,
преимущественно больших объёмов.

### [Слои и срезы на UML](https://github.com/ILYA-NASA/System_design/tree/main/Software_architecture/UML)

---------------------------------------------------

## Чистая архитектура
это способ разделения ответственностей и частей
функциональности по степени их близости к предметной области приложения.

![CleanArch](https://user-images.githubusercontent.com/99810114/213432306-f008aaec-733f-4cb4-9cb6-05de6f94ee5b.jpg)

Принципы чистой архитектуры:
1. Приложение строится вокруг независимой от других слоёв
объектной модели.
2. Внутренние слои определяют интерфейсы, внешние слои содержат
реализации интерфейсов.
3. Направление зависимостей — от внешних слоёв ко внутренним.
4. При пересечении границ слоя данные должны преобразовываться.

### [Драфт системы, написанный с применением принципов чистой архитектуры](https://github.com/ILYA-NASA/System_design/tree/main/Software_architecture/CleanArchitecture)

---------------------------------------------

## Архитектуры веб-приложений

### MPA (Multi Page Application)
это веб-приложение, состоящее из большого количества страниц,
которые полностью обновляются каждый раз, когда на них изменяются данные.

ДОСТОИНСТВА ПОДХОДА MPA | НЕДОСТАТКИ MPA
--|---
Даёт пользователям понятную карту для навигации по приложению, обеспечивает надёжность и многоуровневость переходов в меню | Не позволяет использовать один и тот же бэкенд с мобильными приложениями
Оптимизирует управление поисковой оптимизацией (SEO) | Тесно увязывает разработку фронтенда и бэкенда
Позволяет добиться лучшего ранжирования в поисковиках за счёт оптимизации под одно ключевое слово на странице | Усложняет и замедляет разработку из-за необходимости использовать фреймворки как на стороне клиента, так и на стороне сервера
Позволяет включать столько информации о продукте, сколько необходимо, без ограничений по количеству страниц | Усложняет поддержание безопасности: требует защищать каждую отдельную страницу
Ускоряет начальную загрузку страницы | 
Даёт много аналитики и сведений о работе сайта | 
Экономически эффективен | 

![MPA SPA](https://user-images.githubusercontent.com/99810114/214044333-bc3b116e-6390-458b-9cd6-5e51bcbce606.jpg)

### SPA (Single Page Applications)
Под одностраничным понимают веб-приложение, работающее в
рамках одного HTML-документа.
Переход между разделами внутри SPA выполняется без перезагрузки всей
страницы в браузере.

ДОСТОИНСТВА SPA | НЕДОСТАТКИ SPA
--|---
Скорость работы и отзывчивость приложения, быстрая загрузка | Плохая SEO-оптимизация: только один URL
Возможность переиспользовать 20%–30% кода, превратив SPA в полноценное мобильное приложение | Сравнительно долгая начальная загрузка
Улучшенный пользовательский опыт: после первой загрузки всё работает быстро | Недружественная навигация и отсутствие кнопки «Назад»
Возможность автономной работы | Угрозы безопасности из-за межсайтового скриптинга
Разделение ответственности между front-end и back-end: внешний интерфейс взаимодействует с логикой, а внутренний отвечает за обработку данных | 
Возможность раздельно разрабатывать и тестировать front-end и back-end | 

### [Проект одностраничного веб-приложения](https://github.com/ILYA-NASA/System_design/tree/main/Software_architecture/SPA)

-----------------------------------------------

## Архитектура прикладных приложений

### Прикладная программа (приложение) 
программа, ориентированная
на решение конкретных задач и рассчитанная
на взаимодействие с пользователем.

### Паттерны семейства MV* (Model-View) 

![MV](https://user-images.githubusercontent.com/99810114/215264134-3658d082-0676-4e75-ace4-31a19f677daa.jpg)

Разработка на основе паттернов **MV*** позволяет разделить код на
независимые модули, тем самым упростить поддержку готового продукта и
ускорить разработку нового функционала.

### Model (Модель) 
часть программы, содержащая описание
функциональной и бизнес-логики приложения. Модель должна быть полностью
независимой от остальных частей продукта. Модельный слой ничего не должен
знать об элементах графического интерфейса и того, каким образом он будет
отображаться.

### View (Представление) 
отвечает за отображение данных, полученных от
модели, но не может напрямую влиять на модель. Предполагается, что
представление обладает доступом к данным «только на чтение».

### MVC (Model-View-Controller) 

![MVC](https://user-images.githubusercontent.com/99810114/215266995-5c6b1de7-c157-4b7e-826c-39aef9121260.jpg)

### Controller
отвечает за связь между моделью и
представлением. Код контроллера определяет, как приложение реагирует на
действия пользователя. Это связывающий, контролирующий слой.


### MVP (Model-View-Presenter)

![MVP](https://user-images.githubusercontent.com/99810114/215267005-9fda8561-055a-4314-bffb-6aeb67b9ce1e.jpg)

был разработан для облегчения автоматического модульного тестирования и
улучшения разделения ответственности, то есть отделения логики от
отображения.

### Presenter 
реализует взаимодействие между моделью и
представлением и содержит в себе всю логику представления
данных о предметной области; при необходимости получает данные
из хранилища и преобразует для отображения во View.

### [Проект приложения, разработанного на основе паттерна MVP](https://github.com/ILYA-NASA/System_design/tree/main/Software_architecture/MVP)

### MVVM (Model-View-ViewModel)

![MVVM](https://user-images.githubusercontent.com/99810114/215267014-2073c7fb-ba06-423c-befc-bacaffb26c3f.jpg)

### ViewModel
связывает модель и представление через механизм привязки
данных. Если в модели изменяются значения свойств,
автоматически идет изменение отображаемых данных в
представлении, хотя напрямую модель и представление не связаны.

------------------------------------------------------------
