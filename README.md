# README.md
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

