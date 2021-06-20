![Image](https://img.shields.io/npm/v/djs-reply?style=flat-square&color=5865F2)
![Image](https://img.shields.io/npm/dt/djs-reply.svg?style=flat-square&color=5865F2&maxAge=3600)

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
const { lineReply, lineReplyNoMention } = require('djs-reply');
// --> Ek Bir İşlem Yapmanıza Gerek Yok Ana Dosyanıza Tanımlamanız Yeterli Olacaktır.

//------------------------------------------------------------\\
```

# Örnek Method Kullanımı
```javascript
//-----------------------Örnek-----------------------\\

const Discord = require('discord.js');
const client = new Discord.Client();
const { lineReply, lineReplyNoMention } = require('djs-reply');

client.on('message', (message) => {
if (message.content === '!lineReply') {
const embed = new Discord.MessageEmbed()
.setDescription(`Vay Canına! Bu Bir Satır İçine Alınmış Mesaj!`);
message.lineReply(embed); // --> Kullanıcıyı Etiketleyerek Mesajı Satır İçine Alır.
message.lineReplyNoMention(embed); // --> Sadece Mesajı Satır İçine Alır.
};
};
});

client.login('TOKEN');

//-----------------------Manual Reply Örnek-----------------------\\

const Discord = require('discord.js');
const client = new Discord.Client();
const { manualReply, manualReplyNoMention } = require('djs-reply');

client.on('message', (message) => {
if (message.content === '!manualReply') {
manualReply(message, 'Vay Canına! Bu Bir Manuel Satır İçine Alınmış Mesaj!'); 
// --> Kullanıcıyı Etiketleyerek Mesajı Satır İçine Alır.

manualReplyNoMention(message, 'Vay Canına! Bu Bir Manuel Satır İçine Alınmış Mesaj!'); 
// --> Sadece Mesajı Satır İçine Alır.
};
};
});

client.login('TOKEN');

//---------------------------------------------------\\
```

# İletişim Bilgilerim
[Discord](https://discord.gg/rVnKDGcRKR) 
