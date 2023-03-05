# Введение в алгоритмы

- [Агроном](./Task%20A.cpp)
- [Профессор Хаос](./Task%20B.cpp)
- [Зоопарк Глеба](./Task%20C.cpp)
- [Конфигурационный файл](./Task%20D.cpp)

---

## Агроном
Городской школьник Лёша поехал на лето в деревню и занялся выращиванием цветов. Он посадил n цветков вдоль одной длинной прямой грядки, и они успешно выросли. Лёша посадил множество различных видов цветков, i-й от начала грядки цветок имеет вид ai, где ai "— целое число, номер соответствующего вида в «Каталоге юного агронома».

Теперь Лёша хочет сделать фотографию выращенных им цветов и выложить ее в раздел «мои грядки» в социальной сети для агрономов «ВКомпосте». На фотографии будет виден отрезок из одного или нескольких высаженных подряд цветков.

Однако он заметил, что фотография смотрится не очень интересно, если на ней много одинаковых цветков подряд. Лёша решил, что если на фотографии будут видны три цветка одного вида, высаженные подряд, то его друзья — специалисты по эстетике цветочных фотографий — поставят мало лайков.

Помогите ему выбрать для фотографирования как можно более длинный участок своей грядки, на котором нет трех цветков одного вида подряд.

### Формат ввода
В первой строке содержится целое число n (1 ≤ n ≤ 200 000) — количество цветов на грядке.

Во второй строке содержится n целых чисел ai (1 ≤ ai ≤ 10^9), обозначающих вид очередного цветка. Одинаковые цветки обозначаются одинаковыми числами, разные — разными.

### Формат вывода
Выведите номер первого и последнего цветка на самом длинном искомом участке. Цветки нумерются от 1 до n.

Если самых длинных участков несколько, выведите участок, который начинается раньше.

### Пример
| **Ввод**     | **Вывод**  |
| :----------- | :--------- |
| 6            | 3 6        |
| 5 6 6 6 23 9 |            |

## Профессор Хаос
В секретной лаборатории профессора Хаоса проходит эксперимент по выращиванию особо опасных бактерий. В начале первого дня эксперимента у Хаоса имеется a особо опасных бактерий.

Каждый день эксперимента устроен следующим образом. Рано утром профессор достает из контейнера все свои бактерии и помещает их в инкубатор, где бактерии начинают делиться. Вместо каждой бактерии образуется b новых бактерий.

После извлечения бактерий из инкубатора c из них используются для проведения различных опытов и затем уничтожаются. Если после извлечения из инкубатора имеется менее c бактерий, для проведения опытов используются все имеющиеся бактерии, и эксперимент заканчивается.

Оставшиеся бактерии в конце дня необходимо поместить в контейнер и продолжить использовать в эксперименте. Однако в контейнер можно поместить не более d бактерий, поэтому если число оставшихся бактерий больше d, то в контейнер помещаются d бактерий, а остальные уничтожаются.

Теперь профессор Хаос хочет выяснить, сколько особо опасных бактерий будет у него в контейнере после k-го дня эксперимента. Помогите ему найти ответ на этот вопрос.

### Формат ввода
В единственной строке входного файла содержится пять целых чисел a, b, c, d и k (1 ≤ a, b ≤ 1000, 0 ≤ c ≤ 1000, 1 ≤ d ≤ 1000, a ≤ d, 1 ≤ k ≤ 10^18).

### Формат вывода
Выведите одно число — количество бактерий у Хаоса к концу k-го дня. Если эксперимент завершится в k-й день или ранее, выведите число 0.

### Пример 1
| **Ввод**     | **Вывод**  |
| :----------- | :--------- |
| 1 3 1 5 2    | 5          |

### Пример 2
| **Ввод**     | **Вывод**  |
| :----------- | :--------- |
| 1 2 0 4 3    | 4          |

### Пример 3
| **Ввод**     | **Вывод**  |
| :----------- | :--------- |
| 1 2 3 5 2    | 0          |


## Зоопарк Глеба
Недавно Глеб открыл зоопарк. Он решил построить его в форме круга и, естественно, обнёс забором. Глеб взял вас туда начальником охраны. Казалось бы все началось так хорошо, но именно в вашу первую смену все животные разбежались. В зоопарке n животных различных видов, также под каждый из видов есть свои ловушки. К сожалению некоторые животные враждуют с друг другом в природе (они обозначены разными буквами), а зоопарк обнесён забором и имеет форму круга. С помощью камер, удалось выяснить, где находятся все животные. Умная система поддержки жизнедеятельности зоопарка уже просканировала зоопарк и вывела id всех животных и ловушек в том порядке, в котором они видны из центра зоопарка. Получилось так, что все животные и все ловушки находятся на краю зоопарка. Вы хотите понять, могут ли животные прийти в свою ловушку так, чтобы их путь не пересекался с другими. Если да, также предъявите какую-нибудь из схем поимки животных.

### Формат ввода
На вход подается строчка из 2 ⋅ n символов латинского алфавита, где маленькая буква - животное, а большая - ловушка. Размер строки не более 100000.

### Формат вывода
Требуется вывести "Impossible", если решения не существует или "Possible", если можно вернуть всех животных в клетки. В случае если можно, то для каждой ловушки в порядке обхода требуется вывести индекс животного в ней.

### Пример 1
| **Ввод** | **Вывод**  |
| :------- | :--------- |
| ABba     | Possible   |
|          | 2 1        |

### Пример 2
| **Ввод** | **Вывод**  |
| :------- | :--------- |
| ABab     | Impossible |

### Примечания
Первый пример: Животное b идёт в ловушку B, а животное a ловится в ловушку A. Их пути не пересекаются, поэтому

Второй пример: Пути животных пересекаются, поэтому поймать их невозможно


## Конфигурационный файл
Вадим разрабатывает парсер конфигурационных файлов для своего проекта. Файл состоит из блоков, которые выделяются с помощью символов «{» — начало блока, и «}» — конец блока. Блоки могут вкладываться друг в друга. В один блок может быть вложено несколько других блоков.

В конфигурационном файле встречаются переменные. Каждая переменная имеет имя, которое состоит из не более чем десяти строчных букв латинского алфавита. Переменным можно присваивать числовые значения. Изначально все переменные имеют значение 0.

Присваивание нового значения записывается как <variable>=<number>, где <variable> — имя переменной, а <number> — целое число, по модулю не превосходящее 10^9. Парсер читает конфигурационный файл построчно. Как только он встречает выражение присваивания, он присваивает новое значение переменной. Это значение сохраняется до конца текущего блока, а затем восстанавливается старое значение переменной. Если в блок вложены другие блоки, то внутри тех из них, которые идут после присваивания, значение переменной также будет новым.

Кроме того, в конфигурационном файле можно присваивать переменной значение другой переменной. Это действие записывается как <variable1>=<variable2>. Прочитав такую строку, парсер присваивает текущее значение переменной variable2 переменной variable1. Как и в случае присваивания константного значения, новое значение сохраняется только до конца текущего блока. После окончания блока переменной возвращается значение, которое было перед началом блока.

Для отладки Вадим хочет напечатать присваиваемое значение для каждой строки вида <variable1>=<variable2>. Помогите ему отладить парсер.

### Формат ввода
Входные данные содержат хотя бы одну и не более 105 строк. Каждая строка имеет один из четырех типов:

* { — начало блока;
* } — конец блока;
* <variable>=<number> — присваивание переменной значения, заданного числом;
* <variable1>=<variable2> — присваивание одной переменной значения другой переменной. Переменные <variable1> и <variable2> могут совпадать.

Гарантируется, что ввод является корректным и соответствует описанию из условия. Ввод не содержит пробелов.

### Формат вывода
Для каждой строки типа <variable1>=<variable2> выведите значение, которое было присвоено.

### Пример
| **Ввод**     | **Вывод**  |
| :----------- | :--------- |
| a=b          | 0          |
| b=123        | 123        |
| var=b        | -34        |
| b=-34        | 1000000000 |
| {            | 1000000000 |
| c=b          | 123        |
| b=1000000000 | -34        |
| d=b          |
| {            |
| a=b          |
| e=var        |
| }            |
| }            |
| b=b          |