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
Running `/t` without arguments sometimes returns “Target is offline” unexpectedly. Should return something like Unkown command or a help message
