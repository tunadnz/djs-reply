![Image](https://img.shields.io/npm/v/djs-reply?color=)
![Image](https://img.shields.io/npm/dt/djs-reply.svg?color=E2142D&maxAge=3600)
 
#

# Yüklemek İçin
```npm
npm i djs-reply
```

# Örnek Kullanım
```javascript
//----------------------------Main----------------------------\\

const Discord = require('discord.js');
const client = new Discord.Client();
const { lineReply, lineReplyNoMention } = require('djs-reply'); // --> Ek Bir İşlem Yapmanıza Gerek Yok Ana Dosyanıza Bunu Koymanız Yeterli Olacaktır.

//------------------------------------------------------------\\
```

# Örnek Method Kullanımı
```javascript

//-----------------------Örnek-----------------------\\

const Discord = require('discord.js');
const client = new Discord.Client();
const { lineReply, lineReplyNoMention } = require('djs-reply'); // --> Ek Bir İşlem Yapmanıza Gerek Yok Ana Dosyanıza Bunu Koymanız Yeterli Olacaktır.

client.on('ready', () => {
console.log(`${client.user.tag} Olarak Giriş Yaptım!`);
});

client.on('message', (message) => {
if (message.content === '!reply') {
const embed = new Discord.MessageEmbed()
.setDescription(`Wow! Line Reply Message!`);
message.lineReply(embed); // --> Kullanıcıyı Etiketleyerek Mesajı Satır İçine Alır.
message.lineReplyNoMention(embed); // --> Sadece Mesajı Satır İçine Alır.
};
};
});

client.login('TOKEN');

//-----------------------Embed-----------------------\\

if (message.content === '!reply') {
const embed = new Discord.MessageEmbed()
.setDescription(`Wow! Line Reply Message!`);
message.lineReply(embed); // --> Kullanıcıyı Etiketleyerek Mesajı Satır İçine Alır.
message.lineReplyNoMention(embed); // --> Sadece Mesajı Satır İçine Alır.
};

//-----------------------Edit [Async Function]-----------------------\\

if (message.content === '!ping') {
let msg = await message.lineReply('Ping');
let ping = (msg.createdTimestamp - message.createdTimestamp);
msg.edit(`${ping}ms`)
};

//--------------------------------------------------\\
```

# İletişim Bilgilerim
[Discord](https://discord.gg/rVnKDGcRKR) 
