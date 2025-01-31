## Задача 3. База автомобилей *(не обязательна к выполнению)

### Описание
Вы разрабатываете систему учета автотранспорта. Автомобиль в ней представлен следующими атрибутами — "номер", "марка", "цвет", "тип кузова", где уникальным ключом является номер.
Структура данных, куда сохраняются автомобили, должна отбрасывать ввод одного и того же автомобиля 2 раза. Ввод пустой строки вместо информации об автомобиле, завершает программу и выводит список уже введенных автомобилей,
разделив их по типу автомобиля (грузовой, легковой), где тип автомобиля — класс созданного объекта.

### Функционал программы
1. Ввод информации об автомобиле: номер, марка, цвет, тип кузова, тип автомобиля;
2. Вывод списка сначала легковые автомобили, затем грузовые автомобили.

### Пример
```
Введите информацию об автомобиле:
А192АА199, ВАЗ 2105, белый, седан <enter>
Введите информацию об автомобиле:
А121АА190, ВАЗ 2106, синий, седан <enter>
Введите информацию об автомобиле:
B788AB99, Камаз 120, красный, "" <enter>
<enter>
Легковые автомобили:
А192АА199, ВАЗ2105, белый, седан
А121АА190, ВАЗ2106, синий, седан

Грузовые автомобили:
B788AB99, Камаз 120, красный
```

### Реализация
1. Создайте базовый класс `Car` с полями `Number`, `Producer`, `Color` тип полей – `String` и `Type` - enum.
2. Унаследуйте базовый класс `Car` и создайте два наследника для грузовых автомобилей и легковых.
2. Переопределите методы `hashcode` и `equals` для класса `Car` так, чтобы нельзя было сохранить две машины с одинаковым номером.
3. Продемонстрируйте добавление объектов класса в HashSet, ошибку при добавлении машин с одинаковыми номерами, возможность существования двух одинаковых машин с разным номером.
