# GenericTabulator
#Basic
1. Класс `GenericTabulator` реализовывает интерфейс `Tabulator` и строит трехмерную таблицу значений заданного выражения.
	* `mode` — режим вычислений:
		* `i` — вычисления в `int` с проверкой на переполнение;
		* `d` — вычисления в `double` без проверки на переполнение;
		* `bi` — вычисления в `BigInteger`.
	* `expression` — выражение, для которого надо построить таблицу;
	* `x1`, `x2` — минимальное и максимальное значения переменной `x`(включительно)
	* `y1`, `y2`, `z1`, `z2` — аналогично для `y` и `z`.
2. Результат: 
	* Элемент `result[i][j][k]` содержит значение выражения для `x = x1 + i`, `y = y1 + j`, `z = z1 + k`. Если значение не определено (например, по причине переполнения), то соответствующий элемент должен быть равен `null`.

# Easy
1. Дополнительно реализованы унарные операции:
	* `abs` — модуль числа, `abs -5` равно `5`;
	* `square` — возведение в квадрат, `square 5` равно `25`.
2. Дополнительно реализована бинарная операция (максимальный приоритет):
	* `mod` — взятие по модулю, приоритет как у умножения (`1 + 5 mod 3` равно `1 + (5 mod 3)` равно `3`).
3. Дополнительно реализованы поддержка режимов:
	* `u` — вычисления в `int` без проверки на переполнение;
	* `b` — вычисления в `byte` без проверки на переполнение;
	* `f` — вычисления в `float` без проверки на переполнение.