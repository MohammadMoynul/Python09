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
