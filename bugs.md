# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---
### 1. `/t view` should show all claims  
- The command should display **all player claims**, not just your own.  
- Enemy claims should be red dust
- Your own claim should be green dust
- Ally claims should be blue dust
- This should all be configurable in the config.yml

### 2. Kicked when using `/t bank`
If I withdraw or add money in /t bank I get:
![image](https://github.com/user-attachments/assets/67c9c723-931d-4f88-aa34-da5e9adf8b5c)

### 3. How to handle town enemies
If a town enemies another town, make sure that they are both listed as each others enemies. The other town should be able to surrender too.
The message also needs to be changed from "Surrenered war with Town <town>" to `<townName> has surrended against <otherTownName>` dont show that to the user who types the command. To the town that types the command show: `You have surrended the war with <townName>`

### 4. Usage on commands
Show usages like this for all commands
![image](https://github.com/user-attachments/assets/b9a98a71-e68a-4500-a0f8-07b178be9fa4)
