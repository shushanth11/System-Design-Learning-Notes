📘 @classmethod
✅ Definition

A method that works with the class (cls) instead of an instance, often used to create objects or handle class-level logic.

✅ Example
class User:
    def __init__(self, name):
        self.name = name

    @classmethod
    def from_dict(cls, data):
        return cls(data["name"])
▶ Usage

u = User.from_dict({"name": "Alice"})

print(u.name)

✅ Output

Alice

🧠 Key idea
Uses cls
Can create objects
Works with inheritance
📘 @staticmethod
✅ Definition

A method that does not use class (cls) or instance (self), used for utility/helper logic.

✅ Example
class MathUtils:
    @staticmethod
    def add(a, b):
        return a + b
▶ Usage
result = MathUtils.add(3, 5)
print(result)
✅ Output
8
🧠 Key idea
No self, no cls
Just a function inside a class
🔁 Quick Difference
Feature	@classmethod	@staticmethod
First argument	cls	none
Uses class data	✅	❌
Uses instance data	❌	❌
Main use	Object creation	Utility logic
🎯 Super Simple Summary
@classmethod → works with class → used for creating objects
@staticmethod → works with nothing → used for helper functions
🚀 One-line memory trick

classmethod = class-aware
staticmethod = class-independent
