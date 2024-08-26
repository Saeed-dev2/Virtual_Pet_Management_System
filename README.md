# Virtual Pet Management System

## Overview

The Virtual Pet Management System is a Python application that allows users to adopt and care for virtual pets. Users can perform various actions such as feeding, playing, and checking the health of their pets. The simulator supports different types of pets including dogs, cats, and birds. The application simulates the passage of time, affecting the pets' hunger, happiness, and health.

## Features

- **Adopt Pets**: Add new pets to your collection with customizable attributes.
- **Care for Pets**: Feed, play with, or check the health of your pets.
- **View Pet Status**: Get detailed information about each pet's condition.
- **Remove Pets**: Remove pets from your collection.
- **Pass Time**: Simulate the passage of time to see how it affects your pets.
- **Support for Multiple Pet Types**: Includes dogs, cats, and birds with specific behaviors.

## Classes

### `Pet`

The base class for all pets. It includes methods for feeding, playing, checking health, and simulating the passage of the time.

**Attributes:**
- `name` (str): The name of the pet.
- `age` (int): The age of the pet.
- `hunger_level` (int): The hunger level of the pet.
- `happiness` (int): The happiness level of the pet.
- `health` (int): The health status of the pet.

**Methods:**
- `feed()`: Reduces hunger level.
- `play()`: Increases happiness and hunger level.
- `check_health()`: Evaluates and adjusts the pet's health.
- `pass_time()`: Simulates the passage of time.

### `Dog`, `Cat`, `Bird`

Derived classes from `Pet` that represent specific types of pets with additional attributes and behaviors.

**Dog Attributes:**
- `breed` (str): The breed of the dog.

**Dog Methods:**
- `bark()`: Makes the dog bark.

**Cat Attributes:**
- `breed` (str): The breed of the cat.

**Cat Methods:**
- `meow()`: Makes the cat meow.

**Bird Attributes:**
- `species` (str): The species of the bird.

**Bird Methods:**
- `chirp()`: Makes the bird chirp.

### `User`

The class responsible for managing pets, including adopting, caring for, viewing, and removing pets.

**Attributes:**
- `name` (str): The name of the user.
- `pets` (list): A list of pets owned by the user.

**Methods:**
- `adopt_pet(pet)`: Adds a pet to the user's collection.
- `care_for_pet(pet_name, action)`: Performs an action on a specified pet.
- `view_pet_status(pet_name)`: Displays the status of a specified pet.
- `pass_time()`: Advances time for all pets.
- `add_pet()`: Prompts the user to add a new pet.
- `remove_pet(pet_name)`: Removes a pet from the collection.
- `view_all_pets()`: Displays the status of all pets.

## Usage

1. **Run the Program**: Execute the script to start the Virtual Pet Simulator.
2. **Menu Options**:
   - **View Pet Info**: Check the status of a specific pet.
   - **Care for a Pet**: Feed, play with, or check the health of a pet.
   - **Add a New Pet**: Add a new pet to your collection.
   - **Remove a Pet**: Remove a pet from your collection.
   - **View All Pets**: View the status of all pets.
   - **Pass Time**: Simulate the passage of time.
   - **Exit**: Exit the simulator.

## Example Interaction

```python
user = User("Saeed")

while True:
    print("\nPet Care Menu:")
    print("1. View Pet Info")
    print("2. Care for a Pet")
    print("3. Add a New Pet")
    print("4. Remove a Pet")
    print("5. View All Pets")
    print("6. Pass Time")
    print("7. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        pet_name = input("Enter the name of the pet you want to view: ")
        user.view_pet_status(pet_name)
    elif choice == "2":
        pet_name = input("Enter the name of the pet you want to care for: ")
        action = input("What would you like to do? (feed/play/check_health/bark/meow/chirp): ").lower()
        user.care_for_pet(pet_name, action)
    elif choice == "3":
        user.add_pet()
    elif choice == "4":
        pet_name = input("Enter the name of the pet you want to remove: ")
        user.remove_pet(pet_name)
    elif choice == "5":
        user.view_all_pets()
    elif choice == "6":
        user.pass_time()
    elif choice == "7":
        print("Exiting the Virtual Pet Simulator. Goodbye!")
        break
    else:
        print("Invalid choice. Please try again.")
