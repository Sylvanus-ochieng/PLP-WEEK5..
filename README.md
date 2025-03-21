# PLP-WEEK5..
Designing own class


📱 Assignment 1: Design Your Own Class


# Parent class: Smartphone
class Smartphone:
    def __init__(self, brand, model, battery_life):
        self.brand = brand
        self.model = model
        self.battery_life = battery_life  # in hours

    def display_info(self):
        return f"{self.brand} {self.model} - Battery: {self.battery_life} hours"

# Child class: GamingPhone (inherits from Smartphone)
class GamingPhone(Smartphone):
    def __init__(self, brand, model, battery_life, cooling_system):
        super().__init__(brand, model, battery_life)  # Call parent constructor
        self.cooling_system = cooling_system  # New attribute

    def display_info(self):
        return f"{self.brand} {self.model} - Battery: {self.battery_life} hours - Cooling: {self.cooling_system}"

# Creating objects
phone1 = Smartphone("Apple", "iPhone 14", 20)
gaming_phone1 = GamingPhone("Asus", "ROG Phone 6", 24, "Advanced Cooling Tech")

# Displaying information
print(phone1.display_info())         # Output: Apple iPhone 14 - Battery: 20 hours
print(gaming_phone1.display_info())  # Output: Asus ROG Phone 6 - Battery: 24 hours - Cooling: Advanced Cooling Tech

🎭 Activity 2: Polymorphism Challenge
# Parent class
class Vehicle:
    def move(self):
        pass  # Abstract method

# Child classes with different move() behavior
class Car(Vehicle):
    def move(self):
        return "🚗 Driving on the road"

class Bike(Vehicle):
    def move(self):
        return "🏍️ Riding on two wheels"

class Plane(Vehicle):
    def move(self):
        return "✈️ Flying in the sky"

# Creating objects
vehicles = [Car(), Bike(), Plane()]

# Calling move() method on each object
for v in vehicles:
    print(v.move())
