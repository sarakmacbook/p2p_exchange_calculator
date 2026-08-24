# 💱 P2P Exchange Calculator

> **Live Demo:** [https://sarakmacbook.github.io/p2p_exchange_calculator](https://sarakmacbook.github.io/p2p_exchange_calculator)  
> **GitHub:** [https://github.com/sarakmacbook/p2p_exchange_calculator](https://github.com/sarakmacbook/p2p_exchange_calculator)

A sleek, dark-themed **P2P exchange calculator** for converting **Iraqi Dinar (IQD)** and **US Dollar (USD)** to **USDT**. Built as a single static file — zero dependencies, blazing fast, and fully offline-capable after first load.

![Dark Theme](https://img.shields.io/badge/theme-dark-black?style=flat-square) ![PWA Ready](https://img.shields.io/badge/PWA-ready-c5f000?style=flat-square) ![Zero Dependencies](https://img.shields.io/badge/deps-zero-success?style=flat-square)

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **🔄 Dual Currency** | Switch between **IQD** and **USD** instantly |
| **⚡ Real-time** | Result updates as you type — no submit button |
| **📊 Scale Table** | See preset conversions at your current rate |
| **📋 Tap to Copy** | One tap copies the result |
| **💾 Persistent** | Remembers your last rate & amount (localStorage) |
| **🎯 Quick Chips** | Tap 500K / 1M / 1.5M / 2M for instant input |
| **📱 PWA Ready** | Add to home screen on iOS & Android |
| **🌙 Dark Mode** | Clean black theme with lime green accents |

---

## 🚀 Quick Start

### One-Command VPS Install

```bash
curl -sL https://raw.githubusercontent.com/sarakmacbook/p2p_exchange_calculator/main/install.sh | sudo bash
```

### Clone & Install

```bash
git clone https://github.com/sarakmacbook/p2p_exchange_calculator.git
cd p2p_exchange_calculator
sudo bash install.sh
```

The installer is **fully interactive** — it asks you:
- 🌐 **Domain** (optional, defaults to IP)
- 🔌 **Port** (default: 80)
- ⚙️ **Server** — Nginx / Caddy / Docker
- 📁 **File path** (default: `/var/www/iqd-usdt-calc`)

---

## 🐳 Docker

```bash
docker build -t p2p-calc .
docker run -d -p 80:80 --name p2p-calc --restart unless-stopped p2p-calc
```

Or use the interactive installer and pick **Docker**.

---

## 📤 Manual Deploy

Just upload `index.html` — it works on **any** static host:

| Platform | Method |
|----------|--------|
| **GitHub Pages** | Enable Pages → `main` branch → root |
| **Cloudflare Pages** | Drag & drop |
| **Vercel / Netlify** | Connect repo or drag & drop |
| **Nginx / Apache** | Copy to web root |
| **S3 / GCS / R2** | Upload file |

---

## 🖼️ Screenshots

```
┌─────────────────────────┐
│  Calculator             │
│  [ IQD ] [ USD ]        │
│                         │
│       Receive           │
│     142.86 USDT         │
│  2,000,000 IQD ÷ 14     │
│      tap to copy        │
│                         │
│  Unit price      reset  │
│  14                     │
│  IQD per 1 USDT         │
│                         │
│  Amount send     clear  │
│  2,000,000              │
│  IQD                    │
│                         │
│  [500K][1M][1.5M][2M] │
│                         │
│  Scale at current rate  │
│  500K IQD  →  35.71     │
│  1M IQD    →  71.43     │
│  1.5M IQD  →  107.14    │
│  2M IQD    →  142.86    │
└─────────────────────────┘
```

---

## 📝 Default Rates

| Currency | Rate |
|----------|------|
| **IQD** | 14 IQD = 1 USDT |
| **USD** | 1 USD = 1 USDT |

Tap **reset** to restore defaults.

---

## 🛠️ Tech Stack

- **HTML5** — semantic markup
- **CSS3** — flexbox, custom properties, safe-area insets
- **Vanilla JS** — no frameworks, no build step
- **Single file** — everything in `index.html`
- **Zero dependencies** — no npm, no bundler

---

## 📂 File Structure

```
p2p_exchange_calculator/
├── index.html          # The entire app
├── install.sh          # Interactive VPS installer
├── README.md           # This file
├── Caddyfile           # Caddy server config
├── docker-compose.yml  # Docker Compose setup
└── .gitignore
```

---

## 🤝 Contributing

Pull requests welcome! This is a single-file app — keep it simple.

---

## 📄 License

**MIT** — free to use, modify, and distribute.
