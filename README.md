# RS School 2020Q1 markup task „Singolo“

| Final | [Task „Singolo. Part 1“](https://github.com/rolling-scopes-school/tasks/blob/master/tasks/markups/level-2/singolo/part-1/singolo-1-ru.md) | [Task „Singolo. Part 2“](https://github.com/rolling-scopes-school/tasks/blob/master/tasks/markups/level-2/singolo/part-1/singolo-2-ru.md) | [Task „Singolo. Part 3“](https://github.com/rolling-scopes-school/tasks/blob/master/tasks/markups/level-2/singolo/part-1/singolo-3-ru.md) |
| - | - | - | - |
| **[Full site deploy](https://hallovarvara.github.io/singolo/)** | [Deploy of part 1](https://hallovarvara.github.io/singolo/singolo1.html) | [Deploy of part 2](https://hallovarvara.github.io/singolo/singolo2.html) | [Deploy of part 3](https://hallovarvara.github.io/singolo/singolo3.html) |


## Общие требования

Ключевым моментом является полное соответствие макету (**[singolo.psd](https://github.com/rolling-scopes-school/tasks/blob/master/tasks/markups/level-2/singolo/singolo.psd)**, **[singolo.jpg](https://github.com/rolling-scopes-school/tasks/blob/master/tasks/markups/level-2/singolo/singolo-full.jpg)**). Это достигается совпадением двух изображений при наложении слоя с картинкой поверх готового решения с помощью браузерного расширения [Pixel Perfect (Chrome)](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en). Уделите внимание следующим важным и распространенным моментам:
- [x] Основные блоки должны быть идеально расположены на заданной ширине экрана (1020px).
- [x] Изображения, логотипы (если они есть) должны быть идеально расположены в рамках логического контейнера.
- [x] Иконки должны сохранять идеальное расстояние до соответствующего им текста.
- [x] Если использован правильный шрифт, проверьте высоту текста — он должен соответствовать исходнику. Ширина может варьироваться. Но общепринятой практикой является добавление свойства межбуквенного интервала (letter-spacing) тексту заголовков, девиза (motto) или цитат.
- [x] Если в строке несколько объектов визуально одинаковой ширины, то ширина содержащих их блоков должна быть одинаковой. Разница в несколько пикселей не имеет значения, важно совпадение размеров.
- [x] Если нужно добавить тень, можно использовать один из подходов:
  - Объединить слои в графическом редакторе и использовать изображение в качестве фонового.
  - Добавить тень как box-shadow и подобрать такие значения для этого свойства, при которых она будет максимально похожа на тень в макете.

#### Кроссбраузерность
- [x] Поддержка браузеров: **Google Chrome, Mozilla Firefox, Microsoft Edge (Windows) or Safari (MacOS)**. В первую очередь мы разрабатываем **для Google Chrome** и используем **Pixel Perfect** для проверки соответствия. Затем проверяем, не «рушат» ли *Mozilla Firefox*, *Microsoft Edge* или *Safari* наши стили.

#### Репозиторий
- [x] Репозиторий с решением публичный.
- [x] index.html и style.css (изменены не позже 08.03.2020 23:59).
- [x] singolo1.html и singolo1.css (изменены не позже 23.02.2020 23:59).
- [x] singolo2.html и singolo2.css (изменены не позже 01.03.2020 23:59).
- [x] singolo3.html и singolo3.css (изменены не позже 08.03.2020 23:59).
- [x] Изображения, шрифты и другие вспомогательные файлы лежат в папке **assets**.

## Технические требования

«Интерактивный» означает, что у элемента появляется визуальный эффект или анимация при каких-либо действиях пользователя, например, при наведении курсора или нажатии. Обычно такой эффект реализуют при помощи следующих свойств:
- `pointer: cursor`,
- `background`,
- `text-decoration: underline`,
- `color`.

#### 1. **Header** (`<header>` содержит только логотип и панель навигации):
- [x] Интерактивная панель навигации.
- [x] Логотип содержит 2 разных текстовых элемента, белый и красный.
- [x] На странице обязательно должен присутствовать один элемент `<h1>`. Расположите его на свое усмотрение.
- [x] Внизу есть небольшая линия другого цвета, будьте внимательны.

#### 2. Блок **Slider**
- [x] Стрелки должны быть интерактивными. При нажатии ничего происходить не должно (слайды могут не листаться).

Картинки в слайдере можно реализовать тремя способами. Выберите один из них:
1. Создайте изображения наложением нескольких слоев, используя `z-index`. Элементы должны быть в `position: absolute`. Изображения телефонов так же могут быть сделаны средствами CSS.
- [x] 2. Создайте полные изображения вертикального и горизонтального телефонов с помощью графического редактора (фотошоп или аналог), объединив все слои.
3. Объедините оба предыдущих варианта и создайте изображения трёх отдельных элементов: тень, контейнер телефона, внутреннее изображение на экране. В таком случае одно и то же изображение телефона и тени можно использовать для обеих картинок, просто повернув их на 90 градусов и 180 градусов. Тень можно сделать с помощью CSS.

- [x] Внизу есть небольшая линия другого цвета, будьте внимательны.

#### 3\. Блок **Our Services**
- [x] Трёхколоночный макет снизу. Лучше использовать [flexbox](https://habr.com/ru/post/467049/) или [grid](https://tuhub.ru/posts/css-grid-complete-guide). Float использовать можно. `<table>` - нельзя!
- [x] Изображения можно экспортировать как иконки вместе с кругами. Другой вариант - экспортировать только сами иконки, а круги добавить свойством `border-radius`.
- [x] Если в текстовой ячейке больше текста, чем она вмещает, и текст начинает выходить за границы элемента, то выступающая часть должна быть скрыта.
- [x] Внизу есть небольшая линия другого цвета, будьте внимательны.

#### 1. Блок **Portfolio**
- [x] Интерактивные кнопки навигации.
- [x] Четырехколоночный макет с изображениями.
- [x] Если в сетку добавить больше элементов с изображениями (например, 15) - то следющие за 12-м не должны показываться (т.е. 13, 14, 15 не видны).
- [x] Внизу есть небольшая линия другого цвета, будьте внимательны.

#### 2. Блок **About Us**
- [x] Трёхколоночный макет снизу.
- [x] Имя, если оно очень большое, все равно должно занимать ровно одну строку.
- [x] Интерактивные социальные иконки.
- [x] Внизу есть небольшая линия другого цвета, будьте внимательны.

#### 1. Блок **Get a Quote**
- [x] Все элементы ввода - часть формы
- [x] Форма должна быть интерактивной, а именно иметь возможность отправлять запрос. Добавьте кнопку 'Submit' куда-либо на ваше усмотрение. Кнопка должна находиться внутри формы.
- [x] 2 поля помечены как (Required). Это значит, что должна быть хотя бы базовая валидация на text и на email.
- [x] На всех полях должен быть placeholder.
- [x] Указатель на номер телефона - должен быть ссылкой типа tel.
- [x] Указатель на email - должен быть ссылкой типа mail.
- [x] Внизу есть небольшая линия другого цвета, будьте внимательны.

#### 2. **Footer** (`<footer>` - это серая панель снизу):
- [x] Интерактивные иконки

## Критерии оценки

Если задание выполнено полностью и проверяющий не обнаружил никаких дефектов, вы получаете **100 баллов**. Это касается разметки и использования HTML и CSS.

1. За сдачу не вовремя вы можете потерять **до 40 баллов** от общего результата!
2. Несоблюдение стандартов кода или требований синтаксиса может привести к потере **до 20 баллов**.
3. Несовпадение с PSD-шаблоном (за исключением нюансов со шрифтами) может привести к потере **до 40 баллов**.
4. Невыполнение какого-либо из технических требований может привести к потере **от 3 до 10 баллов**.