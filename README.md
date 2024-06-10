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
    git checkout -b feature-update
    git branch
    echo "Some new content" > newfile.txt
    git add newfile.txt
    git commit -m "Added newfile.txt with some content"
    git checkout main
    git merge feature-update
    git pull
    git checkout -b resolve-conflict
    git add newfile.txt
git commit -m "Resolved conflict in newfile.txt"
git checkout main
git merge resolve-conflict
<!DOCTYPE html>
<html>
<head>
    <title>My GitHub Page</title>
</head>
<body>
    <h1>Hello, GitHub Pages!</h1>
</body>
</html>
git add index.html
git commit -m "Added index.html for GitHub Pages"
git push
