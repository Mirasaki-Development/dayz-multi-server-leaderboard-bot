# DayZ Multi Server Leaderboard Bot

[![GitHub license](https://img.shields.io/github/license/Mirasaki-Development/dayz-multi-server-leaderboard-bot?style=flat-square)](https://github.com/Mirasaki-Development/dayz-multi-server-leaderboard-bot/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/Mirasaki-Development/dayz-multi-server-leaderboard-bot?style=flat-square)](https://github.com/Mirasaki-Development/dayz-multi-server-leaderboard-bot/issues)
[![GitHub forks](https://img.shields.io/github/forks/Mirasaki-Development/dayz-multi-server-leaderboard-bot?style=flat-square)](https://github.com/Mirasaki-Development/dayz-multi-server-leaderboard-bot/network)
[![GitHub stars](https://img.shields.io/github/stars/Mirasaki-Development/dayz-multi-server-leaderboard-bot?style=flat-square)](https://github.com/Mirasaki-Development/dayz-multi-server-leaderboard-bot/stargazers)

A DayZ bot written in Javascript to display your leaderboards using the CFTools Cloud API.

## Demo

Come try the bot yourself in our official [support server](https://discord.gg/jKja5FBnYf)!
![Demo](https://i.imgur.com/vzoS6cq.gif)

## Technologies Used

- [discord.js-bot-template](https://github.com/Mirasaki/discord.js-bot-template)
- [CFTools Cloud API](https://wiki.cftools.de/display/CFAPI/CFTools+Cloud+API)

## Prerequisites

- [Node.js](https://nodejs.org/en/download/)
    1) Head over to the download page
    2) Download the latest LTS available for your OS
    3) Be sure to check the box that says "Automatically install the necessary tools" when you're running the installation wizard
- A [Discord Bot account](https://discord.com/developers/applications)
    1) Head over to the page linked above
    2) Click "New Application" in the top right
    3) Give it a cool name and click "Create"
    4) Click "Bot" in the left hand panel
    5) Click "Add Bot" -> "Yes, do it!"
    6) Click "Rest Token" and copy it to your clipboard, you will need it later

## Installation

1. Download the latest release [here](https://github.com/Mirasaki-Development/dayz-multi-server-leaderboard-bot/releases)
2. Extract/unzip the downloaded compressed file into a new folder
3. Open a command prompt in the project root folder/directory
    - On Windows you can type `cmd.exe` in the File Explorer path
    - Root folder structure:
      - commands/
      - local_modules/
      - .env.example
      - index.js
      - etc...
4. Run the command `npm install`
5. Copy-paste the `.env.example` file in the same directory and re-name the created file to `.env`
6. Open the `.env` file and fill in your values
    - `DISCORD_CLIENT_ID`: Can be grabbed by creating a new application in [your Discord Developer Portal](https://discord.com/developers/applications)
    - `DISCORD_BOT_TOKEN`: After creating your bot on the link above, navigate to `Bot` in the left-side menu to reveal your bot-token
    - `TEST_SERVER_GUILD_ID`: (optional) In your Discord app: `Right-click your server icon -> Copy ID`
    - `CFTOOLS_API_APPLICATION_ID`: Application ID from your [CFTools Developer Apps](https://developer.cftools.cloud/applications) - Authorization has to be granted by navigating to the `Grant URL` that's displayed in your app overview
    - `CFTOOLS_API_SECRET`: Same as above, click `Reveal Secret`
7. Add the bot to your server by using the following link: (Replace CLIENT-ID with your DISCORD_CLIENT_ID from before) <https://discord.com/api/oauth2/authorize?client_id=CLIENT-ID&permissions=0&scope=bot%20applications.commands>
8. Run the command `node .` in the project root folder/directory or `npm run start` if you have [PM2](https://pm2.keymetrics.io/) installed to keep the process alive.
9. Open the `/config/servers.json` file and configure your servers, you can find the `CFTOOLS_SERVER_API_ID` at `Manage Server` in your [CF Cloud Panel](https://app.cftools.cloud/dashboard) (name is just the display name, doesn't affect your server)

### FAQ

#### How do I create the Discord bot account?

Check out [this video](https://www.youtube.com/watch?v=ibtXXoMxaho) by [The Coding Train](https://www.youtube.com/channel/UCvjgXvBlbQiydffZU7m1_aw)

#### Is any specific set-up required to use this?

Yes. Your DayZ server has to be connected to the [CFTools Cloud API](https://wiki.cftools.de/display/CFAPI/CFTools+Cloud+API) and needs the [GameLabs integration](https://steamcommunity.com/sharedfiles/filedetails/?id=2464526692) mod.

## License

[MIT](https://choosealicense.com/licenses/mit/)
