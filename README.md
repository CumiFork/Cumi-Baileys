<h1 align='center'><img alt="Cumi-Baileys logo" src="https://raw.githubusercontent.com/CumiFork/Cumi-Baileys/main/Media/logo.png" height="150"/></h1>

<div align='center'><b>Cumi-Baileys is a custom fork of Baileys, adding Album, Interactive, Rich Response, & Keep Chat features.</b></div>

> [!IMPORTANT]
> This is a customized fork based on [WhiskeySockets/Baileys](https://github.com/WhiskeySockets/Baileys). It includes modern WhatsApp message structures that are not available in the upstream library (such as Albums, Rich Responses, and Native Flows).

## ✨ Fitur Eksklusif Cumi-Baileys

- 🖼️ **Album Message**: Kirim beberapa foto/video sekaligus dalam satu album.
- 🔘 **Interactive Message**: Support Native Flow (Button v2, URL, dll).
- 📊 **Rich Response**: Kirim pesan dengan format Code Block, Table, dan Inline Entities.
- 📌 **Keep Chat**: Fitur centang kuning (Keep in Chat).
- 🔔 **Mention All**: Tag semua member grup dengan mudah.
- 🔑 **Custom Pairing Code**: Bisa input kode custom pas pairing (misal: `CUMI1234`).
- 🤖 **External Ad Reply & Wrappers**: Dukungan `externalAdReply`, `viewOnce`, `spoiler`, `ephemeral`.

---

## 💡 Contoh Penggunaan Fitur Baru

### 1. Kirim Interactive Message (Button & Native Flow)
```javascript
await sock.sendMessage(jid, {
  interactive: {
    header: '🦑 Cumi-Baileys',
    body: 'Silakan pilih menu di bawah:',
    footer: 'Powered by Cumi',
    buttons: [
      { name: 'quick_reply', params: { display_text: 'Ping', id: 'ping' } },
      { name: 'cta_url', params: { display_text: 'Google', url: 'https://google.com' } }
    ]
  }
})
