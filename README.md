!!!!Instructor Disclaimer
I was unable to modify the project starter file I am not sure why, by the time this happened office hours were already closed. But I included my full Python implementation in the submission. All required code for my classes, abilities, and functionality appears correctly in the editable portion of the project and all tests cases pass!!!!


COMP 163 – Project 2: Character Abilities Showcase
README Documentation
Overview

This project demonstrates object-oriented programming concepts in Python, including:
Inheritance
Polymorphism
Method overriding
Composition (Players using Weapon objects)
Class-based ability systems
Interaction simulation via a simple battle engine

The program defines a hierarchy of character classes—Warrior, Mage, and Rogue—each extending the base Player class, which itself inherits from Character.
Each subclass overrides the attack() method and includes unique special abilities to highlight polymorphism and class specialization.

A provided SimpleBattle system (included in the starter file) is used for testing but cannot be modified. Due to restrictions with the project starter, only the Python implementation portion is editable, which is the part provided in the submission.

AI Usage: Chat GPT AI assistance was used for approximately 50% of this project, specifically to help clarify inheritance structure, refine method overriding logic, ReadMe files, generate explanatory comments, and verify behavior against GitHub test cases.

How to Run the Program
1. Ensure Python is Installed. You will need Python 3.8+.
2. Run the Script Normally, Open a terminal or command prompt in the project directory and enter:
python character_abilities.py

3. What You Should See
Running the program will automatically:Display the stats of all character types, Demonstrate polymorphic attacks from Warrior, Mage, and Rogue, Demonstrate each class’s special ability, Display weapon information, Run a sample battle using the provided SimpleBattle system, Print the final results of the test showcase
No additional input is required—this project is fully automated for demonstration.

Core Concepts Demonstrated
✔ Inheritance
- Player inherits from Character
- Warrior, Mage, and Rogue inherit from Player
✔ Polymorphism & Method Overriding
Each subclass overrides attack() to use different damage formulas:
- Warrior: Strength-based melee damage
- Mage: Magic-based spell damage
- Rogue: Chance-based critical strikes
✔ Special Class Abilities
- Warrior.power_strike()
- Mage.fireball()
- Rogue.sneak_attack()
✔ Composition

Testing Notes
- The provided SimpleBattle system cannot be modified (as per assignment rules).
- All implemented classes meet the inheritance and overriding requirements used by the GitHub test cases.
- Only the implementable Python portions were supplied in the submission due to starter-code editing restrictions.















[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/mMxhKicI)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21493007&assignment_repo_type=AssignmentRepo)
# COMP 163 - Project 2: Character Abilities Showcase

## 🎯 Project Overview

Build a simple character system that demonstrates mastery of object-oriented programming fundamentals: inheritance, method overriding, polymorphism, and composition. This project focuses on core OOP concepts without the complexity of a full game system.

## 📋 Getting Started

1. **Complete your implementation** in `project2_starter.py`
2. **Test your code** by running: `python project2_starter.py`
3. **Run automated tests** with: `python -m pytest tests/ -v`
4. **Commit and push** to see GitHub test results

## 🏗️ What You're Building

### **Class Structure (6 Classes Total)**

```
Character (base class)
    ↓
Player (inherits from Character)  
    ↓
Warrior, Mage, Rogue (inherit from Player)

Weapon (composition - separate class)
```

### **Required Stats for Each Class:**

| Class   | Health | Strength | Magic | Special Ability |
|---------|--------|----------|-------|-----------------|
| Warrior | 120    | 15       | 5     | Power Strike    |
| Mage    | 80     | 8        | 20    | Fireball        |
| Rogue   | 90     | 12       | 10    | Sneak Attack    |

## 🎮 Core Functionality

### **All Characters Must Have:**
- `attack(target)` - Basic attack method
- `take_damage(damage)` - Reduce health
- `display_stats()` - Print character information

### **Players Additionally Have:**
- `character_class` attribute (like "Warrior", "Mage")
- `level` and `experience` attributes
- Enhanced `display_stats()` that shows player info

### **Special Abilities (Each Class):**
- **Warrior**: `power_strike(target)` - High damage attack
- **Mage**: `fireball(target)` - Magic damage attack
- **Rogue**: `sneak_attack(target)` - Critical hit attack

### **Weapons (Composition):**
- `Weapon(name, damage_bonus)` - Characters can HAVE weapons
- `display_info()` - Show weapon information

## ✅ Testing Your Code

### **Local Testing**
```bash
# Run all tests
python -m pytest tests/ -v

# Run specific test categories
python -m pytest tests/test_inheritance.py -v
python -m pytest tests/test_method_overriding.py -v
python -m pytest tests/test_special_abilities.py -v

# Test your main program
python project2_starter.py
```

### **GitHub Testing**

After pushing your code, check the **Actions** tab to see automated test results:

- ✅ **Inheritance Tests** (20 points) - Class structure and inheritance chain
- ✅ **Method Overriding Tests** (20 points) - Polymorphism and customized methods
- ✅ **Special Abilities Tests** (15 points) - Character abilities and composition

## 🎮 Example Usage

Your program should work like this:

```python
# Create characters (inheritance)
warrior = Warrior("Marcus")
mage = Mage("Aria")  
rogue = Rogue("Shadow")

# Polymorphism - same method, different behavior
for character in [warrior, mage, rogue]:
    character.attack(target)  # Each attacks differently

# Special abilities
warrior.power_strike(enemy)
mage.fireball(enemy)
rogue.sneak_attack(enemy)

# Composition
sword = Weapon("Iron Sword", 15)
sword.display_info()

# Test battle system (provided for you)
battle = SimpleBattle(warrior, mage)
battle.fight()
```

## 🎲 SimpleBattle System (Provided)

You have a **SimpleBattle** class already written that you can use to test your characters:

```python
battle = SimpleBattle(character1, character2)
battle.fight()  # Simulates a simple battle
```

**⚠️ DO NOT MODIFY the SimpleBattle class** - it's provided for testing your implementations.

## ⚠️ Important Notes

### **Protected Files**
- **DO NOT MODIFY** files in the `tests/` directory
- **DO NOT MODIFY** the `SimpleBattle` class
- Modifying protected files will result in automatic academic integrity violation

### **AI Usage Policy**
- ✅ **Allowed**: AI assistance for implementation, debugging, learning
- 📝 **Required**: Document AI usage in code comments
- 🎯 **Must be able to explain**: Every class and method during interview

## 🏆 Grading

- **Inheritance Tests (20%)**: Proper 3-level inheritance chain
- **Method Overriding (20%)**: Polymorphism and customized behaviors
- **Special Abilities (15%)**: Character-specific methods and composition
- **Code Quality (5%)**: Professional comments and documentation
- **Interview (40%)**: Code explanation and live coding

## 🎨 Bonus Creative Elements

Feel free to add your own creative touches for bonus points:
- Additional character classes beyond the three required
- More weapon types with different properties
- Enhanced special abilities with unique effects
