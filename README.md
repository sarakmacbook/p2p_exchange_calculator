# IQD → USDT Calculator

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

## 🚀 One-Click VPS Install (Interactive)

```bash
# 1. Upload the project folder to your VPS
# 2. Run the installer
cd iqd-usdt-calc
sudo bash install.sh
```

The installer will **ask you**:
1. **Domain** (optional) — e.g. `calc.yoursite.com` or leave blank for IP
2. **Port** — default `80`, or choose any custom port
3. **Web Server** — pick one:
   - **Nginx** — Fast, battle-tested, default choice
   - **Caddy** — Auto HTTPS, simple config
   - **Docker** — Containerized, portable
4. **File location** — where to store the HTML file (default: `/var/www/iqd-usdt-calc`)

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

## 🐳 Docker Option

```bash
# Using the interactive installer (choose Docker)
sudo bash install.sh

# Or manually:
docker build -t iqd-usdt-calc .
docker run -d -p 80:80 --name iqd-usdt-calc --restart unless-stopped iqd-usdt-calc
```

## 📤 Manual Install (Any Web Server)

Just upload `index.html` to any web server or static hosting:

| Platform | How |
|----------|-----|
| **Nginx** | Copy to `/var/www/html/` |
| **Apache** | Copy to `/var/www/html/` |
| **GitHub Pages** | Enable Pages in repo settings |
| **Cloudflare Pages** | Drag & drop the file |
| **Vercel / Netlify** | Drag & drop or connect repo |

## 📝 Usage

1. Enter the **unit price** (IQD or USD per 1 USDT)
2. Enter the **amount** you want to send
3. See the **USDT you receive** at the top
4. Tap result to copy

## 📊 Default Rates

| Currency | Default Rate |
|----------|-------------|
| IQD | 14 IQD = 1 USDT |
| USD | 1 USD = 1 USDT |

## 🛠️ Tech Stack

- Pure HTML + CSS + JavaScript (no frameworks)
- Single file, zero dependencies
- Mobile-first responsive design
- Dark theme with lime green accents

## 📄 License

MIT — free to use, modify, and distribute.
