# dcbotlist.xyz
<a href="https://dcbotlist.xyz/dc" target="_blank"><img src="https://img.devsforum.net/tr/img/h1Z2X3.png" alt="Join our discord" width="256"></a><br>
**Support:** [https://dcbotlist.xyz/dc](https://dcbotlist.xyz/dc) <br>
**NPM:** [npmjs.com/package/dcbotlist-api.js](https://www.npmjs.com/package/dcbotlist-api.js)<br>

## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://dcbotlist.xyz/dc) address.*
- `npm i dcbotlist-api.js`

```js
const vCodes = require("dcbotlist-api.js");
const dbl = new vCodes("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  // console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("859853108292485180");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("701788656695902258")
  console.log(search)
  /*
  {
    avatar: 'https://cdn.discordapp.com/avatars/701788656695902258/8cf145d2189d76cc110101b7a69c6b20.webp',
    botID: '701788656695902258',
    username: 'DCBotlist',
    discrim: '4473',
    shortDesc: 'Cheer up your own server with 🎶',
    prefix: '! [changable]',
    votes: 1,
    ownerID: '267604752764764160',
    owner: 'Claudette',
    coowners: [ '' ],
    tags: [ 'Moderation', 'NSFW', 'Music' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});
```

