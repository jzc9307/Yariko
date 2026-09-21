# Yariko 🎴

> **An Anime Game Discord Bot**

Yariko is a Discord bot built around anime and character-collection gameplay. It provides an interactive game experience through Discord slash commands, with character data, game systems, and persistent player data.

## ✨ Features

* 🎴 **Anime Character Collection**

  * Collect and interact with anime characters
  * Multiple character rarities
  * Anime and promotional character data

* 🎮 **Game System**

  * Play the game directly through Discord
  * Use slash commands for game interactions
  * Persistent player data

* 🌟 **Multiple Rarities**

  * 1-star characters
  * 4-star characters
  * Promotional characters

* ⚔️ **Genshin Characters**

  * Includes a dedicated Genshin character database

* 💾 **Persistent Database**

  * Uses SQLite through `better-sqlite3`
  * Uses `quick.db` for simple data storage

* 🔗 **Discord Integration**

  * Built with Discord.js
  * Slash command support
  * Interactive buttons and embeds

## 🛠️ Built With

* [Node.js](https://nodejs.org/)
* [Discord.js](https://discord.js.org/)
* [QuickDB](https://quickdb.js.org/)
* SQLite
* Express
* [Top.gg](https://top.gg/)

## 📁 Project Structure

```text
Yariko/
├── commands/          # Discord slash commands
├── Dex/               # Character/game data
│   ├── Anime.json
│   ├── 1-star.json
│   ├── 4-star.json
│   ├── Genshin.json
│   └── Promo.json
├── index.js            # Main bot entry point
├── server.js           # Express keep-alive server
├── kekw.sqlite         # SQLite database
├── package.json        # Dependencies and project configuration
├── package-lock.json
├── replit.nix
└── LICENSE
```

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/jzc9307/Yariko.git
cd Yariko
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure the bot

Create an environment variable containing your Discord bot token:

```env
TOKEN=your_discord_bot_token
```

> **Never commit your bot token or other secrets to GitHub.**

### 4. Start the bot

```bash
node index.js
```

Once started, Yariko will connect to Discord and register its application commands.

## 🎮 Commands

Yariko uses Discord slash commands.

Use:

```text
/help
```

to view the available commands.

The bot also includes a simple prefix command:

```text
!ping
```

which returns the bot's current Discord API latency.

## 🗃️ Character Data

Character information is stored inside the `Dex` directory.

Currently included data sets include:

| Data File      | Description            |
| -------------- | ---------------------- |
| `Anime.json`   | Anime character data   |
| `1-star.json`  | 1-star characters      |
| `4-star.json`  | 4-star characters      |
| `Genshin.json` | Genshin character data |
| `Promo.json`   | Promotional characters |

## 🌐 Hosting

Yariko includes a small Express server that listens on port `3000`.

The server provides a simple endpoint that can be used by hosting services that require an active web server.

## 🤝 Contributing

Contributions are welcome!

If you'd like to contribute:

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature/my-feature
```

3. Make your changes
4. Commit your changes

```bash
git commit -m "Add my feature"
```

5. Push your branch

```bash
git push origin feature/my-feature
```

6. Open a Pull Request

## 📜 License

This project is licensed under the **Unlicense**.

See [`LICENSE`](LICENSE) for more information.

## 💬 Support

Need help or want to follow development?

Join the Discord support server:

**[Join the Yariko Support Server](https://discord.gg/v4mTzw6kH4)**

## ⭐ Support the Project

If you enjoy Yariko, consider giving the repository a ⭐ on GitHub!

You can also vote for the bot on Top.gg.

---

Made with ❤️ for anime fans.
