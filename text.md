# -*- coding: cp1251 -*-

#2
def rectangle_area(width, height):
    area = width * height
    return area
#3
def is_even(number):
    if number % 2 == 0:
      return True
    else: 
      return False
#4
def sum_digits(number):
    digits_sum = 0
    while number > 0:
        digits_sum += number % 10
        number //= 10
    return digits_sum

