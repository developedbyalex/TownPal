# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---

### 1. No names are tab-completable in `/t invite`  
No player names appear when trying to tab-complete the invite command.

---

### 2. `/town promote` does not provide tab-completable ranks  
Ranks should appear when tab-completing the command.

---

### 3. Promoting or demoting a player does not notify town members  
There should be a broadcast message to all online town members when a user is promoted or demoted.

---

### 4. Balance is still not formatted  
Currency should be formatted with commas (e.g., `$1,000`, `$10,000`) and without `.00`.

---

### 5. `/town chat` should allow an optional message  
Allow sending a message directly using `/town chat [message]`.

---

### 6. `/town changechat` does not show tab-completable options  
All valid chat types should appear when tab-completing.

---

### 7. Commands only return "missing-arguments"  
Instead, show full usage information for the command.

---

### 8. Leaving a town does not notify other town members  
There should be a message broadcast to the town when a user `/t leaves`.

---

### 9. `/town inv` removes all items after they are added  
Items disappear from the inventory GUI after being placed.

---

### 10. Kicking a user does not notify the town or the kicked player  
There should be messages to all town members and the kicked player when this happens.

---

### 11. `/town togglechat` does not return the correct chat format  
Messages sent using town chat do not appear in the expected format.

---

### 12. Enemy is in your claim error  
This might be due to unclear documentation, but the message should only show if the towns are actually enemies.

---

### 13. Block break denial message for outsiders  
If a non-member tries to break blocks in a town, it should show a message like:  
`%prefix% You are unable to break in %townName%`

---

### 14. `/town admin unclaim [town]` does not unclaim current chunk  
The command should unclaim the chunk the executing user is standing in but currently does not.

---

### 15. `/town admin promote` lacks feedback  
This command needs confirmation messages to indicate the action was successful.
