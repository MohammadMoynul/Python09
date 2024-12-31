# Python09
Software 2_programming_assignment
class Car:
    def __init__(self, registration_number, maximum_speed):
        self.registration_number = registration_number
        self.maximum_speed = maximum_speed
        self.current_speed = 0
        self.travelled_distance = 0

    def __str__(self):
        return (f"Registration Number: {self.registration_number}\n"
                f"Maximum Speed: {self.maximum_speed} km/h\n"
                f"Current Speed: {self.current_speed} km/h\n"
                f"Travelled Distance: {self.travelled_distance} km")

# Main program
if __name__ == "__main__":
    new_car = Car("ABC-123", 142)
    print(new_car)
##
import random

class Car:
    def __init__(self, registration_number, maximum_speed):
        self.registration_number = registration_number
        self.maximum_speed = maximum_speed
        self.current_speed = 0
        self.travelled_distance = 0

    def accelerate(self, speed_change):
        self.current_speed += speed_change
        if self.current_speed > self.maximum_speed:
            self.current_speed = self.maximum_speed
        elif self.current_speed < 0:
            self.current_speed = 0

    def drive(self, hours):
        self.travelled_distance += self.current_speed * hours

    def __str__(self):
        return (f"{self.registration_number:<10} | {self.maximum_speed:<14} | {self.current_speed:<13} | {self.travelled_distance:<17}")

# Main program
if __name__ == "__main__":
    # Create 10 cars
    cars = [Car(f"ABC-{i+1}", random.randint(100, 200)) for i in range(10)


    # Print table header
    print(f"{'Registration':<10} | {'Max Speed (km/h)':<14} | {'Current Speed':<13} | {'Travelled Distance':<17}")
    print("-" * 60)

    winner = None
    while not winner:
        for car in cars:
            # Random speed change between -10 and +15
            speed_change = random.randint(-10, 15)
            car.accelerate(speed_change)
            # Drive for one hour
            car.drive(1)

            # Check if any car has reached 10,000 km
            if car.travelled_distance >= 10000:
                winner = car

    # Print final properties of all cars
    for car in cars:
        print(car)

    print("\nThe winner is:")
    print(f"{winner.registration_number} with {winner.travelled_distance} km travelled!")
    
