# 🤖 GitHubZipBot

A Telegram bot that downloads GitHub repositories as `.zip` files and sends them directly to your chat — complete with rich project details like description, languages, stars, and more.

Built with [Node.js](https://nodejs.org/) and [grammY](https://grammy.dev/) bot framework.

## ✨ Features

- 🔗 **Smart URL Parsing** — Accepts full GitHub URLs or `owner/repo` shorthand
- 📦 **Zip Download** — Downloads the default branch as a zip file
- 📝 **Rich Captions** — Displays name, description, languages, stars, forks, license, and file size
- 📊 **Language Breakdown** — Percentage-based language composition
- ⚡ **Live Progress** — Real-time status updates while processing
- 🎨 **Premium Emojis** — Uses Telegram premium custom emojis for a polished look
- ⚠️ **Error Handling** — Friendly messages for invalid repos, rate limits, and oversized files

## 🛠 Setup

### 1. Clone the repository

```bash
git clone https://github.com/nasirul786/GitHubZipBot.git
cd GitHubZipBot
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Copy the example env file and add your bot token:

```bash
cp .env.example .env
```

Edit `.env`:

```env
BOT_TOKEN=your_telegram_bot_token_here
GITHUB_TOKEN=your_github_personal_access_token  # optional
```

> **💡 Tip:** A GitHub token is optional but recommended. Without it, you're limited to **60 API requests/hour**. With a token, you get **5,000/hour**.

### 4. Start the bot

```bash
npm start
```

## 📖 Usage

1. Open your bot on Telegram
2. Send a GitHub repository link:
   - `https://github.com/expressjs/express`
   - `expressjs/express`
3. The bot fetches project details, downloads the zip, and sends it to you with a detailed caption!

### Example Output

The bot sends the `.zip` file with a caption containing:

- **📦 Repository name**
- **📝 Description**
- **🌐 Languages** (with percentages)
- **⭐ Stars** and **🔄 Forks**
- **🌿 Branch** and **📄 License**
- **💾 Zip file size**
- **🔗 Inline button** to view the repo on GitHub

## 📁 Project Structure

```
GitHubZipBot/
├── bot.js           # Main bot logic
├── .env             # Environment variables (not committed)
├── .env.example     # Template for .env
├── .gitignore
├── package.json
└── README.md
```

## ⚠️ Limitations

- Telegram maximum file upload size: **50 MB** (provides a direct GitHub download link for larger repos)
- Private repositories require a GitHub token with appropriate permissions
- GitHub API rate limiting: **60 req/hr** without token, **5,000 req/hr** with token

## 📄 License

ISC
