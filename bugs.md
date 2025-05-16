# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---
### 1. The `/t view` command doesn't show the entire chunk.
It only shows the side of the chunk you're looking at.

### 2. If a user leaves and /t view is on then it stops it being shown for everyone
Title.

### 3. If you're not using CMI, you still get kicked.
- When using normal Vault, it still kicks you unexpectedly.
- ![image](https://github.com/user-attachments/assets/b640e508-9278-4122-b605-15278edb2751)


### 4.Particle reload issue
- Changing the particle effect for `/t view` and then reloading does not seem to apply the change (all the time).

### 5. Town name validation
- Town names currently allow spaces.
- Need to enforce a rule so town names **cannot** have spaces.

### 6. Ally land claim view color bug
- When land is claimed with an ally, their view color is correct initially.
- However, when standing in the claimed land, the view color changes incorrectly.
- View discord to see it
