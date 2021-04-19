# работа с файлом
print(end='\n')
print('------------------------------------')
file = open('11.txt', encoding='utf-8')

print(file.readline())
print(file.readline())
print(file.seek(0))
print(end='\n')
print(file.read())
print(end='\n')
# с помощью цикла for
file = open('11.txt', encoding='utf-8')
for row in file:
    print(row)
print(end='\n')
# вложенный цикл в переменную row
file = open('11.txt', encoding='utf-8')
for row in file:
    for letter in row:
        print(letter)
# с помощью метода readlines (преобразования в строку)
print(end='\n')
file = open('11.txt', encoding='utf-8')
s = file.readlines()
print(s)
print(end='\n')
# запись в файл и чтение
file = open('11.txt', 'a+', encoding='utf-8')
file.write('Перезаписал\n')
file.read()

print(end='\n')
print('------------------------------------')


def countUpperAndLower(s):
    N1 = 0
    N2 = 0
    for i in s:
        if i >= 'A' and i <= 'Z':
            N1 += 1
        elif i >= 'a' and i <= 'z':
            N2 += 1
    print("upper: " + str(N1), "lower: " + str(N2))


countUpperAndLower("OVERONE cool")

print(end='\n')
print('------------------------------------')
l1 = ['upper', 'lower']
l2 = ['20', '10']


def x_dict(l1, l2):
    a = {}
    for x, y in zip(l1, l2):
        a.update(dict([(x, y)]))
    return a


print(x_dict(['upper', 'lower'], ['20', '10']))

print(end='\n')
print('------------------------------------')

d = dict.fromkeys(['upper', 'lower'])
print(d)
d = dict.fromkeys(['upper', 'lower'], 100)
print(d)

print(end='\n')
print('------------------------------------')

s = 'abba'  # можно сделать вводом от пользователя: input('Введите слово для проверки на Палиндром: ')


def IsPalindrome(s):
    if len(s) <= 1:
        return True
    else:
        return s[0] == s[-1] and IsPalindrome(s[1:-1])


print(IsPalindrome(s))

print(end='\n')
print('------------------------------------')

name = str(input('Введите слово для проверки на Палиндром: '))  # проверка на полиндром
a = name[::-1]
if name == a:
    print("True")
else:
    print("False")

print(end='\n')
print('------------------------------------')


def print_kwargs(**kwargs):
    print(kwargs)


print_kwargs(kwargs_1="Aleks", kwargs_2=4.5, kwargs_3=True)

print(end='\n')
print('-------------------------------------')


# Рекурсией
# ------------------------------------------
def fac(n):
    if n == 0:
        return 1
    return fac(n-1) * n
 
 
print(fac(5))


def factorial(n):
    if (n <= 1):
        return 1
    else:
        return (n * factorial(n-1))
n = int(input("Введите число:"))
print("Факториал числа равен:")
print(factorial(n))
# -------------------------------------------

# циклом
# -------------------------------------------

n = int(input())

factorial = 1
while n > 1:
    factorial *= n
    n -= 1

print(factorial)

# -------------------------------------------

# Реализуйте функцию, которая принимает список и выводит каждый третий элемент из списка/строки (т.е. элементы с индексами 3, 6, 9 и т.д.)
# на счет функции не уверен, тут вот так получилось 
for i in range(3, 10, 3):
    print(i, end=' ')

# -------------------------------------------
# квадрат из звездочек
def print_s(n):
    list(map(print, ['*' * n] * n))
print_s(5)

# -------------------------------------------

# 


def posneg(lst):
    positive, negative = [],[]
    for i in lst:
        if i>0:
            positive.append(i)
        else:
            negative.append(i)
            
    return positive, negative
        
print(posneg([1, 2, -3, 4, -5]))

