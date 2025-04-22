# Allies and Enemies - TownPal Plugin

The **Allies and Enemies** system in the **TownPal** plugin allows towns to form alliances or declare war on each other. 

## Key Features

### 1. **Alliances**

- **Form Alliances**: Towns can ally with one another, this just shows they're friends.

### 2. **Enemies**

- **Declare War**: Towns can declare war on other towns, enabling PvP between the towns' members.
  
### 3. **Manage Alliances and Enemies**

- **Commands for Managing Alliances/Enemies**:
  - `/town ally [town_name]`: Send a request to ally with another town.
  - `/town unally [town_name]`: Remove an alliance with a town.
  - `/town enemy [town_name]`: Declare war on a town.
  - `/town unenemy [town_name]`: End the war with a town.
  - `/town allies`: List all allied towns.
  - `/town enemies`: List all enemy towns.
  
### 4. **Permissions for Alliances/Enemies**

- **Who Can Manage Alliances and Enemies?**
  - **Mayor**: Can send and accept alliance requests, declare war, and manage existing alliances and enemies.
  - **Officer**: Can manage alliances and enemies if given the right permissions.
  - **Member**: Cannot manage alliances or enemies but can view alliance/enemy status.
