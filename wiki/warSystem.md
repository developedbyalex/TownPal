# War System - TownPal Plugin

The War System in the TownPal plugin allows towns to engage in PvP conflicts with each other. Wars can be triggered automatically when towns become enemies (configurable) or declared manually.

## Features:

### 1. **War Declaration**
- Wars can be triggered in two ways:
  - Automatically when towns become enemies (if `automaticWarOnEnemy` is enabled in config)
  - Manually using war commands
- Players can freely PvP in each other's claimed areas during war

### 2. **War Duration**
- By default, wars last for 24 hours (configurable in settings)
- Wars can be set to unlimited duration by setting `warDuration` to -1 in config
- Wars end when the duration expires, one side surrenders, or a truce is called

### 3. **Truce and Surrender**
- Towns can end a war before the duration expires by declaring a truce or surrendering
- **Truce**: A mutual agreement between towns to stop fighting
- **Surrender**: A town may choose to surrender, ending the war immediately

### 4. **Enemy Alerts**
- Towns receive alerts when enemy players enter their claims
- Alert system is configurable with customizable cooldowns and messages

## War Commands:

- `/town war declare <town>`: Manually declare war on another town
- `/town war truce <town>`: Propose a truce to end the war
- `/town war surrender`: Surrender to the enemy town
- `/town war status`: Check current war status
- `/town war timeleft`: View remaining war duration

## War Mechanics:

- **PvP**: Players from towns at war can freely PvP within each other's claimed territories
- **End Conditions**: Wars can end through duration expiry, truce, or surrender
- **Notifications**: All town members are notified of war declarations and status changes
