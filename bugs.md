# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---

### 1. Actionbar message randomly flashing in `/t view`  
When running the `/t view` command, the actionbar message flickers inconsistently.

---

### 2. Enemy notification message wording  
Instead of:  
`Town <town> is now enemy with town <town>`  
Use:  
`Your town is now enemies with <enemyTown>`

---

### 3. Can add money to the town bank without having any  
Players can deposit money into the town bank even if their personal balance is zero.

---

### 4. `/t view` should show all claims  
- The command should display **all player claims**, not just your own.  
- Claims in the **Dust** biome should be highlighted in **red**.

---

### 5. PvP should be disabled in claims unless towns are enemies  
PvP currently works in all claims. It should be disabled unless the attacker and defender are from enemy towns.
