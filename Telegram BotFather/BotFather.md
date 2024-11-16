
# BotFather Guide

## What is BotFather?

**BotFather** is an official [**Telegram**](https://telegram.org/) bot that acts as a centralized bot management tool. It allows users to create, manage, and configure Telegram bots. If you want to develop a Telegram bot, **BotFather** is the first tool you'll need to interact with. It provides you with a simple interface to create new bots, set their properties, generate API tokens, and manage existing bots.

### How to Access BotFather

1. Open the Telegram app (available on mobile, desktop, or web).
2. In the search bar, type **BotFather** and select the verified bot (with a blue checkmark).
3. Start a chat with BotFather by clicking the **Start** button.

You can also directly access BotFather using this link: [**BotFather**](https://t.me/BotFather)

---

## BotFather Commands

Here’s a list of useful commands provided by BotFather to help you manage your Telegram bots:

### 1. **Create a New Bot**

**Command:** `/newbot`

- This command allows you to create a new Telegram bot.
- BotFather will prompt you to enter a name and a unique username for your bot.
- The username must end with the word **"bot"** (e.g., `MyAwesomeBot` or `WeatherHelperBot`).
- Once created, BotFather will generate an **API token** for your bot, which you'll use in your code to interact with Telegram's Bot API.

**Example:**
```
You: /newbot
BotFather: Alright, a new bot. How are we going to call it? Please choose a name for your bot.
You: MyCoolBot
BotFather: Good. Now let's choose a username for your bot. It must end in 'bot'. Like this, for example: TetrisBot or tetris_bot.
You: MyCoolBot
BotFather: Done! Congratulations on your new bot. You will find it at t.me/MyCoolBot. You can now add a description, about section, and profile picture for your bot.
Use this token to access the HTTP API:
`123456789:ABC-DEF1234ghIkl-zyx57W2v23ew11`
Keep your token secure and store it safely; it can be used by anyone to control your bot.
```

---

### 2. **Manage Bot Settings**

- **/setname** - Change the name of your bot.
- **/setdescription** - Add a short description of your bot (displayed in the bot’s profile).
- **/setabouttext** - Set the "About" section text for your bot (visible when users view your bot's profile).
- **/setuserpic** - Upload a profile picture for your bot.
- **/setcommands** - Define custom bot commands (like `/start`, `/help`).

  **Example Usage:**
  ```
  /setcommands
  Command: start - Start interacting with the bot
  Command: help - Get help on how to use the bot
  ```

- **/deletebot** - Delete your bot permanently.

---

### 3. **Bot Configuration**

- **/token** - Regenerate your bot's API token if it's compromised.
- **/revoke** - Revoke your bot’s existing token, which will immediately stop it from working.
- **/setjoingroups** - Enable or disable the bot's ability to be added to groups.
  - **Example**: `/setjoingroups yes` or `/setjoingroups no`
- **/setprivacy** - Toggle the privacy mode of your bot.
  - In **enabled** mode, the bot only sees messages that start with a `/` command.
  - In **disabled** mode, the bot can see all messages sent in a group.
  - **Example**: `/setprivacy off` or `/setprivacy on`

---

### 4. **Bot Interaction and Testing**

- **/setinline** - Enable inline mode, allowing users to interact with your bot in any chat by typing `@YourBotName`.
- **/setinlinefeedback** - Enable or disable inline feedback messages.
- **/setinlinegeo** - Request location access when users use your inline bot.
- **/setdomain** - Link a verified domain to your bot.

---

### 5. **Additional Tools**

- **/mybots** - List all the bots you’ve created.
- **/botsettings** - Adjust settings for a specific bot.
- **/stats** - View your bot’s statistics.
- **/getfile** - Retrieve a file sent to your bot by its file ID.

---

## Example Workflow to Create a Bot

1. **Start BotFather and Create a Bot:**

   ```
   You: /newbot
   BotFather: Alright, a new bot. How are we going to call it? Please choose a name for your bot.
   You: MySampleBot
   BotFather: Good. Now let's choose a username for your bot. It must end in 'bot'.
   You: MySampleBot
   BotFather: Done! Congratulations on your new bot. You will find it at t.me/MySampleBot. Use this token to access the HTTP API:
   123456789:ABC-DEF1234ghIkl-zyx57W2v1u123ew11
   ```

2. **Set a Description:**

   ```
   You: /setdescription
   BotFather: Select a bot to change description.
   You: @MySampleBot
   BotFather: Alright, send me the new description.
   You: This bot helps you track your tasks efficiently.
   ```

3. **Define Bot Commands:**

   ```
   You: /setcommands
   BotFather: Select a bot to set commands.
   You: @MySampleBot
   BotFather: Now send me the list of commands.
   You:
   start - Start the bot
   help - Get help using the bot
   tasks - Show your current tasks
   ```

---

## Security Tips

- **Never share your API token** publicly. Treat it like a password.
- If you suspect your token is compromised, use `/revoke` to generate a new one.
- Regularly review your bot’s settings and permissions to ensure they are secure.

## Useful Links

- [Telegram Bot API Documentation](https://core.telegram.org/bots/api)
- [Python Telegram Bot Library](https://python-telegram-bot.readthedocs.io/)
- [Create Telegram Bots with Python (Tutorial)](https://github.com/abhijit-003/How-to-Create-Telegram-Bot)

This guide should help you get started with **BotFather** and managing your Telegram bots efficiently.
