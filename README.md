# README.md
class TemperatureConverter:
    def __init__(self, celsius: float):
        self.celsius = celsius

    def to_fahrenheit(self) -> float:
        return (self.celsius * 9/5) + 32

    def __str__(self):
        return f"{self.celsius}°C is {self.to_fahrenheit():.2f}°F"

# Example usage
user_input = float(input("Enter temperature in Celsius: "))
converter = TemperatureConverter(user_input)
print(converter)
