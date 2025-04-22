# TownPal Plugin - Role Management System

The **TownPal plugin** provides a comprehensive **role management system** for town-based gameplay in Minecraft. The roles and their permissions are predefined and cannot be edited by players, ensuring a secure and structured environment for town management. Below is an overview of how role management works in the plugin.

## 🎮 Predefined Role Permissions

Each role in TownPal has a **fixed set of permissions** that define what players can and cannot do within the town. These permissions are **predefined** in the plugin's settings and cannot be modified by players, except through the server configuration.

### 1. **Role Permissions Overview**

#### **Mayor**
- Full control over the town.
- Can **promote/demote** players (e.g., from Member to Officer).
- Can **set town home** and manage **town settings**.
- Can manage **town upgrades**.
- Can access the **town bank**.

#### **Officer**
- Can **promote/demote** players within the town (but only to/from Member).
- Can manage **town upgrades** and **chunk claims**.

#### **Member**
- Can access **town chat**, **town home**, and **town shared inventory**.
- Can build, break etc within the towns claim
- Can withdraw and add money into the towns bank

### 3. **Role Management Commands (Restricted to Mayor and Officers)**

#### **Commands for Role Management:**
- **/town role promote [player] [new_role]**
  - The **Mayor** or **Officer** can promote a player to a higher role (e.g., Member to Officer).
  
- **/town role demote [player] [new_role]**
  - The **Mayor** or **Officer** can demote a player to a lower role (e.g., Officer to Member).
  
- **/town role set [player] [role]**
  - Directly sets a player’s role to a specific role (this would bypass the promotion/demotion system).

The **Mayor** will only have the option to manage the **promotion/demotion** of players. The permissions of each role will be fixed and clearly displayed in the GUI, with no option to modify them.
