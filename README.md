# MTProto Manager

یک اسکریپت ساده و کاربردی برای نصب و مدیریت پروکسی MTProto تلگرام روی سرور اوبونتو.

---

## English

A lightweight, one-command installer and management panel for MTProto Proxy on Ubuntu servers.

### Features

- **One-command installation** - Just run the script and everything is set up automatically
- **Interactive management panel** - Add/remove proxies, change port, Fake-TLS domain
- **Auto-generated secrets** - Or use your own 32-character hex secrets
- **TLS伪装** - Uses Fake-TLS to mimic regular HTTPS traffic
- **Per-user limits** - Data quota (GB) and max simultaneous connections
- **Sponsor channel support** - Connect to Telegram's official MTProto bot for promotion
- **Systemd service** - Runs automatically on boot, with automatic restart on failure

### Requirements

- Ubuntu (or Debian-based) server
- Root/sudo access
- Python 3, git, curl (auto-installed)

### Installation

```bash
bash <(curl -s https://raw.githubusercontent.com/winston-hub/mtproto/main/mtproto-manager.sh)
```

Or download and run manually:

```bash
wget https://github.com/winston-hub/mtproto/raw/main/mtproto-manager.sh
chmod +x mtproto-manager.sh
sudo bash mtproto-manager.sh
```

### Usage

After installation, just run:

```bash
mtproto-manager
```

You'll see an interactive menu:

```
=== MTProto Proxy Manager ===
1) Create new proxy
2) Show all proxies and links
3) Remove a proxy
4) Change port (global)
5) Change Fake-TLS domain (global)
6) Set/remove sponsor channel
7) Restart service
0) Exit
```

### How to get the proxy link

1. Run `mtproto-manager`
2. Choose option 2 to show all proxies
3. Copy the generated link (format: `https://t.me/proxy?...`)
4. Paste it in Telegram app → Settings → Proxy

### Technical Details

- Based on [alexbers/mtprotoproxy](https://github.com/alexbers/mtprotoproxy)
- Installs to `/opt/mtprotoproxy`
- Management panel at `/usr/local/bin/mtproto-manager`
- State file at `/opt/mtprotoproxy/manager_state.json`
- Runs as systemd service named `mtprotoproxy`

---

## فارسی

مدیریت آسان پروکسی MTProto تلگرام روی سرور اوبونتو.

### امکانات

- **نصب با یک دستور** - فقط اسکریپت رو اجرا کنید، همه چیز خودکار انجام میشه
- **پنل مدیریت تعاملی** - اضافه/حذف پروکسی، تغییر پورت و دامنه Fake-TLS
- **تولید خودکار کلید** - یا از کلید دلخواه ۳۲ کاراکتری هگز استفاده کنید
- **پشتیبانی از TLS جعلی** - ترافیک شبیه HTTPS معمولی به نظر میرسه
- **محدودیت per-user** - تعیین سقف حجم داده (گیگابایت) و تعداد اتصال همزمان
- **پشتیبانی از کانال اسپانسر** - اتصال به ربات رسمی MTProto تلگرام برای تبلیغات
- **سرویس systemd** - اجرای خودکار هنگام بوت با ری‌استارت خودکار در صورت خطا

### پیش‌نیازها

- سرور اوبونتو (یا دبیان‌بیس)
- دسترسی root/sudo
- پایتون ۳، گیت، کرل (خودکار نصب میشه)

### نصب

```bash
bash <(curl -s https://raw.githubusercontent.com/winston-hub/mtproto/main/mtproto-manager.sh)
```

یا دانلود و اجرای دستی:

```bash
wget https://github.com/winston-hub/mtproto/raw/main/mtproto-manager.sh
chmod +x mtproto-manager.sh
sudo bash mtproto-manager.sh
```

### استفاده

بعد از نصب، فقط بزنید:

```bash
mtproto-manager
```

منوی تعاملی ظاهر میشه:

```
=== MTProto Proxy Manager ===
1) Create new proxy           ساخت پروکسی جدید
2) Show all proxies and links نمایش همه پروکسی‌ها و لینک‌ها
3) Remove a proxy             حذف پروکسی
4) Change port (global)       تغییر پورت (سراسری)
5) Change Fake-TLS domain     تغییر دامنه TLS جعلی
6) Set/remove sponsor channel تنظیم/حذف کانال اسپانسر
7) Restart service            ری‌استارت سرویس
0) Exit                       خروج
```

### نحوه استفاده از لینک پروکسی

1. دستور `mtproto-manager` رو بزنید
2. گزینه ۲ رو انتخاب کنید تا لینک‌ها نمایش داده بشه
3. لینک ساخته‌شده رو کپی کنید
4. در تلگرام: **تنظیمات → اتصال → پروکسی** → اضافه کردن پروکسی
5. لینک رو پیست کنید

### جزئیات فنی

- بر پایه [alexbers/mtprotoproxy](https://github.com/alexbers/mtprotoproxy)
- مسیر نصب: `/opt/mtprotoproxy`
- فایل پنل مدیریت: `/usr/local/bin/mtproto-manager`
- فایل اطلاعات: `/opt/mtprotoproxy/manager_state.json`
- سرویس systemd: `mtprotoproxy`

---

## License / مجوز

MIT License