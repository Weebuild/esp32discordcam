# Discord ESP32-CAM Bot

This is a **Discord bot** that connects to an **ESP32-CAM** and sends images to a Discord channel either on-demand (`!armin`, `!admin`) or on a scheduled basis (every 3 hours).  
The bot includes **admin-only commands**, cooldown timers, and scheduled tasks.

---

## ✨ Features

- **Scheduled Captures**: Automatically takes a picture from ESP32-CAM every 3 hours (6, 9, 12, 15, 18, 21, 0).
- **Cooldown System**:  
  - `!armin` has a **30-day cooldown** (global, not per user).  
  - Admins can bypass cooldown using `!admin`.
- **Activation System**:  
  - Bot starts **inactive**.  
  - Use `!please` (admin only) to activate it.  
  - Use `!terminate` (admin only) to deactivate it.
- **Custom Admin IDs**: Only specified users can use `!please`, `!terminate`, and `!admin`.
- **Special Command**: `!GROMBA` sends a fixed image link.

---

## ⚙️ Setup

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
