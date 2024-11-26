# Activity 25: SOLID PRINCIPLES IN ANGULAR


## SOLID Principles:

## 1. Single Responsibility Principle (SRP)
Definition: A class should have only one reason to change, meaning it should have one responsibility or job.

Example:

 ``` typescript
class Report:
    def generate_report(self):
        # Logic to generate report
        pass

class ReportPrinter:
    def print_report(self, report):
        # Logic to print the report
        pass

 ```
Explanation:
Here, the Report class only handles report generation, while the ReportPrinter class handles printing. This adheres to SRP because each class has only one responsibility.

## 2. Open/Closed Principle (OCP)
Definition: Software entities (classes, modules, functions) should be open for extension but closed for modification.

Example:

 ``` typescript
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius * self.radius
```
Explanation:
New shapes (like Circle, Rectangle) can be added without modifying the Shape class, thus adhering to the OCP principle.

## 3. Liskov Substitution Principle (LSP)
Definition: Objects of a subclass should be replaceable with objects of the superclass without affecting the correctness of the program.

Example:

 ``` typescript
class Bird:
    def fly(self):
        pass

class Sparrow(Bird):
    def fly(self):
        print("Sparrow flying")

class Ostrich(Bird):
    def fly(self):
        raise Exception("Ostriches can't fly")
 ```
Explanation:
Ostrich violates LSP because substituting a Bird with an Ostrich breaks functionality (Ostriches can't fly). A better design would ensure that only birds capable of flying are allowed to implement fly().

## 4. Interface Segregation Principle (ISP)
Definition: Clients should not be forced to depend on interfaces they do not use.

Example:

 ``` typescript
class Printer:
    def print(self):
        pass

class Scanner:
    def scan(self):
        pass

class MultiFunctionDevice(Printer, Scanner):
    def print(self):
        pass
    
    def scan(self):
        pass
 ```
Explanation:
Instead of forcing clients to implement both print() and scan(), we segregate them into different interfaces. Clients who only need printing functionality can implement just the Printer interface, and vice versa.

## 5. Dependency Inversion Principle (DIP)
Definition: High-level modules should not depend on low-level modules. Both should depend on abstractions. Furthermore, abstractions should not depend on details; details should depend on abstractions.

Example:

 ``` typescript
class Database:
    def connect(self):
        pass

class Service:
    def __init__(self, database: Database):
        self.database = database
    
    def perform_action(self):
        self.database.connect()
```
Explanation:
Instead of the Service class depending on a concrete Database class, it depends on an abstract Database interface. This allows easy substitution of different database implementations (e.g., SQL, NoSQL) without changing the Service class.

## Each principle helps make the code more modular, maintainable, and flexible.



## Hashnode Link :
https://christinejane.hashnode.dev/activity-25-solid-principles-in-angular











































