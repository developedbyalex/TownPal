# Town Chat System - TownPal Plugin

The **Town Chat** system in TownPal provides a private communication channel for town members to communicate with each other. This feature enhances town coordination and community building by allowing members to chat privately within their town.

## 📝 Basic Features

### Chat Commands
- `/town chat` or `/t chat` - Toggle town chat mode
- `/t chat <message>` - Send a single message to town chat without toggling

### Chat Format
The default chat format is:
```
[TownChat] (Role) Player: Message
```
- Roles are color-coded based on the sender's role
- Role colors are customizable in the configuration
- The format can be customized in the configuration

### Format Variables
- `%role%` - The player's role in the town
- `%player%` - The player's name
- `%message%` - The chat message

## 💡 Tips for Using Town Chat

1. **Toggle Mode**
   - Use toggle mode when having extended conversations
   - All your messages will go to town chat until you toggle it off
   - Toggle off when you want to return to global chat

2. **Quick Messages**
   - Use `/t chat <message>` for one-off messages
   - Useful when you need to send a quick message without changing chat modes

## 🔒 Privacy and Security

- Only town members can see and send messages in town chat
- Messages are not visible to players outside the town