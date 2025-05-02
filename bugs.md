# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---

### 1. Balance is still not formatted in /town upgrade  
Currency should be formatted with commas (e.g., `$1,000`, `$10,000`) and without `.00`.

---

### 2. `/town chat` should show an optional message  
Allow sending a message directly using `/town chat [message]`. Also when just typing /town chat it returns an error occured. It should show the usage instead.

---

### 3. Can you change /town changechat all to /town changechat global 
Replace all with global

---

### 4. `/town togglechat` returns "ta" before any message.
![image](https://github.com/user-attachments/assets/2a50dcc4-ad04-4cc5-b35f-c691b37dd902)

---

### 5. Block break denial message for outsiders  
If a non-member tries to break blocks in a town, it should show a message like:  
`%prefix% You are unable to break in %townName%`

---

### 6. `/town admin unclaim [town]` doesn't give the town their max amount of claims back  
If an admin unclaims a chunk of a town, it should give the town the chunk back so they don't lose out on claims.

---

### 7. `/town admin promote` lacks feedback  
This command needs confirmation messages to indicate the action was successful.

---

### 8. `/town disband` gives and error occured while executing this command
It doesn't disband the town either even though it does say it did
![image](https://github.com/user-attachments/assets/337854ff-bcc7-4d4e-90b6-40bd32273844)

---
