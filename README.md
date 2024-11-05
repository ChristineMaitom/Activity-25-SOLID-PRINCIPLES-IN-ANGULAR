# Activity 25: SOLID PRINCIPLES IN ANGULAR


## SOLID Principles:

## 1. S - Single Responsibility Principle (SRP):

Explanation: A class should have only one reason to change, meaning it should only have one job or responsibility.

Example:

 ``` typescript
class Invoice:
    def calculate_total(self):
        # Logic to calculate total
        pass
    
    def save_to_database(self):  # This violates SRP
        # Logic to save invoice to database
        pass
 ```




















