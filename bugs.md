# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

---

### 1. `/t admin delete <townName>` doesn't work. 
```
[22:44:30 INFO]: Rooftop issued server command: /t admin delete test
[22:44:31 WARN]: [TownPal] Plugin TownPal vfinal generated an exception while executing task 212
java.lang.RuntimeException: failed to remove town from database
        at townpal-plugin-1.0-SNAPSHOT-all (1).jar/ru.rusekh.townpal.town.TownRepository.deleteTown(TownRepository.java:99) ~[townpal-plugin-1.0-SNAPSHOT-all (1).jar:?]
        at townpal-plugin-1.0-SNAPSHOT-all (1).jar/ru.rusekh.townpal.command.TownCommand.lambda$adminDelete$4(TownCommand.java:1567) ~[townpal-plugin-1.0-SNAPSHOT-all (1).jar:?]
        at org.bukkit.craftbukkit.scheduler.CraftTask.run(CraftTask.java:78) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at org.bukkit.craftbukkit.scheduler.CraftAsyncTask.run(CraftAsyncTask.java:57) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at com.destroystokyo.paper.ServerSchedulerReportingWrapper.run(ServerSchedulerReportingWrapper.java:22) ~[paper-1.21.4.jar:?]
        at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1144) ~[?:?]
        at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:642) ~[?:?]
        at java.base/java.lang.Thread.run(Thread.java:1583) ~[?:?]
```

It does give a successful deletion messsage, yet if I try do another command like `/t create <name>` it still says I am in a town. 

### 2. `/t sethome` changes
You must not be able to:
Set a town home in another town's claim
Set a town home if the land isn't claimed
