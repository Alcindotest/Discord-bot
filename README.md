# Discord-bot
 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index e97f3dc44092992a908c8f1b0bcc60ce5d7c8b01..99f7975dd1871680b4c3f7bae1d0d080be739bb5 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,34 @@
-# Discord-bot
\ No newline at end of file
+# Discord Ticket Bot
+
+A simple Discord bot built with `discord.js` that supports:
+
+- `!ping` health check
+- `!help` command list
+- `!ticket` private ticket channel creation per user
+
+## Setup
+
+1. Install dependencies:
+   ```bash
+   npm install
+   ```
+2. Create a Discord bot in the [Discord Developer Portal](https://discord.com/developers/applications).
+3. Enable **Message Content Intent** for your bot.
+4. Invite the bot to your server with permissions to:
+   - View Channels
+   - Send Messages
+   - Read Message History
+   - Manage Channels
+5. Set your bot token:
+   ```bash
+   export DISCORD_TOKEN="your_bot_token"
+   ```
+6. Run the bot:
+   ```bash
+   npm start
+   ```
+
+## Notes
+
+- Ticket channels are named `ticket-<username>`.
+- If a user already has a ticket channel, a new one is not created.
 
EOF
)
