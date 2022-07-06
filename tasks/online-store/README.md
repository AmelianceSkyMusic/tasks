# Online-Store - Интернет магазин

Вам необходимо создать интернет-магазин произвольной тематики(например: техника, автозапчасти, спорт товары и т.д.), где товары будут иметь следующий функционал: фильтрация, сортировка, поиск, добавление в корзину. Подобную функциональность имеют каталоги интернет-магазинов - [Пример](https://react-course-comfy-sloth-store.netlify.app/products)

## Функционал приложения
1. Главная страница содержит все товары магазина а также фильтры, строку поиска, поле для сортировки. Выполняются [требования к вёрстке](#verstka) +10
2. Карточка товара содержит его изображение, название, количество данного товара на складе, год выхода на рынок, цвет, производитель и т.д., находится ли товар в корзине +10  
Карточки товаров добавляются динамически средствами JavaScript (на кросс-чеке этот пункт не проверяется)
3. Добавление товаров в корзину +20
   - кликая по карточке с товаром или по кнопке на нем, товар можно добавлять в корзину или удалять. Карточки добавленных в корзину товаров внешне отличаются от остальных +10
   - на странице отображается количество добавленных в корзину товаров. При попытке добавить в корзину больше 20 товаров, выводится всплывающее уведомление с текстом "Извините, все слоты заполнены" +10
4. Сортировка +20  
   Сортируются только те товары, которые в данный момент отображаются на странице
   - сортировка товаров по названию в возрастающем и убывающем порядке +10
   - сортировка товаров по году их выхода на рынок в возрастающем и убывающем порядке +10
5. Фильтры в указанном диапазоне `от и до` +30
   - фильтры по количеству +10
   - фильтры по году выпуска на рынок +10
   - для фильтрации в указанном диапазоне используется range slider с двумя ползунками. При перемещении ползунков отображается их текущее значение, разный цвет слайдера до и после ползунка +10       
   Range slider можно создать на основе `input[type=range]` - [пример](https://ru.stackoverflow.com/questions/1025336/Два-бегунка-у-input-с-типом-range) или использовать для этой цели библиотеку [noUiSlider](https://refreshless.com/nouislider/), или другую на ваш выбор
6. Фильтры по значению +30  
   Выбранные фильтры выделяются стилем.   
   - фильтры по производителю +5
   - фильтры по цвету +5
   - фильтры по размеру (в случае с Демо - по количеству камер) +5
   - можно отобразить только популярные товары +5
   - можно отфильтровать товары по нескольким фильтрам одного типа +10  
   Если для выбранной Вами тематики интернет-магазина указанные выше фильтры неактуальны, Вы можете добавить свои фильтры в зависмости от категории товара. Для нескольких фильтров одного типа отображаются товары, которые соответствуют хоть одному выбранному фильтру. Например, можно отобразить Samsung и Apple; или белые, синие и красные товары; или товары с 2 и 3 камерами.
7. Можно отфильтровать товары по нескольким фильтрам разного типа +20  
   Для нескольких фильтров разного типа отображаются только те товары, которые соответствуют всем выбранным фильтрам.  
   Например, можно отобразить только красные товары. Или популярные белые и красные товары впоступившие на рынок в 2010-2020 годах.  
   Если товаров, соответствующих всем выбранным фильтрам нет, на странице выводится уведомление в человекочитаемом формате, например, "Извините, совпадений не обнаружено"
8. Сброс фильтров +20  
   - есть кнопка `reset` для сброса фильтров +10  
   Кнопка `reset` сбрасывает только фильтры, не влияя на порядок сортировки или товары, добавленные в избранное.  
   После использования кнопки `reset` фильтры остаются работоспособными
   - при сбросе фильтров кнопкой `reset`, ползунки range slider сдвигаются к краям, значения ползунков возвращаются к первоначальным, range slider закрашивается одним цветом +10
9. Сохранение настроек в local storage +30
   - выбранные пользователем фильтры, порядок сортировки, добавленные в избранное товары сохраняются при перезагрузке страницы. Есть кнопка сброса настроек, которая очищает local storage +10
10. Поиск +30
   - при открытии приложения курсор находится в поле поиска +2
   - автозаполнение поля поиска отключено (нет выпадающего списка с предыдущими запросами) +2
   - есть placeholder +2
   - в поле поиска есть крестик, позволяющий очистить поле поиска +2
   - если нет совпадения последовательности букв в поисковом запросе с названием товара, выводится уведомление в человекочитаемом формате, например "Извините, совпадений не обнаружено" +2 
   - при вводе поискового запроса на странице остаются только те товары, в которых есть указанные в поиске буквы в указанном порядке. При этом не обязательно, чтобы буквы были в начале слова. Регистр символов при поиске не учитывается +10  
   Поиск ведётся только среди товаров, которые в данный момент отображаются на странице.
   - если очистить поле поиска, на странице отображаются товары, соответствующие всем выбранным фильтрам и настройкам сортировки +10




[Демо](https://rs-online-store.netlify.app/)  

Вы можете редактировать исходные данные или полностью изменить их с целью улучшения качества созданного приложения

## Ключевые навыки:
- TypeScript
- Modules in JavaScript
- Webpack
- сортировка данных
- фильтрация данных
- реализация поиска

## Технические требования
- для написания кода приложения используйте TypeScript
- разбейте код на модули
- для сборки кода используйте `webpack`
- используйте `eslint` настроеный для проверки TypeScript
- работа приложения проверяется в браузере Google Chrome последней версии
- можно использовать [bootstrap](https://getbootstrap.com/), [material design](https://material.io/), css-фреймворки, html и css препроцессоры
- не разрешается использовать jQuery, другие js-библиотеки и фреймворки, за исключением следующих случаев:
  - можно использовать js-библиотеку для создания ползунка с двумя значениями для сортировки в указанном диапазоне, например, [noUiSlider](https://refreshless.com/nouislider/), или другую на ваш выбор
  - можно использовать js-библиотеку для реализации дополнительного функционала - плавного перемещения карточек в ходе сортировки, фильтрации, поиска, например, [Shuffle](https://codepen.io/Vestride/pen/ZVWmMX), или другую на ваш выбор
  - можно использовать jQuery только для подключения используемых js-библиотек, если она необходима для их работы
  - запрещается использование Angular/React/Vue и других фреймворков

## <a id="verstka" />Требования к вёрстке
- внешний вид приложения соответствует предложенному образцу или является его улучшенной версией
- вёрстка адаптирована для планшета и десктопа. Корректность отображения приложения и отсутствие горизонтальной полосы прокрутки проверяется при ширине страницы от 1920рх до 768рх
- интерактивность элементов, с которыми пользователи могут взаимодействовать, изменение внешнего вида самого элемента и состояния курсора при наведении, использование разных стилей для активного и неактивного состояния элемента, плавные анимации
- в футере приложения есть ссылка на гитхаб автора, год создания приложения, [логотип курса](https://rs.school/images/rs_school_js.svg) со [ссылкой на курс](https://rs.school/js/)

## Требования к репозиторию
- задание выполняется в приватном репозитории школы. [Как работать с приватным репозиторием школы](https://docs.rs.school/#/private-repository)
- если у вас не создаётся приватный репозиторий школы, задание можно выполнять в личном приватном репозитории
- от ветки `main` создайте ветку с названием таска в ней создайте папку с названием таска, в ней разместите файлы проекта
- для деплоя используйте `gh-pages` [Как сделать деплой задания из приватного репозитория школы](https://docs.rs.school/#/private-repository?id=Как-сделать-деплой-задания-из-приватного-репозитория-школы)
- если не можете для деплоя использовать `gh-pages`, используйте https://app.netlify.com/drop. Название страницы дайте по схеме: имя гитхаб аккаунта - название таска

## Требования к коммитам
- История коммитов должна отображать процесс разработки приложения.
- [Названия коммитов дайте согласно гайдлайну](https://docs.rs.school/#/git-convention)

## Требования к Pull Request
- Название Pull Request дайте по названию задания
- [Описание Pull Request дайте по схеме](https://docs.rs.school/#/pull-request-review-process?id=Требования-к-pull-request-pr)  
**Мержить Pull Request из ветки разработки в ветку `main` не нужно**.

## Как сабмитить задание
Засабмитить задание необходимо как можно раньше, как только в rs app появится такая возможность. Для этого зайдите в rs app https://app.rs.school/, выберите пункт Cross-Check: Submit, в выпадающем списке выберите название таска, в поле Solution URL добавьте ссылку на задеплоенную версию вашего приложения, нажмите кнопку Submit.   
После сабмита задания его можно продолжать выполнять до самого дедлайна.

## Cross-check
- инструкция по проведению cross-check: https://docs.rs.school/#/cross-check-flow
- ссылки на лучшие работы добавьте, пожалуйста, в эту форму https://docs.google.com/forms/d/e/1FAIpQLSdALk64QGdQjeHWrgYWn2IcteB8lwY_rufDUi13-ucneo7hLw/viewform?usp=pp_url

## Материалы
- [Официальная документация TypeScript](https://www.typescriptlang.org/)
- [Руководство по TypeScript](https://metanit.com/web/typescript/)
- [Практическое руководство по TypeScript для разработчиков](https://habr.com/ru/company/macloud/blog/557996/)
- [TypeScript. Полный курс](https://youtu.be/5QnZ9AyDW6c)
- [TypeScript - Быстрый Курс за 70 минут](https://youtu.be/nyIpDs2DJ_c)

## Вебинары RS School
- [JS/FE 2021Q3 Typescript Basics](https://youtu.be/BRTT8ZJeoS4)
- [Typescript 26.05.21 (part 1)](https://youtu.be/I_aTbZcH8Do)
- [Typescript 28.05.21 (part 2)](https://youtu.be/CegrbRXGw20)


## Критерии оценки cross-check
**Максимальный балл за задание +200**

Для удобства проверки выведите в консоль браузера самооценку своего проекта по пунктам с указанием баллов за каждый выполненный вами пункт.

Баллы за отдельные пункты требований указаны в разделе ["Функционал приложения"](#функционал-приложения)  
Если после пункта требований не указаны баллы, данный пункт является пояснением и условием получения баллов за предыдущий пункт с баллами.  
Баллы за пункты требований связанные с сортировкой, фильтрацией, поиском, добавлением в избранное выставляются полностью только в случае согласованной работы всего функционала.  
Фильтрация и поиск не должны ломать сортировку, кнопка `reset` сбрасывает только фильтры, но не порядок сортировки и т.д. 

Разница между максимальной оценкой за приложение (200 баллов) и максимально возможным количеством баллов за выполнение всех пунктов требований (220 баллов) позволит сгладить возможные ошибки проверяющих в ходе кросс-чека, неточности в описании задания, разное понимание требований задания проверяющим и проверяемым.

## Проверка задания ментором
**Максимальный балл за задание +200**

1. Репозиторий +20
   - pull request выполнен в соответствии с [требованиями](https://docs.rs.school/#/pull-request-review-process?id=Требования-к-pull-request-pr) +10
   - ведётся история коммитов, названия коммитов даются согласно [гайдлайну](https://docs.rs.school/#/git-convention) +10
2. Качество кода +160
   - приложение написано на TypeScript. 
      - используется Everyday Types +10
      - используются Generics +10
      - использование Object Types +10
      - использование Classes +10
      - использование Function +10
      - нигде не используется тип Any +10
      - ESLinter настроен на TypeScript (используется плагин `typescript-eslint/recommended`) и отсутствуют ошибки +10
      - В конфигурационном файле TypeScript стоят флаги `"noImplicitAny": true` и `"strict": true` + 20
      - webpack настроен и работает с TypeScript +10
   - код разбит на модули +10
   - карточки товаров добавляются динамически средствами JavaScript +10
   - у ментора нет замечаний к качеству кода, либо все замечания ментора исправлены +30
3. Тесты в приложении +20
   - реализованы юнит-тесты, использующие различные методы jest – 2 балла за каждую покрытую функию/метод, но не более 20 баллов (процент покрытия каждой функции/метода не учитывается)


## Штрафы

1. Используется тип Any -20
2. Код не полностью покрыт типами -20
3. В конфигурационном файле TypeScript не стоят обязательные флаги `"noImplicitAny": true` и `"strict": true` -20
4. В конфигурационном файле ESLint не включено правило `no-explicit-any` -10