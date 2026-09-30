# CryptNest V1

Files:
- `CryptNestbot.py` = Telegram bot + persistent SQLite + Mini App API
- `requirements.txt` = Python dependencies
- `index.html` = Mini App frontend
- `README.md` = instructions

## GitHub
Put ONLY `index.html` and `README.md` in the GitHub Pages repository:

`https://nihadmohammed504-prog.github.io/Cryptonest_bot/`

Do NOT put `CryptNestbot.py` or the bot token on GitHub.

## Bot host
Upload `CryptNestbot.py` and `requirements.txt` to your Telegram bot host.

The host must support:
1. Python
2. outbound HTTPS
3. an inbound public HTTPS URL to the aiohttp API
4. persistent storage/volume for `data/cryptnest.db`

Start command:

`python CryptNestbot.py`

If the host requires a different start command, use its normal Python start command.

## Mini App API URL
After deployment, your host must give you a public HTTPS URL, for example:

`https://YOUR-HOST-DOMAIN`

Open `index.html` and replace:

`const API_BASE="https://YOUR-BOT-HOST-DOMAIN";`

with that exact URL.

Without this one change, the Mini App cannot communicate with the bot server because GitHub Pages and the bot server are separate sites.

## Admin
Admin ID: `8259663112`

Commands:
`/admin`
`/addtask`
`/tasks`
`/enabletask ID`
`/disabletask ID`
`/deltask ID`
`/stats`
`/users`
`/setseason 1`

Use `/addtask` to add YouTube, Telegram, social or website tasks without editing code.

## Database safety
Never delete `data/cryptnest.db`.

When updating the bot, replace the Python file but keep the database file. Your hosting provider must use persistent storage; otherwise a restart/redeploy can erase users and points.

## Token
The token was supplied for setup and is inside `CryptNestbot.py`. Do not upload that file to GitHub. Because the token was shared in chat, regenerate it with @BotFather before public promotion if possible.