<div align="center">

# 🌸 Yariko

### ✨ An Anime Game Discord Bot ✨

*A little bit of anime. A little bit of chaos. A lot of fun.*

[![Discord.js](https://img.shields.io/badge/Discord.js-v14-5865F2?style=for-the-badge\&logo=discord\&logoColor=white)](https://discord.js.org/)
[![Node.js](https://img.shields.io/badge/Node.js-JavaScript-339933?style=for-the-badge\&logo=node.js\&logoColor=white)](https://nodejs.org/)
[![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?style=for-the-badge\&logo=sqlite\&logoColor=white)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-Unlicense-blue?style=for-the-badge)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/jzc9307/Yariko?style=for-the-badge)](https://github.com/jzc9307/Yariko/stargazers)

<br>

[📖 Documentation](#-documentation) •
[⚡ Installation](#-installation) •
[🎮 Commands](#-commands) •
[🛠️ Development](#️-development) •
[🤝 Contributing](#-contributing)

</div>

---

## 🌸 About Yariko

**Yariko** is an anime-themed Discord game bot built with **Node.js** and **Discord.js**.

The project is designed to bring anime-inspired character collecting and game mechanics directly into Discord, allowing users to interact with the bot without leaving their server.

Yariko stores persistent game information using SQLite and organizes its character data through the `Dex` directory.

> 💮 **Collect. Discover. Play. Repeat.**

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🎴 Anime Game

Interact with an anime-focused game directly through Discord.

* Character-based gameplay
* Anime character database
* Multiple character categories
* Promotional character data
* Discord interactions

</td>
<td width="50%">

### 💾 Persistent Data

Player information can be stored persistently using:

* SQLite
* `better-sqlite3`
* `quick.db`

Your game data doesn't have to disappear when the bot restarts.

</td>
</tr>

<tr>
<td>

### ⚔️ Discord Integration

Built around the Discord platform with:

* Discord.js v14
* Slash commands
* Discord interactions
* Embeds
* Buttons / interactive components

</td>
<td>

### 🌟 Character Database

Yariko includes several data collections inside `Dex/`.

* Anime characters
* 1-star characters
* 4-star characters
* Genshin characters
* Promotional characters

</td>
</tr>
</table>

---

# 📸 Screenshots & GIFs

> Replace the placeholders below with screenshots or GIFs from your actual bot.

### 🎮 In-game

<p align="center">
  <img src="assets/gameplay.gif" width="700">
</p>

### 🎴 Character Collection

<p align="center">
  <img src="assets/collection.png" width="700">
</p>

### 🌸 Commands

<p align="center">
  <img src="assets/commands.png" width="700">
</p>

### ✨ More Coming Soon

Have a cool screenshot or GIF?

Feel free to open a pull request and add it to the showcase.

---

# 🎮 Commands

Yariko uses Discord commands to interact with the game.

> **Note:** The exact command list should be kept synchronized with the files inside `commands/`.

| Command | Description                       |
| :-----: | --------------------------------- |
| `/help` | Display available Yariko commands |
| `/ping` | Check the bot's response latency  |
|  `/...` | More commands coming soon         |

### Command Format

Arguments can be documented using:

|    Syntax    | Meaning              |
| :----------: | -------------------- |
| `<argument>` | Required argument    |
| `[argument]` | Optional argument    |
|    `@user`   | Discord user mention |
|  `#channel`  | Discord channel      |

For example:

```text
/help
```

> 💡 **Tip:** Run `/help` inside Discord to see the commands available in your current version of Yariko.

---

# 🗂️ Project Structure

```text
Yariko/
│
├── 📁 commands/
│   └── Discord bot commands
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
├── 📄 package.json
├── 📄 package-lock.json
├── 📄 replit.nix
├── 💾 kekw.sqlite
├── 📄 LICENSE
└── 📄 README.md
```

The repository currently contains separate `commands/` and `Dex/` directories, along with the main bot entry point, server, package configuration, SQLite database, and Replit configuration.

---

# ⚡ Installation

## 📋 Requirements

Before running Yariko, make sure you have:

* [Node.js](https://nodejs.org/) installed
* A Discord account
* A Discord application/bot
* A Discord bot token
* Git installed

Yariko currently uses Discord.js **v14.11.0** and Node.js packages including `better-sqlite3`, `quick.db`, `express`, and the Top.gg SDK.

---

## 1️⃣ Clone the repository

```bash
git clone https://github.com/jzc9307/Yariko.git
cd Yariko
```

---

## 2️⃣ Install dependencies

```bash
npm install
```

This installs the dependencies defined in `package.json`.

---

## 3️⃣ Configure your Discord bot

Create a Discord application through the Discord Developer Portal.

You will need your:

```text
Bot Token
Client ID
Guild ID
```

Keep your bot token **private**.

Never upload it to GitHub.

### Recommended configuration

Use environment variables rather than placing secrets directly inside your source code.

Example:

```env
DISCORD_TOKEN=your_bot_token_here
CLIENT_ID=your_client_id_here
GUILD_ID=your_guild_id_here
```

Then add `.env` to `.gitignore`:

```gitignore
.env
```

> ⚠️ **Security:** If your Discord token is ever exposed, immediately regenerate it through the Discord Developer Portal.

---

# 🚀 Running Yariko

Start the bot with:

```bash
node index.js
```

If your project is configured with an npm start script, you can also use:

```bash
npm start
```

### Development

For development, simply restart the bot after making changes:

```bash
node index.js
```

The current repository does not define a dedicated `start` or `dev` npm script, so `node index.js` is the reliable command based on the current `package.json`.

---

# 🛠️ Developer Setup

Want to modify Yariko?

### 1. Fork the repository

Click **Fork** on GitHub and clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/Yariko.git
cd Yariko
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create your development configuration

Set your Discord credentials using environment variables or whatever configuration mechanism your local version of the bot expects.

### 4. Start the bot

```bash
node index.js
```

### 5. Make your changes

A typical workflow might look like:

```text
commands/
   ↓
Add / modify command
   ↓
Test locally
   ↓
Check Discord interaction
   ↓
Commit changes
   ↓
Open Pull Request
```

---

# 🧩 Adding a Command

Commands are located inside:

```text
commands/
```

A typical command should:

1. Define the command name
2. Define its description/options
3. Handle the Discord interaction
4. Return a useful response
5. Handle errors gracefully

Example structure:

```js
module.exports = {
    data: {
        name: 'example',
        description: 'An example Yariko command'
    },

    async execute(interaction) {
        await interaction.reply('🌸 Hello from Yariko!');
    }
};
```

> The exact command module format should follow the existing implementation in `commands/`.

---

# 🎴 Character Data

Yariko's character information is organized inside:

```text
Dex/
```

The repository currently includes data files for:

```text
Anime.json
1-star.json
4-star.json
Genshin.json
Promo.json
```

This makes it possible to expand Yariko's character database without putting all character information directly into the bot's main code.

### Adding Characters

When adding new characters:

* Follow the existing JSON structure
* Keep naming consistent
* Validate JSON before committing
* Avoid duplicate entries
* Check that image URLs remain accessible

---

# 💾 Database

Yariko includes an SQLite database:

```text
kekw.sqlite
```

The project also depends on:

```text
better-sqlite3
quick.db
```

These packages provide persistent local storage for the bot.

### ⚠️ Database Backups

If you're hosting your own instance, regularly back up:

```text
kekw.sqlite
```

Do not commit production player data to a public repository.

---

# 🌐 Server

Yariko also contains:

```text
server.js
```

The project includes Express as a dependency, allowing a lightweight HTTP server to run alongside the Discord bot.

This can be useful for hosting environments that expect an HTTP service.

---

# 🔧 Tech Stack

| Technology        | Purpose                     |
| ----------------- | --------------------------- |
| 🟨 **Node.js**    | Runtime                     |
| 💬 **Discord.js** | Discord API / bot framework |
| 💾 **SQLite**     | Persistent database         |
| 🗃️ **QuickDB**   | Database abstraction        |
| ⚡ **Express**     | HTTP server                 |
| 📊 **Top.gg SDK** | Bot listing integration     |
| 📦 **npm**        | Package management          |

The current `package.json` lists Discord.js 14.11.0, Express 4.18.2, QuickDB 9.0.8, better-sqlite3 7.6.2, and `@top-gg/sdk` 3.1.3 among its dependencies.

---

# 🤝 Contributing

Contributions are welcome! 🌸

### Contribution workflow

```bash
# Fork the project first

git clone https://github.com/YOUR_USERNAME/Yariko.git

cd Yariko

npm install

git checkout -b feature/my-new-feature
```

Make your changes, test them, then:

```bash
git add .
git commit -m "feat: add my new feature"
git push origin feature/my-new-feature
```

Finally, open a **Pull Request**.

### 💡 Good contribution ideas

* Add new characters
* Improve existing commands
* Add new game mechanics
* Improve error handling
* Improve embeds/UI
* Add documentation
* Fix bugs
* Improve database handling
* Add tests

---

# 🐛 Bug Reports

Found a bug?

Please open a GitHub Issue and include:

```text
What happened?
What did you expect to happen?
How can we reproduce it?
What version are you using?
Any relevant error messages?
```

Screenshots and console errors are especially helpful.

---

# 💡 Feature Requests

Have an idea for Yariko?

Open an issue describing:

* What you want to add
* Why it would be useful
* How you imagine it working
* Any examples or references

Anime character suggestions are welcome too. 🌸

---

# 📜 License

Yariko is currently distributed under the **Unlicense**.

See [`LICENSE`](LICENSE) for the complete license text.

---

# 🌸 Roadmap

> This section can be updated as development continues.

### 🎴 Game

* [ ] Expand character database
* [ ] Improve ch
