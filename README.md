<h1 align="center">🎮 UNO LAN MULTIPLAYER 🎮</h1>

<p align="center">
  <b>Real-Time Client–Server Card Game using TCP/IP Sockets</b>
</p>

Course project for **NT106 – Application Programming over Networks** at the **University of Information Technology (UIT)**.

A desktop multiplayer implementation of the classic **UNO card game** built with **C#**, **Windows Forms**, and **TCP/IP socket programming**.

The project adopts a **multi-threaded client–server architecture**, enabling **2–4 players** to compete over a Local Area Network (LAN) while ensuring **real-time communication**, **server-authoritative game synchronization**, and **strict rule validation**.

---

# Features

- Real-time multiplayer UNO gameplay
- TCP/IP Socket communication
- Windows Forms desktop application
- Dynamic lobby (2–4 players)
- Multi-threaded server architecture
- Complete UNO game mechanics
- Real-time game state synchronization
- Server-side rule validation
- Automatic packet broadcasting

---

# System Architecture

```text
                           +-------------------------------+
                           |      UNO Client (Player 1)    |
                           +-------------------------------+
                                      │
                           +-------------------------------+
                           |      UNO Client (Player 2)    |
                           +-------------------------------+
                                      │
                           +-------------------------------+
                           |      UNO Client (Player 3)    |
                           +-------------------------------+
                                      │
                           +-------------------------------+
                           |      UNO Client (Player 4)    |
                           +-------------------------------+
                                      │
                              TCP/IP Socket Network
                                      │
                                      ▼
+-----------------------------------------------------------------------+
|                     Multi-threaded UNO Server                          |
|-----------------------------------------------------------------------|
|  • TCP Socket Listener                                                 |
|  • Lobby & Player Management                                           |
|  • Game Engine                                                         |
|  • Deck Shuffle                                                        |
|  • Turn Controller                                                     |
|  • Rule Validation                                                     |
|  • Packet Dispatcher                                                   |
|  • State Synchronization                                               |
|  • Broadcast Manager                                                   |
+-----------------------------------------------------------------------+
```

---

# Gameplay Flow

```text
Client Connect
      │
      ▼
Join Lobby
      │
      ▼
Waiting for Players
      │
      ▼
Start Match
      │
      ▼
Shuffle Deck
      │
      ▼
Distribute Cards
      │
      ▼
Game Loop
      │
      ├── Receive Player Action
      ├── Validate Move
      ├── Update Game State
      ├── Broadcast New State
      └── Next Turn
      │
      ▼
Winner Detected
      │
      ▼
End Game
```

---

# Supported UNO Rules

The game implements the complete core UNO rule set, including:

### Number Cards

- 0–9
- Four colors (Red, Yellow, Green, Blue)

### Action Cards

- Skip
- Reverse
- Draw Two
- Wild
- Wild Draw Four

Additional mechanics include:

- Turn rotation
- Reverse direction
- Forced card drawing
- Wild color selection
- Winner detection
- Illegal move prevention

---

# Networking

The networking layer is implemented using **System.Net.Sockets**.

Main capabilities include:

- TCP Socket Communication
- Client–Server Architecture
- Multi-threaded Connection Handling
- Custom Packet Protocol
- Server-side Validation
- Broadcast Synchronization
- Graceful Client Disconnect

---

# State Synchronization

The server acts as the single source of truth for the game.

Every player action is processed exclusively by the server before being synchronized to all connected clients.

The synchronized game state includes:

- Current turn
- Active card
- Active color
- Player hand sizes
- Draw pile
- Discard pile
- Match status
- Winner information

This approach guarantees consistency across all connected clients and prevents unauthorized or invalid actions.

---

# Technology Stack

| Category | Technology |
|-----------|------------|
| Language | C# |
| Framework | .NET Framework |
| GUI | Windows Forms |
| Networking | TCP/IP (System.Net.Sockets) |
| Concurrency | Multi-threading |
| IDE | Visual Studio 2022 |
| Version Control | Git & GitHub |

---

# Technical Highlights

Multi-threaded TCP Socket Server
Real-time Multiplayer Communication
Custom Client–Server Protocol
Server-authoritative Game Logic
Thread-safe Windows Forms Updates
Dynamic Lobby Management
Automatic State Synchronization
Complete UNO Rule Enforcement

---

## 👨‍💻 Project Team

* **Hong Bich Nhu** - UNO Game Logic, Windows Forms UI, Gameplay Flow, Client–Server Architecture
* **Nguyen Thi Huynh Nhu** - Client–Server Architecture, TCP Socket Communication, Network Protocol
