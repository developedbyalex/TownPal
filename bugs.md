# 🐞 TownPal Plugin - Bugs

This file contains a list of known bugs found during testing of the TownPal plugin.

### 1. `/t view` particles
For the claims, if there isn't a claim and it's just the wilderness it should not show the particles. The particles should also go around the entire chunk, not just the edges.

### 2. `/t disband` doesn't do anything
/t disband doesn't do anything. It gives the success message and then the town still exists and the user is still in the town. Error:
```sh
[01:34:49 INFO]: Rooftop issued server command: /t disband
[01:34:50 WARN]: [TownPal] Plugin TownPal vfinal generated an exception while executing task 160
java.lang.RuntimeException: failed to remove town from database
        at townpal-plugin-1.0-SNAPSHOT-all (2).jar/ru.rusekh.townpal.town.TownRepository.deleteTown(TownRepository.java:99) ~[townpal-plugin-1.0-SNAPSHOT-all (2).jar:?]
        at townpal-plugin-1.0-SNAPSHOT-all (2).jar/ru.rusekh.townpal.command.TownCommand.lambda$disband$0(TownCommand.java:194) ~[townpal-plugin-1.0-SNAPSHOT-all (2).jar:?]
        at org.bukkit.craftbukkit.scheduler.CraftTask.run(CraftTask.java:78) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at org.bukkit.craftbukkit.scheduler.CraftAsyncTask.run(CraftAsyncTask.java:57) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at com.destroystokyo.paper.ServerSchedulerReportingWrapper.run(ServerSchedulerReportingWrapper.java:22) ~[paper-1.21.4.jar:?]
        at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1144) ~[?:?]
        at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:642) ~[?:?]
        at java.base/java.lang.Thread.run(Thread.java:1583) ~[?:?]
```

### 3. Error message when trying to enemy a clan
![image](https://github.com/user-attachments/assets/b90d79f1-eb2d-44af-b0b4-da7493a6e7b4)

### 4. `/t admin claim ` doesn't claim the chunk
title.

### 5. `/t admin delete <townName` doesn't work. 
```
[01:37:20 INFO]: Rooftop issued server command: /t admin delete EpicTown
[01:37:20 WARN]: java.lang.RuntimeException: failed to remove town from database
[01:37:20 WARN]:        at townpal-plugin-1.0-SNAPSHOT-all (2).jar//ru.rusekh.townpal.town.TownRepository.deleteTown(TownRepository.java:99)
[01:37:20 WARN]:        at townpal-plugin-1.0-SNAPSHOT-all (2).jar//ru.rusekh.townpal.command.TownCommand.adminDelete(TownCommand.java:1553)
> 
```

### 6. Issue when viewing another towns inv
```
[01:42:41 INFO]: Rooftop issued server command: /t admin inv lalaland
[01:42:41 WARN]: [TownPal] Plugin TownPal vfinal generated an exception while executing task 26
java.lang.NullPointerException: Cannot invoke "ru.rusekh.townpal.town.Town.setInventoryContents(org.bukkit.inventory.ItemStack[])" because "town" is null
        at townpal-plugin-1.0-SNAPSHOT-all (2).jar/ru.rusekh.townpal.task.TownInventoryUpdateTask.run(TownInventoryUpdateTask.java:22) ~[townpal-plugin-1.0-SNAPSHOT-all (2).jar:?]
        at org.bukkit.craftbukkit.scheduler.CraftTask.run(CraftTask.java:78) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at org.bukkit.craftbukkit.scheduler.CraftAsyncTask.run(CraftAsyncTask.java:57) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at com.destroystokyo.paper.ServerSchedulerReportingWrapper.run(ServerSchedulerReportingWrapper.java:22) ~[paper-1.21.4.jar:?]
        at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1144) ~[?:?]
        at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:642) ~[?:?]
        at java.base/java.lang.Thread.run(Thread.java:1583) ~[?:?]
[01:42:42 ERROR]: Could not pass event InventoryCloseEvent to TownPal vfinal
java.lang.NullPointerException: Cannot invoke "ru.rusekh.townpal.town.Town.setInventoryContents(org.bukkit.inventory.ItemStack[])" because "town" is null
        at townpal-plugin-1.0-SNAPSHOT-all (2).jar/ru.rusekh.townpal.inventory.TownInventoryListener.onInventoryClose(TownInventoryListener.java:27) ~[townpal-plugin-1.0-SNAPSHOT-all (2).jar:?]
        at co.aikar.timings.TimedEventExecutor.execute(TimedEventExecutor.java:80) ~[paper-api-1.21.4-R0.1-SNAPSHOT.jar:?]
        at org.bukkit.plugin.RegisteredListener.callEvent(RegisteredListener.java:70) ~[paper-api-1.21.4-R0.1-SNAPSHOT.jar:?]
        at io.papermc.paper.plugin.manager.PaperEventManager.callEvent(PaperEventManager.java:54) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at io.papermc.paper.plugin.manager.PaperPluginManagerImpl.callEvent(PaperPluginManagerImpl.java:131) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at org.bukkit.plugin.SimplePluginManager.callEvent(SimplePluginManager.java:628) ~[paper-api-1.21.4-R0.1-SNAPSHOT.jar:?]
        at org.bukkit.craftbukkit.event.CraftEventFactory.handleInventoryCloseEvent(CraftEventFactory.java:1653) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.network.ServerGamePacketListenerImpl.handleContainerClose(ServerGamePacketListenerImpl.java:2915) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.network.ServerGamePacketListenerImpl.handleContainerClose(ServerGamePacketListenerImpl.java:2907) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.network.protocol.game.ServerboundContainerClosePacket.handle(ServerboundContainerClosePacket.java:33) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.network.protocol.game.ServerboundContainerClosePacket.handle(ServerboundContainerClosePacket.java:8) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.network.protocol.PacketUtils.lambda$ensureRunningOnSameThread$0(PacketUtils.java:29) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.TickTask.run(TickTask.java:18) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.util.thread.BlockableEventLoop.doRunTask(BlockableEventLoop.java:155) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.util.thread.ReentrantBlockableEventLoop.doRunTask(ReentrantBlockableEventLoop.java:24) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.doRunTask(MinecraftServer.java:1448) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.doRunTask(MinecraftServer.java:176) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.util.thread.BlockableEventLoop.pollTask(BlockableEventLoop.java:129) ~[paper-1.21.4.jar:1.21.4-227-7675321]        at net.minecraft.server.MinecraftServer.pollTaskInternal(MinecraftServer.java:1428) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.pollTask(MinecraftServer.java:1422) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.util.thread.BlockableEventLoop.managedBlock(BlockableEventLoop.java:139) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.managedBlock(MinecraftServer.java:1379) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.waitUntilNextTick(MinecraftServer.java:1387) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.runServer(MinecraftServer.java:1264) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at net.minecraft.server.MinecraftServer.lambda$spin$2(MinecraftServer.java:310) ~[paper-1.21.4.jar:1.21.4-227-7675321]
        at java.base/java.lang.Thread.run(Thread.java:1583) ~[?:?]
> 
```

### 7. `/t admin promote ` needs feedback of the command
For example, if the admin tries to promote the user to mayor and the user is already mayor it should say that.

### 8. `/t resetupkeep <town>` doesn't do anything. no feedback either.

### 9. `/t admin unclaim <town>` doesn't work
It says "This chunk is not claimed by your town". That shouldn't matter if we're doing it with the admin command.

### 10. `/t warp <warpName>` displays a weird message
It says: Town with that name doesn't exist. Can you also make the warps tabable. 

---

## Cannot be tested atm:
### 2. If a user leaves and /t view is on then it stops it being shown for everyone
Title.
