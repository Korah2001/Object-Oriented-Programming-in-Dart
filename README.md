# Object-Oriented-Programming-in-Dart
# Define an interface
class Animal:
    def speak(self):
        pass

# Define a class that implements the interface
class Dog(Animal):
    def speak(self):
        return "Woof!"

# Define a class that overrides an inherited method
class Cat(Animal):
    def speak(self):
        return "Meow!"

# Define a class that initializes with data from a file
class Zoo:
    def __init__(self, filename):
        self.animals = []
        with open(filename, 'r') as file:
            for line in file:
                animal_type, name = line.strip().split(',')
                if animal_type == "dog":
                    self.animals.append(Dog(name))
                elif animal_type == "cat":
                    self.animals.append(Cat(name))

    def make_sounds(self):
        for animal in self.animals:
            print(animal.speak())

# Demonstrate the use of a loop
def main():
    zoo = Zoo("animals.txt")
    zoo.make_sounds()

if __name__ == "__main__":
    main()
