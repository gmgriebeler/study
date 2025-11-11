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

**Class inheritance:**
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

    **Customizing constructors:**
      class SavingsAccount(BankAccount):
      
        **# specific constructor for SavingsAccount with an additional parameter**
        def __init__(self, balance, interest_rate):
        
          **# call the parent constructor using ClassName.__init__()**
          BankAccount.__init__(self, balance) # <-- first call the constructor from the parent class (self in this case is a SavingsAccount, but also a BankAccount)
          
          # Adding more functionality
          self.insterest_rate = interest_rate

          acct = SavingsAccount(1000, 0.03)
          acct.interest_rate

          # New functionality
          def compute_interest(self, n_periods = 1):
            return self.balance * ((1 + self.interest_rate) ** n_periods - 1) # the new method uses the balance attribute (inherited from the Parent class) and also the interest_rate attribute, which only exists in the new class 


      
