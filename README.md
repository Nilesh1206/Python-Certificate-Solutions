# Python-Certificate-Solutions
This is my hand written solution,I just write here required code.
problem 1: Reverse word and Swap Cases
   
   def reverse_words_order_and_swap_cases(sentence):
       words=sentence.split()
       words=list(reversed(words))
       j="".join(words)
       return j.swapcase()
       
       
Problem 2: Car boat problem
   
    class Car:
         def __init__(self,speed,unit):
             self.speed=speed
             self.unit=unit
         def__str__(self):
             my_string="Car with the maximum speed of {} {} "
             return my_string.format(self.speed,self.unit)
             
    class Boat:
    def__init__(self,speed):
        self.speed=speed
    def__str__(self):
        my_string="Boat with the maaximum speed of {} knots"
        return my_string.format(self.speed)
        
 problem 3: Shape classes with Area method
 
import math
import os
import random
import re
import sys



class Rectangle:
    def _init_(self,l,b):
        self.l=l
        self.b=b
    def area(self):
        return self.l*self.b

   

class Circle:
    def _init_(self,r):
        self.r=r
    def area(self):
        return math.pi*self.r*self.r
   
if _name_ == '_main_': 
    fptr = open(os.environ['OUTPUT_PATH'], 'w')
    q = int(input())
    queries = []
    for _ in range(q):
        args = input().split()
        shape_name, params = args[0], tuple(map(int, args[1:]))
        if shape_name == "rectangle":
            a, b = params[0], params[1]
            shape = Rectangle(a, b)
        elif shape_name == "circle":
            r = params[0]
            shape = Circle(r)
        else:
            raise ValueError("invalid shape type")
        fptr.write("%.2f\n" % shape.area())
    fptr.close()
    
    
Problem 4:Average Function
       from statistics import mean
       def avg(*num1):
            return mean(num1)
 
  
