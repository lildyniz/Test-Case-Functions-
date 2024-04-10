### 1. Написать функцию, которая принимает на вход список целых чисел и возвращает новый список, содержащий только уникальные элементы из исходного списка.
```
def unique_elements(input_list):

    # Реализация через цикл for:
    unique_list = []
    for elem in input_list:
        if elem not in unique_list:
            unique_list.append(elem)
    return unique_list

    # Реализация через преобразование в множество:
    unique_set = set(input_list)
    unique_list = list(unique_set)
    return unique_list

    # Реализация через преобразование в ключи словаря:
    return list(dict.fromkeys(input_list))
```

### 2. Написать функцию, которая принимает на вход два целых числа (минимум и максимум) и возвращает список всех простых чисел в заданном диапазоне.
```
def prime_numbers_range(minimum, maximum):
    primes = []
    for num in range(max(2, minimum), maximum + 1):
        is_prime = True
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            primes.append(num)
    return primes
```

### 3. Создать класс Point, который представляет собой точку в двумерном пространстве. Класс должен иметь методы для инициализации координат точки, вычисления расстояния до другой точки, а также для получения и изменения координат.
```
class Point:
    def __init__(self, x=0, y=0):
        # Инициализация.
        self.x = x
        self.y = y

    def distance_to(self, other):
        # Вычисление расстояния до другой точки.
        return ((self.x - other.x) ** 2 + (self.y - other.y) ** 2) ** 0.5

    def get_coordinates(self):
        # Получение координат точки в виде кортежа (x, y).
        return self.x, self.y

    def set_coordinates(self, x, y):
        # Установка новых координат точки.
        self.x = x
        self.y = y
```

### 4. Написать программу, которая сортирует список строк по длине, сначала по возрастанию, а затем по убыванию.
```
def sort_strings_by_length(strings):

    # Сортировка по возрастанию длины строки
    sorted_strings_asc = sorted(strings, key=len)

    # Сортировка по убыванию длины строки
    sorted_strings_desc = sorted(strings, key=len, reverse=True)

    return sorted_strings_asc, sorted_strings_desc
```
