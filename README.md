<p align="center">
<a href="#"><img title="Whatsapp-Bot" src="https://img.shields.io/badge/Whatsapp Bot-green?colorA=%23ff0000&colorB=%23017e40&style=for-the-badge"></a>
</p>
<p align="center">
<a href="https://github.com/Rex-Arnab"><img title="Author" src="https://img.shields.io/badge/AUTHOR-Rex--Arnab-red?style=for-the-badge&logo=github"></a>
</p>
<p align="center">
<a href="https://github.com/Rex-Arnab/followers"><img title="Followers" src="https://img.shields.io/github/followers/Rex-Arnab?color=blue&style=flat-square"></a>
<a href="https://github.com/Rex-Arnab/whatsapp-bot/stargazers/"><img title="Stars" src="https://img.shields.io/github/stars/Rex-Arnab/whatsapp-bot?color=red&style=flat-square"></a>
<a href="https://github.com/Rex-Arnab/whatsapp-bot/network/members"><img title="Forks" src="https://img.shields.io/github/forks/Rex-Arnab/whatsapp-bot?color=red&style=flat-square"></a>
<a href="https://github.com/Rex-Arnab/whatsapp-bot/watchers"><img title="Watching" src="https://img.shields.io/github/watchers/Rex-Arnab/whatsapp-bot?label=Watchers&color=blue&style=flat-square"></a>
<a href="#"><img title="UNMAINTENED" src="https://img.shields.io/badge/MAINTENED-YES-blue.svg"></a>
</p>

## Clone this project

```bash
> git clone https://github.com/Rex-Arnab/Jarvis_Whatsapp_Bot_2.0.git
```
# whatsapp-web.js
A WhatsApp API client that connects through the WhatsApp Web browser app

It uses Puppeteer to run a real instance of Whatsapp Web to avoid getting blocked.

**NOTE:** I can't guarantee you will not be blocked by using this method, although it has worked for me. WhatsApp does not allow bots or unofficial clients on their platform, so this shouldn't be considered totally safe.

## Installation

The module is now available on npm! `npm i whatsapp-web.js`

Please note that Node v10.18.1+ is required due to Puppeteer.

## Example usage

```js
const { Client } = require('whatsapp-web.js');
const client = new Client();

client.on('qr', (qr) => {
    // Generate and scan this code with your phone
    console.log('QR RECEIVED', qr);
});

client.on('ready', () => {
    console.log('Client is ready!');
});

client.on('message', msg => {
    if (msg.body == '!ping') {
        msg.reply('pong');
    }
});

client.initialize();
```

Take a look at [example.js](https://github.com/pedroslopez/whatsapp-web.js/blob/master/example.js) for another example with more use cases.


## Troubleshooting

Make sure all the necessary dependencies are installed.
https://github.com/puppeteer/puppeteer/blob/main/docs/troubleshooting.md


# Supported features

| Feature  | Status |
| ------------- | ------------- |
| Send messages  | ✅  |
| Receive messages  | ✅  |
| Send media (images/audio/documents)  | ✅  |
| Send media (video)  | ✅ [(requires google chrome)](https://waguide.pedroslopez.me/features/handling-attachments#caveat-for-sending-videos-and-gifs)  |
| Send stickers | ✅ |
| Receive media (images/audio/video/documents)  | ✅  |
| Send contact cards | ✅ |
| Send location | ✅ |
| Receive location | ✅ | 
| Message replies | ✅ |
| Join groups by invite  | ✅ |
| Get invite for group  | ✅ |
| Modify group info (subject, description)  | ✅  |
| Modify group settings (send messages, edit info)  | ✅  |
| Add group participants  | ✅  |
| Kick group participants  | ✅  |
| Promote/demote group participants | ✅ |
| Mention users | ✅ |
| Mute/unmute chats | ✅ |
| Block/unblock contacts | ✅ |
| Get contact info | ✅ |
| Get profile pictures | ✅ |
| Set user status message | ✅ |

Something missing? Make an issue and let us know!

## Comming Soon Features

| Sticker Creator |            Feature             |
| :-------------: | :----------------------------: |
|       ✅        |    Send Photo with Caption     |
|       ✅        |         Reply A Photo          |
|       ❌        |           Image Url            |
|       ❌        | Send Video or GIF with Caption |

| Downloader |             Feature              |
| :--------: | :------------------------------: |
|     ❌     |    YouTube mp3/mp4 Downloader    |
|     ❌     |        Doujin Downloader         |
|     ❌     | Instagram Video/Image Downloader |
|     ❌     |    Facebook Video Downloader     |

| Other |          Feature          |
| :---: | :-----------------------: |
|  ❌   |     Get a random meme     |
|  ❌   |      Text to speech       |
|  ❌   | Get a random waifu images |
|  ❌   |    Get a random quotes    |
|  ❌   | Get a random anime quotes |
|  ❌   | Get info gempa from BMKG  |
|  ❌   |    Weather's report's     |
|  ❌   |         Wikipedia         |
|  ❌   |      Anime searcher       |
|  ❌   |  Get a random cat images  |
|  ❌   |  Get a random dog images  |
|  And  |         Others...         |

| Group Only |              Feature              |
| :--------: | :-------------------------------: |
|     ✅     |           Promote User            |
|     ✅     |            Demote User            |
|     ✅     |             Kick User             |
|     ✅     |             Add User              |
|     ✅     |         Mention All User          |
|     ✅     |          Get link group           |
|     ❌     |          Get Admin list           |
|     ❌     |          Get owner group          |
|     ❌     |  enable or disable nsfw command   |
|     ❌     | enable or disable welcome feature |

| Owner Group Only |        Feature        |
| :--------------: | :-------------------: |
|        ❌        | Kick All Member Group |

| Owner Bot Only |      Feature      |
| :------------: | :---------------: |
|       ❌       |  leave all group  |
|       ❌       | clear all message |
|       ❌       |     Broadcast     |


## Links

* [Reference](https://pedroslopez.me/whatsapp-web.js)
* [Guide](https://waguide.pedroslopez.me/) _(work in progress)_
* [GitHub](https://github.com/pedroslopez/whatsapp-web.js)
* [GitHub](https://github.com/Rex-Arnab/Jarvis_Whatsapp_Bot_2.0)


## Special Thanks to

- [`open-wa/wa-automate-nodejs`](https://github.com/open-wa/wa-automate-nodejs)
- [`YogaSakti/imageToSticker`](https://github.com/YogaSakti/imageToSticker)
- [`SomnathDas/Whatsapp-Botto-Re`](https://github.com/SomnathDas/Whatsapp-Botto-Re)
