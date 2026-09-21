<div align="center">

# 🌸 Yariko

### An Anime Game Discord Bot

[![Discord.js](https://img.shields.io/badge/Discord.js-v14-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.js.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-Unlicense-blue?style=for-the-badge)](LICENSE)

<br>

**🎴 Collect • 💰 Earn • 🛒 Shop • 🌸 Explore**

<br>

[Commands](#-commands) •
[Installation](#-installation) •
[Configuration](#-configuration) •
[Development](#-development) •
[Contributing](#-contributing)

</div>

---

# 🌸 About

**Yariko** is an anime-themed Discord game bot built with **Node.js** and **Discord.js**.

Yariko brings an anime game experience directly into Discord, featuring a character database, player profiles, inventory and economy systems, shops, events, daily rewards, voting, and more.

The project uses a local SQLite database for persistent data and stores character information in the `Dex` directory.

> ✨ **Your anime adventure starts here.**

---

# ✨ Features

### 🎴 Anime Character System

Explore Yariko's collection of anime characters through the built-in Dex system.

- Anime character database
- Character categories
- 1-star characters
- 4-star characters
- Genshin characters
- Promotional characters

### 💰 Economy

Yariko includes an in-game economy system.

- 💰 Balance
- 🎁 Daily rewards
- 🛒 Shop
- 🛍️ Item purchasing
- 🎒 Inventory

### 🌲 Exploration

Encounter and interact with characters through the game's exploration system.

- 🌲 Wild encounters
- 📖 Character Dex
- 🎉 Events

### 👤 Player System

Each player can have their own game profile and persistent data.

- Player profiles
- Inventory
- Balance
- Game progression

### 💬 Discord Integration

Built specifically for Discord using Discord.js.

- Slash commands
- Discord interactions
- Embeds
- Buttons and interactive components
- Persistent player data

---

# 📸 Screenshots

> Screenshots and GIFs can be added here once you have some gameplay captures.

### 🎮 Gameplay

<p align="center">
  <img src="assets/gameplay.gif" width="750" alt="Yariko gameplay">
</p>

### 🎴 Character System

<p align="center">
  <img src="assets/dex.png" width="750" alt="Yariko Dex">
</p>

### 🛒 Shop & Economy

<p align="center">
  <img src="assets/shop.png" width="750" alt="Yariko Shop">
</p>

> **Don't have screenshots yet?**
>
> You can remove these sections temporarily and add them once you have gameplay screenshots.

---

# 🎮 Commands

Yariko uses Discord **slash commands**.

There are currently **17 commands** in the `commands/` directory.

## 🌸 Player

| Command | Description |
|:---:|---|
| `/start` | Start your Yariko journey |
| `/profile` | View your player profile |
| `/balance` | View your current balance |
| `/inventory` | View your inventory |
| `/daily` | Claim your daily reward |
| `/dex` | Access the character Dex |
| `/wild` | Access the wild system |
| `/event` | Access the event system |

---

## 💰 Economy & Items

| Command | Description |
|:---:|---|
| `/shop` | View the available shop |
| `/buy` | Purchase items |
| `/itemsadd` | Add items |
| `/itemsdel` | Remove items |

---

## 🔗 Community

| Command | Description |
|:---:|---|
| `/vote` | Vote for Yariko |
| `/invite` | Get an invite link for Yariko |
| `/help` | View the available commands |

---

## 🛠️ Testing

| Command | Description |
|:---:|---|
| `/test` | Testing and development command |

> **Note:** Some commands may require specific permissions, arguments, or game conditions.

---

# 🗂️ Project Structure

```text
Yariko/
│
├── 📁 commands/
│   ├── balance.js
│   ├── buy.js
│   ├── daily.js
│   ├── dex.js
│   ├── event.js
│   ├── help.js
│   ├── inventory.js
│   ├── invite.js
│   ├── itemsadd.js
│   ├── itemsdel.js
│   ├── profile.js
│   ├── shop.js
│   ├── start.js
│   ├── test.js
│   ├── vote.js
│   └── wild.js
│
├── 📁 Dex/
│   ├── Anime.json
│   ├── 1-star.json
│   ├── 4-star.json
│   ├── Genshin.json
│   └── Promo.json
│
├── 📄 index.js
├── 📄 server.js
├── 💾 kekw.sqlite
├── 📄 package.json
├── 📄 package-lock.json
├── 📄 replit.nix
├── 📄 LICENSE
└── 📄 README.md
````

---

# ⚡ Installation

## 📋 Requirements

Before installing Yariko, make sure you have:

* [Node.js](https://nodejs.org/) installed
* [Git](https://git-scm.com/) installed
* A Discord account
* A Discord application
* A Discord bot
* Your Discord bot token

---

## 1. Clone the repository

```bash
git clone https://github.com/jzc9307/Yariko.git
```

Enter the project directory:

```bash
cd Yariko
```

---

## 2. Install dependencies

Install the required npm packages:

```bash
npm install
```

---

## 3. Configure your Discord bot

Create a Discord application through the:

**Discord Developer Portal**

Create a bot and obtain your bot token.

Your bot will also need the appropriate permissions and intents required by the project.

---

# 🔐 Configuration

## Environment Variables

For security, sensitive information should be stored in environment variables instead of being written directly into the source code.

Create a `.env` file:

```env
DISCORD_TOKEN=your_discord_bot_token
```

If additional credentials are required by your deployment, add them to the same file.

### ⚠️ Important

**Never commit your `.env` file to GitHub.**

Add this to `.gitignore`:

```gitignore
.env
node_modules/
*.sqlite
```

If a Discord or API token has already been exposed publicly, **revoke and regenerate it immediately**.

---

# 🚀 Running Yariko

Start the bot with:

```bash
node index.js
```

If everything is configured correctly, Yariko should connect to Discord.

You can then use:

```text
/help
```

inside Discord to see the available commands.

---

# 💾 Database

Yariko uses SQLite for persistent data.

The repository contains:

```text
kekw.sqlite
```

The project also uses:

* `better-sqlite3`
* `quick.db`

The database stores persistent information used by the bot.

### ⚠️ Database Backups

If you're hosting your own instance, make regular backups of your database.

```text
kekw.sqlite
```

Avoid committing production databases containing player data to a public repository.

---

# 🎴 Character Data

Character data is stored inside the:

```text
Dex/
```

directory.

Currently available datasets include:

| File           | Purpose                    |
| -------------- | -------------------------- |
| `Anime.json`   | Anime character data       |
| `1-star.json`  | 1-star character data      |
| `4-star.json`  | 4-star character data      |
| `Genshin.json` | Genshin character data     |
| `Promo.json`   | Promotional character data |

This structure allows the character database to be expanded without putting all character information directly into the bot's main code.

---

# 🛠️ Development

Want to work on Yariko?

Start by cloning the repository:

```bash
git clone https://github.com/jzc9307/Yariko.git
cd Yariko
```

Install dependencies:

```bash
npm install
```

Create your local configuration and start the bot:

```bash
node index.js
```

---

## 📁 Working With Commands

Discord commands are located in:

```text
commands/
```

Each JavaScript file represents a command.

For example:

```text
commands/
├── balance.js
├── buy.js
├── daily.js
├── dex.js
├── event.js
├── help.js
├── inventory.js
├── invite.js
├── itemsadd.js
├── itemsdel.js
├── profile.js
├── shop.js
├── start.js
├── test.js
├── vote.js
└── wild.js
```

The bot automatically loads the command files when it starts.

---

# 🎴 Working With the Dex

Character data is stored separately from the commands.

```text
Dex/
├── Anime.json
├── 1-star.json
├── 4-star.json
├── Genshin.json
└── Promo.json
```

When adding or modifying characters:

* Follow the existing JSON structure
* Keep character names consistent
* Validate your JSON
* Avoid duplicate entries
* Check image URLs
* Test the relevant commands before committing

---

# 🌐 Server

Yariko also includes an Express server:

```text
server.js
```

This provides an HTTP server alongside the Discord bot and can be useful for hosting environments that expect a web service.

---

# 🧰 Tech Stack

| Technology        | Purpose                          |
| ----------------- | -------------------------------- |
| 🟨 **Node.js**    | JavaScript runtime               |
| 💬 **Discord.js** | Discord bot framework            |
| 💾 **SQLite**     | Persistent data storage          |
| 🗃️ **QuickDB**   | Database interface               |
| ⚡ **Express**     | Web server                       |
| 📦 **npm**        | Dependency management            |
| 📊 **Top.gg SDK** | Bot listing / voting integration |

---

# 🧪 Testing

The project contains a dedicated:

```text
/test
```

command for development/testing purposes.

When developing new features, test changes locally before pushing them to the main repository.

---

# 🤝 Contributing

Contributions are welcome! 🌸

## Getting Started

Fork the repository and clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/Yariko.git
cd Yariko
```

Create a new branch:

```bash
git checkout -b feature/my-feature
```

Install dependencies:

```bash
npm install
```

Make your changes and test them.

Then commit:

```bash
git add .
git commit -m "feat: add my feature"
```

Push your branch:

```bash
git push origin feature/my-feature
```

Open a Pull Request on GitHub.

---

# 💡 Contribution Ideas

There are many ways to contribute to Yariko:

### 🎴 Game

* Add new characters
* Add new anime series
* Improve the Dex
* Add new game mechanics
* Improve existing systems

### 💰 Economy

* Improve the shop
* Add new items
* Add additional rewards
* Improve balancing

### 💬 Discord

* Add new slash commands
* Improve embeds
* Improve interactive menus
* Improve error handling
* Improve `/help`

### 🛠️ Development

* Improve code structure
* Add tests
* Improve documentation
* Improve database handling
* Improve security

---

# 🐛 Bug Reports

Found something broken?

Open an issue on GitHub and include:

```text
What happened?

What did you expect to happen?

How can the problem be reproduced?

What command were you using?

Were there any errors in the console?
```

Screenshots and error logs are helpful when reporting bugs.

---

# 💡 Feature Requests

Have an idea for Yariko?

Open a feature request and describe:

* What you want to add
* How the feature would work
* Why it would be useful
* Any examples or references

Anime and character suggestions are welcome. 🌸

---

# 🔒 Security

Please **do not** publish:

* Discord bot tokens
* API keys
* Database credentials
* Private configuration
* User data

If you discover a security vulnerability, avoid posting sensitive information publicly in an issue.

---

# 📜 License

Yariko is released under the **Unlicense**.

See [`LICENSE`](LICENSE) for the complete license text.

---

# 🌸 Roadmap

The following roadmap can be updated as Yariko develops.

### 🎴 Characters

* [ ] Expand anime character database
* [ ] Add more character categories
* [ ] Expand promotional characters
* [ ] Add more anime franchises

### 🎮 Gameplay

* [ ] Expand game mechanics
* [ ] Improve character interactions
* [ ] Expand events
* [ ] Improve progression

### 💰 Economy

* [ ] Expand shop
* [ ] Add more items
* [ ] Improve economy balancing
* [ ] Expand rewards

### 🎨 Presentation

* [ ] Add official Yariko banner
* [ ] Add gameplay GIFs
* [ ] Add command screenshots
* [ ] Add character showcase

### 🛠️ Development

* [ ] Add automated testing
* [ ] Improve developer documentation
* [ ] Improve error handling
* [ ] Improve configuration
* [ ] Improve database management

---

# ⭐ Support

If you enjoy **Yariko**, consider supporting the project!

⭐ **Star the repository**

🐛 **Report bugs**

💡 **Suggest features**

🤝 **Contribute**

🎴 **Help expand the character database**

Every contribution helps Yariko grow.

---

<div align="center">

## 🌸 Thanks for checking out Yariko! 🌸

**Made with ❤️ for anime fans.**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-Yariko-181717?style=for-the-badge\&logo=github)](https://github.com/jzc9307/Yariko)

<br><br>

**🎴 Collect • 💰 Earn • 🌸 Explore 🎴**

</div>
