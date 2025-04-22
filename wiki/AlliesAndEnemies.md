# Allies and Enemies - TownPal Plugin

The **Allies and Enemies** system in the **TownPal** plugin allows towns to form alliances or declare war on each other. 

## Key Features

### 1. **Alliances**

- **Form Alliances**: Towns can ally with one another, this just shows they're friends.

### 2. **Enemies**

- **Declare War**: Towns can declare other towns as enemies. By default, this automatically triggers a war between the towns (configurable in settings).
- **War System**: When towns become enemies, they enter into a war state that enables PvP between town members. See the War System documentation for more details.
  
### 3. **Manage Alliances and Enemies**

- **Commands for Managing Alliances/Enemies**:
  - `/town ally [town_name]`: Send a request to ally with another town.
  - `/town unally [town_name]`: Remove an alliance with a town.
  - `/town enemy [town_name]`: Declare a town as an enemy (may trigger war automatically).
  - `/town unenemy [town_name]`: Remove enemy status with a town.
  - `/town allies`: List all allied towns.
  - `/town enemies`: List all enemy towns.
  
### 4. **Permissions for Alliances/Enemies**

- **Who Can Manage Alliances and Enemies?**
  - **Mayor**: Can send and accept alliance requests, declare enemies, and manage existing alliances and enemies.
  - **Officer**: Can manage alliances and enemies as part of their standard permissions.
  - **Member**: Cannot manage alliances or enemies but can view alliance/enemy status.
