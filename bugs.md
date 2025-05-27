# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---

### 1. `/t admin delete <townName` doesn't work. 
```
[19:25:39 INFO]: Rooftop issued server command: /t admin delete test
[19:25:39 WARN]: java.lang.RuntimeException: failed to remove town from database
[19:25:39 WARN]:        at townpal-plugin-1.0-SNAPSHOT-all.jar//ru.rusekh.townpal.town.TownRepository.deleteTown(TownRepository.java:99)
[19:25:39 WARN]:        at townpal-plugin-1.0-SNAPSHOT-all.jar//ru.rusekh.townpal.command.TownCommand.adminDelete(TownCommand.java:1557)
```

### 2. `/t admin promote ` needs feedback of the command
For example, if the admin tries to promote the user to mayor and the user is already mayor it should say that.

### 3. `/3 admin resetupkeep <town>` is incorrect
It says "successfully reset failed upkeep number"? This doesn't make sense, it's just meant to reset the timer...

### 4. `/t warp <warpName>` changes
You must not be able to:
Set a warp in another town's claim
Set a warp if the land isn't claimed

### 5. `/t sethome` changes
You must not be able to:
Set a town home in another town's claim
Set a town home if the land isn't claimed
