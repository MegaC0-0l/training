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

