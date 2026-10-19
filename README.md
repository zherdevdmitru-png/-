# -Task 1
# Определить переменные разных типов и вывести их типы

integer_value = 10
float_value = 3.14
boolean_value = True
string_value = "Привет"
none_value = None

print(type(integer_value))
print(type(float_value))
print(type(boolean_value))
print(type(string_value))
print(type(none_value))

#Task 2
# Преобразования типов данных

# 1. Преобразовать age в число
age = "23"
age = int(age)
print(age)

# 2. Строка "23abc" не преобразуется в число напрямую через int()
foo = "23abc"
try:
    foo_number = int(foo)
    print(foo_number)
except ValueError:
    print(f"Строку {foo!r} нельзя преобразовать в int напрямую.")

# 3. Преобразовать строку "123abc" в Boolean
age = "123abc"
print(bool(age))  # True, потому что строка не пустая

# 4. Преобразовать flag в Boolean
flag = 1
print(bool(flag))  # True

# 5. Преобразовать строки в Boolean
str_one = "Privet"
str_two = ""
print(bool(str_one))  # True
print(bool(str_two))  # False

# 6. Преобразовать 0 и 1 в Boolean
print(bool(0))  # False
print(bool(1))  # True

# 7. Преобразовать False в строку
print(str(False))  # "False"

#Task 3
# Поменять значения переменных местами

age = 36.6
temperature = 25

age, temperature = temperature, age

print("age =", age)
print("temperature =", temperature)

#Task 4
# Вывести наибольшее из трех чисел без max() и других функций поиска максимума

x = int(input("Введите x: "))
y = int(input("Введите y: "))
z = int(input("Введите z: "))

largest = x

if y > largest:
    largest = y

if z > largest:
    largest = z

print("Наибольшее число", largest)

#Task 5
# Арифметические операции над двумя числами

a = float(input("Введите первое число: "))
b = float(input("Введите второе число: "))

print("Сумма:", a + b)
print("Разность:", a - b)

if b != 0:
    print("Частное:", a / b)
    print("Результат целочисленного деления:", a // b)
    print("Остаток от деления:", a % b)
else:
    print("Деление, целочисленное деление и остаток не определены: второе число равно нулю.")

print("Произведение:", a * b)
print("Возведение первого числа в степень второго:", a ** b)

#Task 6
# Площадь квадрата

a = float(input("Введите сторону квадрата: "))
S = a ** 2

print("Площадь квадрата:", S)

#Task 7
# Длины отрезков AC и BC и их сумма

A = float(input("Введите координату точки A: "))
B = float(input("Введите координату точки B: "))
C = float(input("Введите координату точки C: "))

AC = abs(A - C)
BC = abs(B - C)

print("Длина отрезка AC:", AC)
print("Длина отрезка BC:", BC)
print("Сумма длин отрезков AC и BC:", AC + BC)

#Task 8
# Проверить, читается ли четырехзначное число одинаково слева направо и справа налево

number = input("Введите четырехзначное число: ")

if len(number) == 4 and number.isdigit():
    if number[0] == number[3] and number[1] == number[2]:
        print("Число читается одинаково слева направо и справа налево.")
    else:
        print("Число не читается одинаково слева направо и справа налево.")
else:
    print("Ошибка: необходимо ввести ровно четырехзначное число.")

#Task 9
# Решение линейного уравнения A * x + B = 0
# По условию коэффициент A не равен нулю.

A = float(input("Введите коэффициент A (A != 0): "))
B = float(input("Введите коэффициент B: "))

x = -B / A

print("Решение уравнения: x =", x)

#Task 10
#10.1
# Проверить, является ли целое число A четным.

A = int(input("Введите целое число A: "))
print(A % 2 == 0)
#10.2
# Проверить, является ли целое число A нечетным.

A = int(input("Введите целое число A: "))
print(A % 2 != 0)

#Task 11
# По номеру месяца вывести соответствующее время года.

month = int(input("Введите номер месяца (1–12): "))

if month in (12, 1, 2):
    print("зима")
elif month in (3, 4, 5):
    print("весна")
elif month in (6, 7, 8):
    print("лето")
elif month in (9, 10, 11):
    print("осень")
else:
    print("Ошибка: номер месяца должен быть от 1 до 12.")

#Task 12
# Перевести массу тела в килограммы.
# 1 — килограмм, 2 — миллиграмм, 3 — грамм,
# 4 — тонна, 5 — центнер.

unit = int(input("Введите номер единицы массы (1–5): "))
M = float(input("Введите массу тела M: "))

if unit == 1:
    mass_kg = M
elif unit == 2:
    mass_kg = M / 1_000_000
elif unit == 3:
    mass_kg = M / 1_000
elif unit == 4:
    mass_kg = M * 1_000
elif unit == 5:
    mass_kg = M * 100
else:
    print("Ошибка: номер единицы массы должен быть от 1 до 5.")
    raise SystemExit

print("Масса тела в килограммах:", mass_kg)

#Task 13
# Задание 13
# По номеру года определить его название по восточному календарю.
# 1984 год — год зеленой крысы, начало 60-летнего цикла.

year = int(input("Введите номер года: "))

colors_feminine = ["зеленой", "красной", "желтой", "белой", "черной"]
colors_masculine = ["зеленого", "красного", "желтого", "белого", "черного"]

animals = [
    ("крысы", "f"), ("коровы", "f"), ("тигра", "m"), ("зайца", "m"),
    ("дракона", "m"), ("змеи", "f"), ("лошади", "f"), ("овцы", "f"),
    ("обезьяны", "f"), ("курицы", "f"), ("собаки", "f"), ("свиньи", "f")
]

cycle_position = (year - 1984) % 60
color_index = cycle_position // 12
animal, gender = animals[cycle_position % 12]

if gender == "f":
    color = colors_feminine[color_index]
else:
    color = colors_masculine[color_index]

print(f"Год {year}: {color} {animal}")

#Task 14
# Найти для каждого повторяющегося значения массива пару одинаковых элементов
# с минимальным расстоянием между индексами.
# Индексы считаются с нуля.

N = int(input("Введите размер массива N: "))
mass = []

for i in range(N):
    value = int(input(f"Введите элемент массива с индексом {i}: "))
    mass.append(value)

positions = {}

# Сохраняем индексы всех вхождений каждого значения.
for i in range(N):
    value = mass[i]
    if value not in positions:
        positions[value] = []
    positions[value].append(i)

# Для каждого значения ищем ближайшую пару индексов.
for value, indexes in positions.items():
    if len(indexes) < 2:
        print(f"Для числа {value} нет минимального расстояния: элемент в массиве один.")
    else:
        min_distance = indexes[1] - indexes[0]
        left_index = indexes[0]
        right_index = indexes[1]

        # Индексы уже идут по возрастанию, поэтому достаточно сравнить соседние.
        for i in range(1, len(indexes) - 1):
            distance = indexes[i + 1] - indexes[i]
            if distance < min_distance:
                min_distance = distance
                left_index = indexes[i]
                right_index = indexes[i + 1]

        print(
            f"Для числа {value} минимальное расстояние по индексам: "
            f"{left_index} и {right_index} (расстояние {min_distance})."
        )

#Task 15
# Дан целочисленный массив из 10 элементов.
# Увеличить каждый элемент массива на единицу.

mass = []

for i in range(10):
    value = int(input(f"Введите элемент массива с индексом {i}: "))
    mass.append(value)

for i in range(10):
    mass[i] += 1

print("Преобразованный массив:", mass)

#Task 16
users = [{'login': 'Piter', 'age': 23, 'group': "admin"},
         {'login': 'Ivan',  'age': 10, 'group': "guest"},
         {'login': 'Dasha', 'age': 30, 'group': "master"},
         {'login': 'Fedor', 'age': 13, 'group': "guest"}]


def age_word(age):
    """Подбирает форму слова: год / года / лет."""
    if 11 <= age % 100 <= 14:
        return "лет"
    last = age % 10
    if last == 1:
        return "год"
    if 2 <= last <= 4:
        return "года"
    return "лет"


def print_users(result):
    if not result:
        print("Пользователи не найдены")
        return
    for u in result:
        print(f"Пользователь: '{u['login']}' возраст {u['age']} {age_word(u['age'])} , "
              f"группа  \"{u['group']}\"")


print("Выберите тип сортировки:")
print("1. По возрасту")
print("2. По первой букве")
print("3. По группе")

sort_type = input("тип сортировки: ").strip()
criteria = input("Введите критерии поиска: ").strip()

if sort_type == "1":
    if criteria.isdigit():
        min_age = int(criteria)
        result = sorted((u for u in users if u['age'] > min_age),
                        key=lambda u: u['age'])
        print("Результат:")
        print_users(result)
    else:
        print("Ошибка: возраст должен быть числом")

elif sort_type == "2":
    if criteria:
        letter = criteria[0].lower()
        result = sorted((u for u in users if u['login'].lower().startswith(letter)),
                        key=lambda u: u['login'])
        print("Результат:")
        print_users(result)
    else:
        print("Ошибка: введите букву")

elif sort_type == "3":
    group = criteria.lower()
    result = sorted((u for u in users if u['group'].lower() == group),
                    key=lambda u: u['login'])
    print("Результат:")
    print_users(result)

else:
    print("Ошибка: неверный тип сортировки")
