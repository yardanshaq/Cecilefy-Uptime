<div align="center" width="100%">
    <img src="./public/icon.svg" width="128" alt="" />
</div>

# Cecilefy Uptime

Cecilefy Uptime is an easy-to-use self-hosted monitoring tool.

<a target="_blank" href="https://github.com/yardanshaq/cecilefy-uptime"><img src="https://img.shields.io/github/stars/louislam/cecilefy-uptime?style=flat" /></a> <a target="_blank" href="https://hub.docker.com/r/louislam/cecilefy-uptime"><img src="https://img.shields.io/docker/pulls/louislam/cecilefy-uptime" /></a> <a target="_blank" href="https://hub.docker.com/r/louislam/cecilefy-uptime"><img src="https://img.shields.io/docker/v/louislam/cecilefy-uptime/latest?label=docker%20image%20ver." /></a> <a target="_blank" href="https://github.com/yardanshaq/cecilefy-uptime"><img src="https://img.shields.io/github/last-commit/louislam/cecilefy-uptime" /></a>  <a target="_blank" href="https://opencollective.com/cecilefy-uptime"><img src="https://opencollective.com/cecilefy-uptime/total/badge.svg?label=Open%20Collective%20Backers&color=brightgreen" /></a>
[![GitHub Sponsors](https://img.shields.io/github/sponsors/louislam?label=GitHub%20Sponsors)](https://github.com/sponsors/louislam) <a href="https://weblate.kuma.pet/projects/cecilefy-uptime/cecilefy-uptime/">
<img src="https://weblate.kuma.pet/widgets/cecilefy-uptime/-/svg-badge.svg" alt="Translation status" />
</a>

<img src="https://user-images.githubusercontent.com/1336778/212262296-e6205815-ad62-488c-83ec-a5b0d0689f7c.jpg" width="700" alt="" />

## 🥔 Live Demo

Try it!

Demo Server (Location: Frankfurt - Germany): https://demo.kuma.pet/start-demo

It is a temporary live demo, all data will be deleted after 10 minutes. Sponsored by [Cecilefy Uptime Sponsors](https://github.com/yardanshaq/cecilefy-uptime#%EF%B8%8F-sponsors).

## ⭐ Features

- Monitoring uptime for HTTP(s) / TCP / HTTP(s) Keyword / HTTP(s) Json Query / Ping / DNS Record / Push / Steam Game Server / Docker Containers
- Fancy, Reactive, Fast UI/UX
- Notifications via Telegram, Discord, Gotify, Slack, Pushover, Email (SMTP), and [90+ notification services, click here for the full list](https://github.com/yardanshaq/cecilefy-uptime/tree/master/src/components/notifications)
- 20-second intervals
- [Multi Languages](https://github.com/yardanshaq/cecilefy-uptime/tree/master/src/lang)
- Multiple status pages
- Map status pages to specific domains
- Ping chart
- Certificate info
- Proxy support
- 2FA support

## 🔧 How to Install

### 🐳 Docker

```bash
docker run -d --restart=always -p 3001:3001 -v cecilefy-uptime:/app/data --name cecilefy-uptime louislam/cecilefy-uptime:1
```

Cecilefy Uptime is now running on <http://0.0.0.0:3001>.

> [!WARNING]
> File Systems like **NFS** (Network File System) are **NOT** supported. Please map to a local directory or volume.

> [!NOTE]
> If you want to limit exposure to localhost (without exposing port for other users or to use a [reverse proxy](https://github.com/yardanshaq/cecilefy-uptime/wiki/Reverse-Proxy)), you can expose the port like this:
> 
> ```bash
> docker run -d --restart=always -p 127.0.0.1:3001:3001 -v cecilefy-uptime:/app/data --name cecilefy-uptime louislam/cecilefy-uptime:1
> ```

### 💪🏻 Non-Docker

Requirements:

- Platform
  - ✅ Major Linux distros such as Debian, Ubuntu, CentOS, Fedora and ArchLinux etc.
  - ✅ Windows 10 (x64), Windows Server 2012 R2 (x64) or higher
  - ❌ FreeBSD / OpenBSD / NetBSD
  - ❌ Replit / Heroku
- [Node.js](https://nodejs.org/en/download/) 18 / 20.4
- [npm](https://docs.npmjs.com/cli/) 9
- [Git](https://git-scm.com/downloads)
- [pm2](https://pm2.keymetrics.io/) - For running Cecilefy Uptime in the background

```bash
git clone https://github.com/yardanshaq/cecilefy-uptime.git
cd cecilefy-uptime
npm run setup

# Option 1. Try it
node server/server.js

# (Recommended) Option 2. Run in the background using PM2
# Install PM2 if you don't have it:
npm install pm2 -g && pm2 install pm2-logrotate

# Start Server
pm2 start server/server.js --name cecilefy-uptime
```

Cecilefy Uptime is now running on http://localhost:3001

More useful PM2 Commands

```bash
# If you want to see the current console output
pm2 monit

# If you want to add it to startup
pm2 save && pm2 startup
```

### Advanced Installation

If you need more options or need to browse via a reverse proxy, please read:

https://github.com/yardanshaq/cecilefy-uptime/wiki/%F0%9F%94%A7-How-to-Install

## 🆙 How to Update

Please read:

https://github.com/yardanshaq/cecilefy-uptime/wiki/%F0%9F%86%99-How-to-Update

## 🆕 What's Next?

I will assign requests/issues to the next milestone.

https://github.com/yardanshaq/cecilefy-uptime/milestones

## ❤️ Sponsors

Thank you so much! (GitHub Sponsors will be updated manually. OpenCollective sponsors will be updated automatically, the list will be cached by GitHub though. It may need some time to be updated)

<img src="https://uptime.kuma.pet/sponsors?v=6" alt />

## 🖼 More Screenshots

Light Mode:

<img src="https://uptime.kuma.pet/img/light.jpg" width="512" alt="" />

Status Page:

<img src="https://user-images.githubusercontent.com/1336778/134628766-a3fe0981-0926-4285-ab46-891a21c3e4cb.png" width="512" alt="" />

Settings Page:

<img src="https://louislam.net/cecilefyuptime/2.jpg" width="400" alt="" />

Telegram Notification Sample:

<img src="https://louislam.net/cecilefyuptime/3.jpg" width="400" alt="" />

## Motivation

- I was looking for a self-hosted monitoring tool like "Uptime Robot", but it is hard to find a suitable one. One of the closest ones is statping. Unfortunately, it is not stable and no longer maintained.
- Wanted to build a fancy UI.
- Learn Vue 3 and vite.js.
- Show the power of Bootstrap 5.
- Try to use WebSocket with SPA instead of a REST API.
- Deploy my first Docker image to Docker Hub.

If you love this project, please consider giving it a ⭐.

## 🗣️ Discussion / Ask for Help

⚠️ For any general or technical questions, please don't send me an email, as I am unable to provide support in that manner. I will not respond if you ask questions there.

I recommend using Google, GitHub Issues, or Cecilefy Uptime's subreddit for finding answers to your question. If you cannot find the information you need, feel free to ask:

- [GitHub Issues](https://github.com/yardanshaq/cecilefy-uptime/issues)
- [Subreddit (r/CecilefyUptime)](https://www.reddit.com/r/CecilefyUptime/)

My Reddit account: [u/louislamlam](https://reddit.com/u/louislamlam)
You can mention me if you ask a question on the subreddit.

## Contributions

### Create Pull Requests

We DO NOT accept all types of pull requests and do not want to waste your time. Please be sure that you have read and follow pull request rules:
[CONTRIBUTING.md#can-i-create-a-pull-request-for-cecilefy-uptime](https://github.com/yardanshaq/cecilefy-uptime/blob/master/CONTRIBUTING.md#can-i-create-a-pull-request-for-cecilefy-uptime)

### Test Pull Requests

There are a lot of pull requests right now, but I don't have time to test them all.

If you want to help, you can check this:
https://github.com/yardanshaq/cecilefy-uptime/wiki/Test-Pull-Requests

### Test Beta Version

Check out the latest beta release here: https://github.com/yardanshaq/cecilefy-uptime/releases

### Bug Reports / Feature Requests

If you want to report a bug or request a new feature, feel free to open a [new issue](https://github.com/yardanshaq/cecilefy-uptime/issues).

### Translations

If you want to translate Cecilefy Uptime into your language, please visit [Weblate Readme](https://github.com/yardanshaq/cecilefy-uptime/blob/master/src/lang/README.md).

### Spelling & Grammar

Feel free to correct the grammar in the documentation or code.
My mother language is not English and my grammar is not that great.


# Cecilefy-Uptime
