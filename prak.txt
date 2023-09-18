import math

def is_digit(x):
    try:
        float(x)
        return True
    except ValueError:
        return False

while True:
    choice = input("Выберите операцию:\n"
                   "1) Сложение\n"
                   '2) Вычитание\n'
                   '3) Умножение\n'
                   '4) Деление\n'
                   '5) Возвести в степень\n'
                   '6) Квадратный корень\n'
                   '7) Факториал\n'
                   '8) Синус\n'
                   '9) Косинус\n'
                   '10) Тангенс\n'
                   '0) Выход\n')
    if not is_digit(choice):
        print("Ошибка, неверыный номер Вашей операции")
        continue

    choice = int(choice)

    if choice == 0:
        break
    if choice in [1, 2, 3, 4]:
        while True:
            x = input ('Введите первое число: ')
            y = input ('Введите второе число: ')

            if is_digit(x) and is_digit(y):
                x = float(x)
                y = float(y)
                break
            else:
                print('Ошибка, некорректно введенны числа')
    elif choice in [5,6,7,8,9,10]:
        x = input('Введите число: ')

        if is_digit (x): 
            x = float(x)
        else:
            print ("Ошибка, некорректно введенно число")

    if choice == 1:
        print('Результат: ', x + y)
    elif choice == 2:
        print ('Результат: ', x - y)
    elif choice == 3:
        print ('Результат: ', x * y)
    elif choice == 4:
        if y == 0:
           print ('Ошибка, делить на 0 нельзя')
        else:
           print('Результат: ', x / y)
    elif choice == 5:
         print('Результат: ', x ** y)
    elif choice == 6:
        if x < 0:
          print ('Ошибка, не бывает квадратного корня из отрицательного числа')
        else:
           print('Результат: ', math.sqrt(x))
    elif choice == 7:
         if x < 0:
           print('Ошибка, не бывает факториал отрицательного числа')
         else:
           print("Результат: ", math.factorial(int(x)))
    elif choice == 8:
        print('Результат: ', math.sin(x))
    elif choice == 9:
        print("Результат:", math.cos(x))
    elif choice == 10:
        print ('Результат: ', math.tan(x))
    else:
        print ('Ошибка, неверный номер операции')
