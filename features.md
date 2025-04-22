# TownPal Plugin Ideas

A plugin designed to enhance town management and interaction in Minecraft servers. All features listed below will be **toggleable** through configuration settings.

## 📦 Core Features

### 🧱 Chunk-Based Claiming and Ownership
- Towns can claim chunks using a command or GUI.
- Only members of a town can build or interact within claimed chunks.
- Admins can override or edit claims.

### 🏦 Town Bank (GUI-Based)
- GUI interface for depositing and withdrawing currency.
- Shared town balance used for upkeep, upgrades, and purchases.
- Permissions for who can access and manage the town bank.

### 💬 Town Chat
- Private chat channel for each town.
- Accessible with `/town chat`, `/t chat`, or toggle mode.
- Option to show prefix like `[TownChat]` for clarity.

### 📈 Town Upgrades
- Upgrade town features like:
  - Max members
  - Claim size
  - Bank capacity
  - Passive income or resource boosts
- GUI for upgrade purchasing using bank balance or resources.

### 🔧 Upkeep System
- Daily/weekly upkeep costs (currency or items).
- Payment pulled automatically from the town bank or town chest.
- Notifications when upkeep is due or unpaid.
- Grace period and consequences for missed payments (e.g., losing claims).

---

### 🧰 Town Shared Inventory
- Command: `/town inv`
- Opens a shared double chest inventory accessible by all town members.
- Optionally configurable permissions for who can view, add, or remove items.
- Data stored persistently to avoid loss on server restart.

---

### 🤝 Alliances and Enemies
- Towns can ally or enemy other towns.
- Shared town chat between allies (optional).
- PvP enabled between enemies (configurable).
- Special benefits for allies (e.g., shared warp access).
  
---

### 🏰 Town Roles and Permissions
- Customizable town roles (Mayor, Officer, Member, etc.).
- GUI or command-based role management.
- Fine-grained permission settings for bank, claims, upgrades, etc.

---

### 🏡 Town Homes
- Set town home with `/town sethome`.
- Members can teleport with `/town home`.

---
