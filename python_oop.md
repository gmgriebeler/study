Objects --> Data structure that incorporates state + behavior

Encapsulation --> Bundling data with code operating in it

Class --> "Blueprints for objects"
  --> objects are the realization of classes, with particular state values

  **Classes** incorporate info about state and behavior
    - states are contained in **attributes** --> attributes are represented by **variables** (ex: obj.my_attribute)
    - behavior are contained in **methods** --> methods are represented by **functions()** (ex: obj.my_method())

__init__ is a class constructor, which is a method that automatically called when a new **instance(object)** is created, allowing the definition of initital parameters for the method, and for the objects to come
  def __init__(self, parameter_1):

@class methods are methods that impact the class itself, not only specific instances
  @classmethod
  def example(cls, parameter_1):

Class inheritance:
  Is a mechanism that allows to define new classes that gets functionalities of older classes, without reimplementing the code already written
  To implement class inheritance, we simply add parenthesis after the class name and specify the class to inherit from.
    Ex: class BankAccount:
          def __init__(self, balance):
            self.balance = balance
    
          def withdraw(self, amount):
            self.balance -= amount

        class SavingsAccount(BankAccount):
          pass     #empty class for now

  Inheritance: "is-a" relationship --> Ex: SavingsAccount is a BankAccount


      
