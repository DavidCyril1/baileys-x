# <div align='center'>🚀 Baileys-X</div>

<div align="center">

  <img src="https://files.catbox.moe/jzwzve.png" />

  <a href="https://www.npmjs.com/package/baileys-x">
    <img src="https://img.shields.io/npm/v/baileys-x?color=00ff88&label=Version&logo=npm&style=for-the-badge" alt="npm version" />
  </a>

  <a href="https://www.npmjs.com/package/baileys-x">
    <img src="https://img.shields.io/npm/dt/baileys-x?color=ff6b6b&label=Downloads&logo=npm&style=for-the-badge" alt="npm downloads" />
  </a>

  <a href="https://whatsapp.com/channel/0029VaEe0l9Au3aVRw2x2r0V">
    <img src="https://img.shields.io/badge/WhatsApp-Channel-25D366?logo=whatsapp&logoColor=white&style=for-the-badge" alt="WhatsApp Channel" />
  </a>

  <img src="https://img.shields.io/badge/Powered%20by-Cyril%20Tech-blue?style=for-the-badge&logo=lightning&logoColor=white" alt="Cyril Tech" />

</div>

---

<div align="center">

### ⚡ **The Ultimate WhatsApp API Enhancement** ⚡

*Blazing fast • Feature-rich • Developer-friendly*

**Baileys-X** is the next-generation WhatsApp Web API library that pushes the boundaries of what's possible. Built by **Cyril Tech** with cutting-edge enhancements and modern features.

</div>

---

## 🎯 Quick Navigation

- [⚠️ Important Notice](#️-important-notice)
- [📦 Installation](#-installation)
- [✨ Revolutionary Features](#-revolutionary-features)
- [🔥 Feature Showcase](#-feature-showcase)
  - [📢 Newsletter Management](#-newsletter-management)
  - [🔘 Interactive Messages](#-interactive-messages)
  - [🖼️ Album Messages](#️-album-messages)
  - [🤖 AI Message Icons](#-ai-message-icons)
  - [🔑 Custom Pairing](#-custom-pairing)
- [🐛 Issue Reporting](#-issue-reporting)
- [📝 Important Notes](#-important-notes)

---

## ⚠️ Important Notice

**Baileys-X** represents a revolutionary leap forward from the original Baileys library. While the original repository faced challenges and was eventually maintained by [WhiskeySockets](https://github.com/WhiskeySockets), **Cyril Tech** has completely reimagined the possibilities.

This isn't just a modification—it's a complete evolution that introduces game-changing features and rock-solid performance improvements that weren't even conceptualized in the original codebase.

---

## 📦 Installation

### Quick Start

**Package.json method:**
```json
{
  "dependencies": {
    "baileys-x": "github:nstar-y/bail"
  }
}
```

**Terminal installation:**
```bash
npm install baileys-x@github:nstar-y/bail
```

### Import & Usage

```typescript
// ES Modules (Recommended)
import makeWASocket from 'baileys-x'

// CommonJS
const { default: makeWASocket } = require("baileys-x")
```

---

## ✨ Revolutionary Features

<div align="center">

| 🎭 **Feature** | 🔥 **What Makes It Amazing** |
|:---:|:---|
| **💬 Channel Messaging** | Send rich media and text directly to WhatsApp channels with zero limitations |
| **🔘 Interactive UI** | Create stunning button interfaces and interactive messages that work on both Messenger and Business |
| **🖼️ Album Magic** | Send multiple images as beautiful grouped albums - perfect for storytelling |
| **👥 LID Group Support** | Full compatibility with `@lid` group addressing - future-proof your bots |
| **🤖 AI Message Icons** | Add that premium AI touch to your messages with customizable icons |
| **🖼️ HD Profile Pictures** | Upload full-resolution profile pictures without any quality loss |
| **🔑 Custom Pairing Codes** | Create personalized pairing codes that match your brand |
| **🛠️ Clean Libsignal** | Enjoy crystal-clear logs with our refined libsignal implementation |

</div>

> 🚀 **More revolutionary features are cooking in Cyril Tech's lab!**

---

## 🔥 Feature Showcase

### 📢 Newsletter Management

<details>
<summary>🎯 <strong>Advanced Newsletter Operations</strong></summary>

#### 📊 Get Newsletter Info
```typescript
const metadata = await sock.newsletterMetadata("invite", "xxxxx")
// Alternative method
const metadata = await sock.newsletterMetadata("jid", "abcd@newsletter")
console.log(metadata)
```

#### ✏️ Update Newsletter Details
```typescript
// Update description
await sock.newsletterUpdateDescription("abcd@newsletter", "🔥 New Epic Description")

// Update name
await sock.newsletterUpdateName("abcd@newsletter", "🚀 Cyril Tech Newsletter")

// Update profile picture
await sock.newsletterUpdatePicture("abcd@newsletter", buffer)

// Remove profile picture
await sock.newsletterRemovePicture("abcd@newsletter")
```

#### 🔔 Notification Control
```typescript
// Mute notifications
await sock.newsletterMute("abcd@newsletter")

// Unmute notifications
await sock.newsletterUnmute("abcd@newsletter")
```

#### 🏗️ Newsletter Lifecycle
```typescript
// Create newsletter
const metadata = await sock.newsletterCreate("🔥 Cyril Tech Updates")

// Delete newsletter
await sock.newsletterDelete("abcd@newsletter")

// Follow newsletter
await sock.newsletterFollow("abcd@newsletter")

// Unfollow newsletter
await sock.newsletterUnfollow("abcd@newsletter")
```

#### 🎭 Reactions
```typescript
// React to newsletter message
// Extract ID from URL: https://whatsapp.com/channel/xxxxx/175 (175 is the ID)
const messageId = "175"
await sock.newsletterReactMessage("abcd@newsletter", messageId, "🔥")
```

</details>

### 🔘 Interactive Messages

<details>
<summary>🎨 <strong>Next-Gen Interactive UI</strong></summary>

#### 🔥 Text Buttons
```typescript
const buttons = [
  { buttonId: 'fire', buttonText: { displayText: '🔥 Fire' }, type: 1 },
  { buttonId: 'rocket', buttonText: { displayText: '🚀 Rocket' }, type: 1 }
]

const buttonMessage = {
    text: "🎯 Choose your power-up!",
    footer: '⚡ Powered by Cyril Tech',
    buttons,
    headerType: 1
}

await sock.sendMessage(id, buttonMessage, { quoted: null })
```

#### 🖼️ Image Buttons
```typescript
const buttons = [
  { buttonId: 'awesome', buttonText: { displayText: '😎 Awesome' }, type: 1 },
  { buttonId: 'epic', buttonText: { displayText: '🔥 Epic' }, type: 1 }
]

const buttonMessage = {
    image: { url: "https://example.com/cyril-tech.jpg" },
    caption: "🎨 Interactive image with buttons!",
    footer: '🚀 Cyril Tech Innovation',
    buttons,
    headerType: 1
}

await sock.sendMessage(id, buttonMessage, { quoted: null })
```

#### 🎬 Video Buttons
```typescript
const buttons = [
  { buttonId: 'play', buttonText: { displayText: '▶️ Play' }, type: 1 },
  { buttonId: 'share', buttonText: { displayText: '📤 Share' }, type: 1 }
]

const buttonMessage = {
    video: { url: "https://example.com/cyril-demo.mp4" },
    caption: "🎬 Interactive video experience!",
    footer: '⚡ Cyril Tech Media',
    buttons,
    headerType: 1
}

await sock.sendMessage(id, buttonMessage, { quoted: null })
```

#### 🎭 Advanced Interactive Messages
```typescript
const interactiveButtons = [
     {
        name: "quick_reply",
        buttonParamsJson: JSON.stringify({
             display_text: "⚡ Quick Reply",
             id: "CYRIL_QUICK"
        })
     },
     {
        name: "cta_url",
        buttonParamsJson: JSON.stringify({
             display_text: "🌐 Visit Cyril Tech",
             url: "https://cyril-tech.com/"
        })
     },
     {
        name: "cta_copy",
        buttonParamsJson: JSON.stringify({
             display_text: "📋 Copy Code",
             id: "CYRIL123",
             copy_code: "CYRIL123"
        })
     }
]

const interactiveMessage = {
    text: "🔥 Welcome to Cyril Tech!",
    title: "🚀 Interactive Experience",
    footer: "⚡ Powered by Baileys-X",
    interactiveButtons
}

await sock.sendMessage(id, interactiveMessage, { quoted: null })
```

#### 📋 Interactive Lists
```typescript
const interactiveButtons = [
  {
    name: "single_select",
    buttonParamsJson: JSON.stringify({
      title: "🎯 Select Your Option",
      sections: [
        {
          title: "🔥 Cyril Tech Services",
          highlight_label: "⭐ Premium",
          rows: [
            {
              header: "🚀 DEVELOPMENT",
              title: "Custom Solutions",
              description: "Tailored tech solutions for your needs",
              id: "CYRIL_DEV"
            },
            {
              header: "🎨 DESIGN",
              title: "UI/UX Excellence",
              description: "Beautiful and functional designs",
              id: "CYRIL_DESIGN"
            }
          ]
        }
      ]
    })
  }
];

const interactiveMessage = {
    text: "🌟 Choose your Cyril Tech service!",
    title: "🏆 Premium Services",
    footer: "⚡ Quality guaranteed",
    interactiveButtons
};

await sock.sendMessage(id, interactiveMessage, { quoted: null });
```

</details>

### 🖼️ Album Messages

<details>
<summary>📸 <strong>Stunning Media Albums</strong></summary>

```typescript
// Create beautiful media albums
const media = [
  {
    image: { url: "https://example.com/cyril-tech-1.jpg" }
  },
  {
    image: await getBuffer("https://example.com/cyril-showcase.jpg")
  },
  {
    video: { url: "https://example.com/cyril-demo.mp4" }
  }
]

await sock.sendMessage(id, { 
    album: media, 
    caption: "🎨 Cyril Tech Portfolio - Where Innovation Meets Excellence!" 
}, { quoted: null })
```

</details>

### 🤖 AI Message Icons

<details>
<summary>🎭 <strong>AI-Powered Message Enhancement</strong></summary>

```typescript
// Add that premium AI touch to your messages
await sock.sendMessage(id, { 
    text: "🤖 Hello! I'm powered by Cyril Tech's AI technology!", 
    ai: true 
});
```

</details>

### 🔑 Custom Pairing

<details>
<summary>🎯 <strong>Branded Pairing Experience</strong></summary>

```typescript
if(usePairingCode && !sock.authState.creds.registered) {
    const phoneNumber = await question('📱 Enter your mobile number:\n');
    // Create your custom branded pairing code
    const customPairingCode = "CYRILTECH";
    const code = await sock.requestPairingCode(phoneNumber, customPairingCode);
    console.log(`🔑 Your Cyril Tech Pairing Code: ${code?.match(/.{1,4}/g)?.join('-') || code}`);
}
```

</details>

---

## 🐛 Issue Reporting

Found a bug or have a feature request? **Cyril Tech** is here to help!

🔗 **[Report Issues Here](https://github.com/DavidCyril1/baileys-x/issues)**

Our team monitors issues 24/7 and provides lightning-fast responses!

---

## 📝 Important Notes

**Baileys-X** maintains full backward compatibility with the original Baileys library while adding revolutionary new features. Everything from the original repository works seamlessly, but now with **Cyril Tech's** premium enhancements.

**Original Repository:** [WhiskeySockets/Baileys](https://github.com/WhiskeySockets/Baileys)

---

<div align="center">

### 🎉 **Ready to Build Something Amazing?**

**Baileys-X** by **Cyril Tech** is your gateway to creating next-generation WhatsApp experiences!

---

*Built with ❤️ by [Cyril Tech](https://david-cyril.net.ng) • Making the impossible, possible*

</div>
# baileys-x
