# Лабораторна робота №3: Обробка тексту та чисел на мові Python

## Мета роботи
Метою даної лабораторної роботи є реалізація та перевірка роботи різних функцій для обробки тексту та чисел на мові Python.

## Опис завдання
Реалізувати наступні функції:
- `clean_data(data)`: Очищає та нормалізує дані.
- `filter_emails(emails)`: Фільтрує валідні електронні адреси.
- `extract_keywords(text, min_length=4)`: Витягує ключові слова з тексту.
- `process_text(text)`: Обробляє текст, видаляючи символи та приводячи до нижнього регістру.
- `normalize_data(numbers)`: Нормалізує числа.
- `concatenate_strings(data, separator)`: Об'єднує рядки.
- `sum_numeric_strings(numbers)`: Підсумовує числові рядки.
- `filter_numbers(string, threshold)`: Фільтрує числа, що перевищують поріг.
- `map_to_squares(numbers)`: Повертає квадрати чисел.
- `reverse_strings(words)`: Повертає перевернуті рядки.

## Виконання роботи
### Структура проекту
- `main.py`: Основний файл з реалізацією всіх функцій.

### Опис файлів
- `main.py`: Містить реалізацію функцій для обробки тексту та чисел.

### Основні функції
- `clean_data(data)`: Очищає та нормалізує дані, розділені комами.
- `filter_emails(emails)`: Фільтрує валідні електронні адреси.
- `extract_keywords(text, min_length=4)`: Витягує ключові слова, довжина яких перевищує заданий мінімум.
- `process_text(text)`: Видаляє неалфавітні символи та приводить текст до нижнього регістру.
- `normalize_data(numbers)`: Нормалізує числа, ділячи їх на максимальне значення.
- `concatenate_strings(data, separator)`: Об'єднує рядки за заданим розділювачем.
- `sum_numeric_strings(numbers)`: Підсумовує числові значення в рядках.
- `filter_numbers(string, threshold)`: Повертає числа, що перевищують заданий поріг.
- `map_to_squares(numbers)`: Повертає квадрати чисел.
- `reverse_strings(words)`: Повертає перевернуті рядки.

### Приклади використання
```python
data = " Apple, Banana , orange "
cleaned = clean_data(data)
print(cleaned)  # Output: ['apple', 'banana', 'orange']

emails = "mail us @email.com test@example.com and invalid-email.com.djwd with example@test.co"
valid_emails = filter_emails(emails)
print(valid_emails)  # Output: ['test@example.com', 'example@test.co']

words = "apple pear banana kiwi"
filtered_words = extract_keywords(words, 4)
print(filtered_words)  # Output: ['apple', 'banana', 'kiwi']

texts = " Hello! , Yes? , No. , "
processed_texts = process_text(texts)
print(processed_texts)  # Output: ['hello', 'yes', 'no']

numbers = "10, 20,30"
normalized_numbers = normalize_data(numbers)
print(normalized_numbers)  # Output: [0.333, 0.667, 1.0]

data = "hello*world*again"
concatenated = concatenate_strings(data, '*')
print(concatenated)  # Output: 'helloworldagain'

numbers = "1, 2, test, 3, 4"
total_sum = sum_numeric_strings(numbers)
print(total_sum)  # Output: 10

numbers = "10, test30, 40"
filtered = filter_numbers(numbers, 25)
print(filtered)  # Output: [30, 40]

numbers = "1, 2, 3, 4"
squared_numbers = map_to_squares(numbers)
print(squared_numbers)  # Output: [1, 4, 9, 16]

words = "apple,banana,carrot"
reversed_words = reverse_strings(words)
print(reversed_words)  # Output: ['elppa', 'ananab', 'torrac']
