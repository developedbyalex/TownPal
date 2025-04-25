# Chunk Claiming System - TownPal Plugin

The **Chunk Claiming System** is a core feature of TownPal that allows towns to establish and maintain their territory through Minecraft's chunk system. This document explains how chunk claiming works and the various mechanics involved.

## 📋 Basic Concepts

### Claiming Process
- Towns can claim chunks using the command `/town claim` or `/t claim`
- Claims can be unclaimed via `/t unclaim`
- Only the chunk the player is standing in can be claimed

## 🕒 Passive Claim Generation

### How It Works
- Mayors automatically receive new claim slots over time
- These slots represent the number of chunks that can be claimed
- The generation is continuous as long as the town exists
- This encourages active town management and organic growth

### Claim Generation Details
- Each hour, mayors receive additional claim slots
- These slots stack up if not used immediately
- The maximum number of available claims can be viewed using the placeholder `%town_available_claims%`
- Current claimed chunks can be viewed using `%town_claims%`

## 🛡️ Claim Protection

### What's Protected?
- Building and breaking blocks
- Interacting with:
  - Containers (chests, furnaces, etc.)
  - Doors and gates
  - Redstone mechanisms
  - Farm areas (crops, animals)

### Who Can Build?
1. **Town Members**: Full access within their town's claims

## ⚠️ Claim Management

### Maintaining Claims
- Claims require upkeep payment to maintain
- Failing to pay upkeep may result in losing claims
- Lost claims become unclaimed and available for other towns