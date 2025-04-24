# 🧾 Upkeep System - TownPal Plugin

The **Upkeep System** in the TownPal plugin introduces a resource management challenge for towns, encouraging active participation and maintenance.

## 🔧 How It Works

- Each town must pay a set amount of currency at regular intervals.  
- Both the **upkeep cost** and **interval** (in hours) are configurable via the plugin’s `config.yml`.
- Payments are automatically taken from the **Town Bank**.
- If a town fails to pay the required upkeep:
  - The town’s claimed chunks will be **unclaimed**.
  - A log entry will be created detailing the time, the town name and the mayor of the town.

## 📜 Logging

- All unclaim events triggered by unpaid upkeep will be saved to a log file.
- This ensures server administrators can track which towns have lost land and why.
