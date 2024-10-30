- 👋 Hi, I’m @adhamalghryani
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
import random

class Fighter:
    def __init__(self, name, health, attack_min, attack_max):
        self.name = name
        self.health = health
        self.attack_min = attack_min
        self.attack_max = attack_max

    def attack(self):
        return random.randint(self.attack_min, self.attack_max)

    def take_damage(self, damage):
        self.health -= damage
        return self.health > 0

def battle(fighter1, fighter2):
    print(f"{fighter1.name} vs {fighter2.name} - Let the battle begin!")
    while fighter1.health > 0 and fighter2.health > 0:
        damage = fighter1.attack()
        if not fighter2.take_damage(damage):
            print(f"{fighter1.name} attacks {fighter2.name} for {damage} damage. {fighter2.name} has been defeated!")
            break
        else:
            print(f"{fighter1.name} attacks {fighter2.name} for {damage} damage. {fighter2.name} has {fighter2.health} health remaining.")

        damage = fighter2.attack()
        if not fighter1.take_damage(damage):
            print(f"{fighter2.name} attacks {fighter1.name} for {damage} damage. {fighter1.name} has been defeated!")
            break
        else:
            print(f"{fighter2.name} attacks {fighter1.name} for {damage} damage. {fighter1.name} has {fighter1.health} health remaining.")

if __name__ == "__main__":
    player = Fighter("Player", 100, 10, 20)
    computer = Fighter("Computer", 100, 5, 15)
    battle(player, computer)
<!---
adhamalghryani/adhamalghryani is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
