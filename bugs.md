# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---

### 1. `/town create` should require a `<name>` argument  
Currently, the command can be run without specifying a town name.

---

### 2. Currency formatting does not include commas and shows `.00`  
Currency values should be displayed like `$1,000` instead of `$1000.00`.

---

### 3. TownChat does not change the chat format  
Enabling TownChat does not visibly alter how messages appear.

---

### 4. Messages disappear when using `/town changechat town`  
After switching to town chat mode, messages typed do not appear in chat.

---

### 5. Players can deposit money into the bank without having sufficient funds  
Deposits succeed even if the player has a balance of $0.

---

### 6. `/t` command randomly displays "Target is offline"  
Running `/t` without arguments sometimes returns “Target is offline” unexpectedly.

---

### 7. `/town disband` says "Town has been disbanded" but also shows "An error occurred"  
The command executes, but an error message appears even though the town is removed.

---

### 8. `/town invite` lists selectors like `@a`, `@e`, `@p`, `@r`  
Only real online players should be shown in the invite list.

---

### 9. `/town sethome` teleports to wrong position  
It sets the location, but teleports the player to the lower corner of the block. It should preserve the player’s exact location and facing direction.

---

### 10. Town warps are missing from the upgrades menu  
There’s no option to view or manage town warps through the in-game upgrades menu.

---

# 🌟 Feature Suggestions

---

### A. `/town view` command to show claimed chunks with particles  
Would help visualize chunk borders claimed by the town.

---

### B. Show messages when entering or leaving claimed land  
Add a message like "Now entering [TownName]" or "Leaving [TownName]" for better immersion.
