# Russkikh_SPm_22_06_Lab1
## Комп'ютерні системи імітаційного моделювання
## СПм-22-6, **Рускix Олександр Валерійович**
### Лабораторна робота №**1**. Опис імітаційних моделей та проведення обчислювальних експериментів

<br>

### Варіант 6, модель у середовищі NetLogo:
[Rabbits Grass Weeds](http://www.netlogoweb.org/launch#http://www.netlogoweb.org/assets/modelslib/Sample%20Models/Biology/Rabbits%20Grass%20Weeds.nlogo)

<br>

### Вербальний опис моделі:
Цей проект досліджує просту екосистему, що складається з кроликів, трави та бур’янів. Кролики безладно блукають, а трава та бур’яни безладно ростуть. Коли кролик натикається на траву або бур’ян, він їсть траву і отримує енергію. Якщо кролик отримує достатньо енергії, він розмножується. Якщо він не отримує достатньо енергії, він гине.

Траву та бур’яни можна налаштувати так, щоб вони росли з різною швидкістю та давали кроликам різну кількість енергії. Модель можна використовувати для дослідження конкурентних переваг цих змінних.

### Керуючі параметри:
- **model speed**. Управління швидкістю моделювання.
- **number**. Початкова кілкість кроликів.
- **birth threshold**. Поріг народження, мінімальна кількість осіб необхідних для продовження популяції
- **grass-grow-rate**. Швидкість росту трави
-  **grass-energy**. Енергетична поживність трави
-  **weeds-grow-rate**. Швидкість росту бур’янів
-  **weeds-energy**.  Енергетична поживність бур’янів

### Внутрішні параметри:
- **move**. Переміщення кроликів.
- **eat-grass**. Їсти траву.
- **eat-weeds**. Їсти бур’ян.
- **reproduce**. Розмножуватися.
- **death**. Смерть.

### Показники роботи системи:
- максимальна швидкість на поточному такті симуляції, тобто, швидкість найшвидшої на даний момент машини на трасі. Не може перевищувати значення speed-limit.
- найменша швидкість на поточному такті, тобто, швидкість найповільнішої в даний момент машини.
- поточна швидкість машини, що відстежується (червона машина).

### Примітки:
При початковому налаштуванні системи не враховується швидкість зростання та поживна енергія бур'янів

### Недоліки моделі:
Недолік системи в тому, що вона не враховує впливу навколишнього середовища, як, наприклад, хижаки (вовки чи лисиці), вплив температури на розмноження, смерть кроликів від хвороб тощо, чисельність і швидкість розмноження кроликів.

<br>

## Обчислювальні експерименти

### 1. Вплив поживної цінності трави на кільккість кроликів
Досліджується залежність максимальної кількості кроликів протягом певної кількості тактів (200) від поживної цінності трави.
Експерименти проводяться при 100 кроликів, з кроком 10, усього 5 симуляцій.  
Інші керуючі параметри мають значення за замовчуванням:
- **birth threshold**: 15
- **grass-grow-rate**: 15

<table>
<thead>
<tr><th>Максимальна кількість кроликів</th><th>Поживна цінність трави</th></tr>
</thead>
<tbody>
<tr><td>173</td><td>3</td></tr>
<tr><td>180</td><td>3</td></tr>
<tr><td>170</td><td>3</td></tr>
<tr><td>166</td><td>3</td></tr>
<tr><td>154</td><td>3</td></tr>
<tr><td>168</td><td>3</td></tr>
</tbody>
</table>

### 2. Перевірка гіпотези про те що поживна цінність трави впливає на максимальну кількість кроликів

## 2. Вплив поживної цінності трави на кільккість кроликів
Досліджується залежність максимальної кількості кроликів протягом певної кількості тактів (200) від поживної цінності трави.
Експерименти проводяться при поживної цінності трави 3 та сталою початковою кількісттю кроликів 150, з кроком 0.5, усього 5 симуляцій.  
Інші керуючі параметри мають значення за замовчуванням:
- **birth threshold**: 15
- **grass-grow-rate**: 15

<table>
<thead>
<tr><th>Максимальна кількість кроликів</th><th>Поживна цінність трави</th></tr>
</thead>
<tbody>
<tr><td>171</td><td>3</td></tr>
<tr><td>204</td><td>3.5</td></tr>
<tr><td>200</td><td>4</td></tr>
<tr><td>255</td><td>4.5</td></tr>
<tr><td>278</td><td>5</td></tr>
<tr><td>280</td><td>5.5</td></tr>
</tbody>
</table>

### 3. Перевірка гіпотези про те що на максимальну кількість кроликів може впливати не тільки поживна цінність трави, а й бур'янів

## 3. Вплив поживної цінності трави та бур'янів на кільккість кроликів
Досліджується залежність максимальної кількості кроликів протягом певної кількості тактів (200) від поживної цінності трави та бур'янів.
Експерименти проводяться при поживної цінності бур'янів 1, сталою швидкісттю роста бур'янів 10, сталою початковою кількісттю кроликів 150, з кроком 1, усього 5 симуляцій.  
Інші керуючі параметри мають значення за замовчуванням:
- **birth threshold**: 15
- **grass-grow-rate**: 15

<table>
<thead>
<tr><th>Максимальна кількість кроликів</th><th>Поживна цінність трави</th></tr>
</thead>
<tbody>
<tr><td>289</td><td>1</td></tr>
<tr><td>331</td><td>2</td></tr>
<tr><td>384</td><td>3</td></tr>
<tr><td>401</td><td>4</td></tr>
<tr><td>466</td><td>5</td></tr>
<tr><td>482</td><td>6</td></tr>
</tbody>
</table>
