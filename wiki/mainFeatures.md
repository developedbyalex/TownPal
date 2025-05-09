# TownPal Plugin Ideas

A plugin designed to enhance town management and interaction in Minecraft servers. All features listed below will be **toggleable** through configuration settings.

## 📦 Core Features

### 🧱 Chunk-Based Claiming and Ownership
- Towns can claim chunks using a command (/t claim)
- Only members of a town can build or interact within claimed chunks.
- Admins can override, edit or delete claims.
- Mayors will gain x amount of claim chunks per hour

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

### 🧰 Town Shared Inventory
- Command: `/town inv`
- Opens a shared double chest inventory accessible by all town members.
- Optionally configurable permissions for who can view, add, or remove items.
- Data stored persistently to avoid loss on server restart.

### 🤝 Alliances and Enemies
- Towns can ally or enemy other towns.
- Shared town chat between allies (optional).
- PvP enabled between enemies (configurable).
- Special benefits for allies (e.g., shared warp access).

### 🏰 Town Roles and Permissions
- Customizable town roles (Mayor, Officer, Member, etc.).
- GUI or command-based role management.
- Fine-grained permission settings for bank, claims, upgrades, etc.

### 🏡 Town Homes
- Set town home with `/town sethome`.
- Members can teleport with `/town home`.

---

## 📜 Commands and Permissions

> 💡 **Note:** An available alias for `/town` is `/t`.

| Command                  | Description                                  | Permission Node           |
|--------------------------|----------------------------------------------|----------------------------|
| `/town create <name>`    | Create a new town                            | `townpal.create`           |
| `/town disband`          | Disband your town                            | `townpal.disband`          |
| `/town invite <player>`  | Invite a player to your town                 | `townpal.invite`           |
| `/town join <name>`      | Join a town you've been invited to           | `townpal.join`             |
| `/town leave`            | Leave your current town                      | `townpal.leave`            |
| `/town claim`            | Claim the chunk you're standing in           | `townpal.claim`            |
| `/town unclaim`          | Unclaim the current chunk                    | `townpal.unclaim`          |
| `/town sethome`          | Set the town’s home                          | `townpal.sethome`          |
| `/town home`             | Teleport to your town home                   | `townpal.home`             |
| `/town chat`             | Toggle or send a message in town chat        | `townpal.chat`             |
| `/town bank`             | Open the town bank GUI                       | `townpal.bank`             |
| `/town deposit <amt>`    | Deposit money into the town bank             | `townpal.bank.deposit`     |
| `/town withdraw <amt>`   | Withdraw money from the town bank            | `townpal.bank.withdraw`    |
| `/town upgrade`          | Open the upgrade GUI                         | `townpal.upgrade`          |
| `/town info`             | View town info                               | `townpal.info`             |
| `/town inv`              | Open the shared inventory                    | `townpal.inv`              |
| `/town ally <town>`      | Ally with another town                       | `townpal.ally`             |
| `/town enemy <town>`     | Mark another town as enemy                   | `townpal.enemy`            |
| `/town promote <player>` | Promote a member’s role                      | `townpal.promote`          |
| `/town demote <player>`  | Demote a member’s role                       | `townpal.demote`           |
| `/town kick <player>`    | Remove a player from your town               | `townpal.kick`             |
| `/town war declare <town>`  | Declare war on another town.                                  | `/t war declare`  |
| `/town war truce <town>`    | Declare a truce with a town, ending the war early.            | `/t war truce`    |
| `/town war surrender`       | Surrender to an enemy town, ending the war immediately.       | `/t war giveup`   |
| `/town war status`          | Check the current status of an ongoing war.                   | `/t war status`   |
| `/town war timeleft`        | View how much time is left before the war ends.               | `/t war timeleft` |

## 🔧 Admin Commands

| Command                                  | Description                                                                 | Permission Node              |
|------------------------------------------|-----------------------------------------------------------------------------|------------------------------|
| `/town admin claim <town>`               | Force claim the current chunk for a specified town                          | `townpal.admin.claim`        |
| `/town admin unclaim`                    | Force unclaim the current chunk                                             | `townpal.admin.unclaim`      |
| `/town admin delete <town>`              | Delete a town instantly                                                     | `townpal.admin.delete`       |
| `/town admin setbank <town> <amount>`    | Set a town’s bank balance                                                   | `townpal.admin.setbank`      |
| `/town admin setlevel <town> <level>`    | Set a town’s upgrade level                                                  | `townpal.admin.setlevel`     |
| `/town admin sethome <town>`             | Set a specific town’s home to the current location                          | `townpal.admin.sethome`      |
| `/town admin setname <town> <name>`      | Set a town's name                                                           | `townpal.admin.setname`      |
| `/town admin info <town>`                | View full info about any town                                               | `townpal.admin.info`         |
| `/town admin inv <town>`                 | Open a town’s shared inventory                                              | `townpal.admin.inv`          |
| `/town admin resetupkeep <town>`         | Reset or clear a town’s unpaid upkeep status                                | `townpal.admin.resetupkeep`  |
| `/town admin forcejoin <player> <town>`  | Force a player to join a town                                               | `townpal.admin.forcejoin`    |
| `/town admin forceleave <player>`        | Force a player to leave their current town                                  | `townpal.admin.forceleave`   |
| `/town admin promote <player>`           | Promote a player regardless of role restrictions                            | `townpal.admin.promote`      |
| `/town admin demote <player>`            | Demote a player regardless of role restrictions                             | `townpal.admin.demote`       |
| `/town reload`                     | Reload the plugin and all configurations                                    | `townpal.admin.reload`       |
| `/town war forceend <town>`    | Force the end of the war with a specific town.                    | `/t war forceend`    |

## ⛔ Placeholders

These placeholders are compatible with **PlaceholderAPI**.

| Placeholder                    | Description                                                  | Example Output              |
|----------------------------------|--------------------------------------------------------------|-----------------------------|
| `%town_townname%`                   | The name of the town                                          | `StoneHaven`                |
| `%town_owner%`                  | The owner of the town (mayor)                                 | `Kommandant`                |
| `%town_members%`                | List of members in the town                                   | `Kommandant, Player123, Alex`|
| `%town_balance%`                | The current balance in the town's bank                        | `1000`                      |
| `%town_claims%`                 | Number of chunks claimed by the town                          | `5`                         |
| `%town_available_claims%`                 | Number of chunks can be claimed by the town                          | `15`        |
| `%town_members_online%`         | Number of members currently online in the town                | `3`                         |
| `%town_members_max%`            | The maximum number of members allowed in the town             | `50`                        |
| `%town_members_offline%`        | Number of members currently offline in the town               | `47`                        |
