# README.md

# Program Overview
The Weather Reporter System is a simple object-oriented Python program that simulates weather reports for any city input by the user. Its purpose is to demonstrate OOP principles such as encapsulation, object creation, and method invocation while generating randomized weather conditions and temperatures.

# Development Environment 
Developed in Python 3.11 using Visual Studio Code with the built-in terminal and Python extension.

# Implementation Process: 
First, a WeatherReport class was created to store city data and generate weather output. Then, a WeatherSystem class was built to manage multiple reports. Finally, sample cities were passed to the system to display results.

# Testing & Debugging: 
![My Screenshot](Screenshot)

```python
import random

class WeatherReport:
    def __init__(self, city):
        self.city = city
        self.temperature = None
        self.condition = None

 def generate_report(self):
        self.temperature = round(random.uniform(15.0, 35.0), 1)  # Celsius
        self.condition = random.choice(["Sunny", "Cloudy", "Rainy", "Stormy", "Windy"])
        return f"Weather in {self.city}: {self.temperature}°C, {self.condition}"

class WeatherSystem:
    def __init__(self):
        self.reports = []

 def get_weather(self, city):
        report = WeatherReport(city)
        result = report.generate_report()
        self.reports.append(report)
        return result

# 🧪 Example usage
if __name__ == "__main__":
    system = WeatherSystem()
    print(system.get_weather("Manila"))
    print(system.get_weather("Tokyo"))
    print(system.get_weather("New York"))



