# UBDS Manager v2.0.0
## Universal Bedrock Dedicated Server (Plugin Support)

**Version**: 2.0.0  

---

## 🎯 What is UBDS?

UBDS enables you to run Minecraft Bedrock servers on all operating systems, launching from JAR files like Minecraft Java Edition servers. You can simultaneously launch and manage standalone systems by placing them in the plugins folder.

### What it can do:
- ✅ Launch Minecraft Bedrock server on Windows, Mac, Linux
- ✅ Simultaneous management of Java standalone programs

---

## 📥 Getting Started

### Requirements:
- **Java 17 or later**
- **Computer** - Windows, Mac, or Linux (CLI support)

### Quick Setup:
1. Download UBDS from releases
2. Place in a folder (e.g., "MinecraftServer")
3. Run: java -jar Universal-BDS-2.0.0.jar

---

## 📂 File Structure

When you run UBDS Manager, the following folders will be created:

    MinecraftServer/
    ├── Universal-BDS-2.0.0.jar     # UBDS
    ├── server.properties      # Server settings (port, world name, etc.)
    ├── plugins/               # Place plugin JAR files here
    │   ├── MyBot/            # Each plugin gets its own folder
    │   │   ├── MyBot.jar     # Plugin file
    │   │   └── config.yml    # Plugin settings
    │   └── ChatManager/
    │       └── ChatManager.jar
    ├── logs/                  # All logs saved here
    │   ├── latest.log         # Today's log
    │   └── old logs...
    └── worlds/                # Minecraft world data
        └── Bedrock level/

---

## 🎮 How to Use

### Starting the server:
1. Launch Universal-BDS-2.0.0.jar
2. Wait for the server to start
3. Minecraft server is now running!
4. Players can connect to your IP address

### Basic Commands:

#### Server Management (start with !):
    !status     # Check server status
    !info       # Show computer information
    !plugins    # Show plugin list
    !stop       # Stop server and exit program
    !help       # Show all commands

#### Send commands to plugins (start with @):
    @PluginName command

Examples:
    @MyBot help           # Ask MyBot plugin for help
    @ChatManager reload   # Restart ChatManager plugin

#### Minecraft Server Commands (type normally):
    say Hello everyone!   # Send message to all players
    list                  # Show online players
    gamemode creative Steve  # Change Steve to creative mode
    time set day         # Set time to day

---

## 🔌 Adding Plugins

### Step 1: Get a plugin
- Download a JAR file (e.g., "MyBot.jar")
- Must work as standalone only

### Step 2: Install
- Place JAR file in "plugins" folder
- Example: Copy "MyBot.jar" to "plugins/MyBot.jar"

### Step 3: Server restart
- Plugin will start automatically
- If errors occur, restart twice

### Step 4: Start using
- Type: @MyBot help
- Each plugin has different available commands

---

## 🔧 Common Settings

### Change server settings:
Edit "server.properties" file:

    server-name=My Awesome Server    # Server name
    gamemode=survival               # Default game mode
    difficulty=easy                 # Difficulty level
    max-players=20                  # Maximum players
    server-port=19132              # Port number (change if needed)

### Change plugin settings:
Each plugin has settings files in its dedicated folder:
- MyBot plugin: "plugins/MyBot/config.yml"
- ChatManager: "plugins/ChatManager/settings.json"

---

## ❓ Troubleshooting

### Problem: Server won't start
**Solution:**
1. Check if port 19132 is available
2. Check for errors
3. Type !info to check system information

### Problem: Plugin not working
**Solution:**
1. Type !plugins to check if it's running
2. Check if Java is installed: java -version
3. Check logs in "logs/latest.log"

### Problem: Can't connect to server
**Solution:**
1. Check server.properties for correct port
2. Check if firewall allows the port
3. Give friends your IP address and port number

### Problem: Server running slow
**Solution:**
1. Close unnecessary programs
2. Remove unused plugins
3. Reduce max-players in server.properties

---

## 📋 Quick Reference

### Command Types:
- **!command** = Server program management
- **@plugin command** = Communicate with specific plugin
- **normal command** = Send to Minecraft server

### Commonly used commands:
    !status          # Check if everything is working normally
    !plugins         # Check running plugins
    say Hello!       # Talk to all players
    list             # Check online players

---

## 📞 Support

**Creator**: ZSHARE  
**Version**: 2.0.0  

**When seeking help, please include:**
- Operating System (Windows, Mac, Linux)
- Error messages from latest.log
- What you were trying to do
- Please visit https://discord.zpw.jp for questions

---
