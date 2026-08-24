# P2P Exchange Calculator

> **Live Demo:** [https://sarakmacbook.github.io/p2p_exchange_calculator](https://sarakmacbook.github.io/p2p_exchange_calculator)  
> **GitHub Repo:** [https://github.com/sarakmacbook/p2p_exchange_calculator](https://github.com/sarakmacbook/p2p_exchange_calculator)

A clean, dark-themed calculator for converting **Iraqi Dinar (IQD)** and **US Dollar (USD)** to **USDT**. Built as a single-page static app — fast, mobile-friendly, and works offline after first load.

![screenshot](screenshot.png)

## Features

- **IQD & USD** — switch between Iraqi Dinar and US Dollar
- **Real-time calculation** — updates as you type
- **Quick amount chips** — tap 500K, 1M, 1.5M, 2M (IQD) or 500, 1K, 1.5K, 2K (USD)
- **Scale table** — see conversion for preset amounts at current rate
- **Copy result** — tap the result to copy USDT value
- **Persistent** — remembers your last rate and amount (localStorage)
- **Reset/Clear** — one-tap reset for rate and amount fields
- **PWA-ready** — can be added to home screen on iOS/Android

---

## 🚀 One-Click VPS Install

Copy and paste this **one command** on your VPS:

```bash
curl -sL https://raw.githubusercontent.com/sarakmacbook/p2p_exchange_calculator/main/install.sh | sudo bash
```

> ⚠️ Make sure `install.sh` is uploaded to your repo first!

### Interactive Install (Recommended)

```bash
# 1. Clone the repo
git clone https://github.com/sarakmacbook/p2p_exchange_calculator.git
cd p2p_exchange_calculator

# 2. Run the interactive installer
sudo bash install.sh
```

The installer will **ask you**:

| Step | Question | Default |
|------|----------|---------|
| **1** | Domain (optional) | *(empty = IP only)* |
| **2** | Port | `80` |
| **3** | Web Server — **Nginx** / **Caddy** / **Docker** | `Nginx` |
| **4** | File storage path | `/var/www/iqd-usdt-calc` |

Then shows a **summary** and asks for confirmation before installing.

### Example Session
```
🌐 Step 1: Domain (optional)
   Enter domain [e.g., calc.yoursite.com]: calc.mysite.com

🔌 Step 2: Port
   Enter port [80]: 80

⚙️  Step 3: Web Server
   1) Nginx
   2) Caddy
   3) Docker
   Choose [1/2/3] (default: 1): 1

📁 Step 4: Where to store files
   Enter path [/var/www/iqd-usdt-calc]: 

📋 Installation Summary:
   Domain:    calc.mysite.com
   Port:      80
   Service:   nginx
   Files:     /var/www/iqd-usdt-calc

   Proceed? [Y/n]: Y
```

### Requirements
- Ubuntu/Debian VPS
- Root or sudo access
- The script auto-installs missing dependencies

---

## 🐳 Docker Option

```bash
# Using the interactive installer (choose Docker)
sudo bash install.sh

# Or manually:
docker build -t iqd-usdt-calc .
docker run -d -p 80:80 --name iqd-usdt-calc --restart unless-stopped iqd-usdt-calc
```

---

## 📤 Manual Install (Any Web Server)

Just upload `index.html` to any web server or static hosting:

| Platform | How |
|----------|-----|
| **Nginx** | Copy to `/var/www/html/` |
| **Apache** | Copy to `/var/www/html/` |
| **GitHub Pages** | Enable Pages in repo settings |
| **Cloudflare Pages** | Drag & drop the file |
| **Vercel / Netlify** | Drag & drop or connect repo |

---

## 📝 Usage

1. Enter the **unit price** (IQD or USD per 1 USDT)
2. Enter the **amount** you want to send
3. See the **USDT you receive** at the top
4. Tap result to copy

---

## 📊 Default Rates

| Currency | Default Rate |
|----------|-------------|
| IQD | 14 IQD = 1 USDT |
| USD | 1 USD = 1 USDT |

---

## 🛠️ Tech Stack

- Pure HTML + CSS + JavaScript (no frameworks)
- Single file, zero dependencies
- Mobile-first responsive design
- Dark theme with lime green accents

---

## 📄 License

MIT — free to use, modify, and distribute.
