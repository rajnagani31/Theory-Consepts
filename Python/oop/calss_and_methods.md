# what is class and methods

class is a blueprint for creating objects, defining a set of attrbutes(data) and methods(functions) that objects of the class will have.

# Whats is OOPs?

Object-oriented programming (OOP) is a programming paradigm that orgeanizes code around objects rather than functions and logic.
it halps in creating modular, reusable and scalable code.

# What is Static Method?

1. Static method behave like regular and normal functions, but lives inside a class for logical grouping.

2. They do not have access to instance (self) or class (cls) variables and methods.

### key points

- not use self
- not use cls
- used for utility and hlper functions
- Keeps related logic inside a class

```bash
class MathUtils:
    @staticmethod
    def add(a, b):
        return a + b

```

# what is class method?

1. Takes cls as the first parameter instead of self.

2. Can access and modify class variables

3. Often used as alternative constructors

```bash
class User:
    company = "ScalerByte"

    @classmethod
    def get_company(cls):
        return cls.company
```

### alernative constructor

```bash
class User:
    def __init__(self, name):
        self.name = name

    @classmethod
    def from_email(cls, email):
        name = email.split("@")[0]
        return cls(name)

# Output

u = User.from_email("raj@gmail.com")
print(u.name)   # raj
```

# what is proparty decorator?


1. @property lets you access methods like attributes.

        without property
        user.get_age()

        with property
        user.age

        class Person:
            def __init__(self, age):
                self._age = age

            @property
            def age(self):
                return self._age


```bash
class ReadOnly:
    def __init__(self,brand,model):
        self.brand = brand
        self._model = model -> private attribute like _model

    @property  
    def models(self): -> getter method
        return self._model
    
data = ReadOnly('TATA','Seari')
#data.models='new' 
print(data.models)

->when you overwrite your model after make priavet when generate this error AttributeError: can't set attribute ERROR : property 'models' of 'ReadOnly' object has no setter
```

###property with setter

```bash
class Person:
    def __init__(self, age):
        self._age = age

    @property
    def age(self):
        return self._age

    @age.setter
    def age(self, value):
        if value < 0:
            raise ValueError("Age cannot be negative")
        self._age = value

p = Person()
p.age = 30     # ✅ allowed
p.age = -5    # ❌ error

```
### key points

- Encapsulation
- Validation logic
- Cleaner syntax
- Used like attributes

### 🔹 When to use @property

✅ Need read-only or controlled attributes
✅ Validation required
✅ Want clean API

# 🆚 Quick Comparison Table

Feature	       @staticmethod	@classmethod	@property

Uses self	       ❌	          ❌	            ✅

Uses cls	       ❌	          ✅	            ❌

Access instance data❌	          ❌         	✅

Access class data	❌	          ✅	            ❌

Called like method	✅	          ✅	            ❌ (attribute style)

Common use	    Helper functions Factory methods	Encapsulation

# 🧠 Interview One-Line Answers

- @staticmethod → Utility function inside a class

- @classmethod → Class-level method or factory method

- @property → Method that behaves like an attribute

# 🎯 Which one should you use?

- Validation / Encapsulation → @property

- Alternate object creation → @classmethod

- Helper logic → @staticmethod