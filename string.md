## Задание 1

Составьте запрос, который выводит список студентов в формате: фамилия и имя заглавными буквами, а email — строчными буквами. Для таких задач обычно используются функции изменения регистра, например `UPPER()` и `LOWER()`. [postgresql](https://www.postgresql.org/docs/current/functions-string.html)

Таблица: `students`
- `id`
- `last_name`
- `first_name`
- `email`

Что нужно получить:
- `student_name` — результат объединения `last_name` и `first_name` через пробел в верхнем регистре.
- `email_normalized` — email в нижнем регистре. 

## Задание 2

Напишите запрос, который очищает телефонные номера от лишних символов. Для обработки строк SQL поддерживает замену фрагментов текста через `REPLACE()`, а также удаление пробелов по краям через `TRIM()`. [tigerdata](https://www.tigerdata.com/learn/postgresql-string-functions)

Таблица: `clients`
- `id`
- `full_name`
- `phone`

Что нужно сделать:
- удалить из `phone` символы `(`, `)`, `-`, пробелы;
- вывести результат в поле `clean_phone`. 

Пример:
- было: `+7 (999) 123-45-67`
- стало: `+79991234567`

## Задание 3

Составьте запрос, который для каждого товара выделяет первые 3 символа кода и последние 2 символа кода. Для этого применяют функции извлечения части строки, например `LEFT()` и `RIGHT()`. [sqlservertutorial](https://www.sqlservertutorial.net/sql-server-string-functions/)

Таблица: `products`
- `id`
- `product_name`
- `article_code`

Что нужно вывести:
- `product_name`
- `code_start` — первые 3 символа `article_code`
- `code_end` — последние 2 символа `article_code` 

## Задание 4

Напишите запрос, который находит позицию символа `@` в адресе электронной 
почты и отдельно выделяет доменную часть email. Строковые функции SQL позволяют искать подстроку внутри строки и извлекать часть текста по позиции, например через функции поиска и `SUBSTRING()`. [postgresql](https://www.postgresql.org/docs/current/functions-string.html)

Таблица: `users`
- `id`
- `username`
- `email`

Что нужно вывести:
- `email`
- `at_position` — позиция символа `@`
- `email_domain` — часть строки после `@` 

