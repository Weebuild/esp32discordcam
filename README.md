Got it 👍 here’s the entire README.md as one single Markdown block — no splitting, everything continuous:

# Discord ESP32-CAM Bot

This is a Discord bot that connects to an ESP32-CAM and sends images to a Discord channel either on-demand (!armin, !admin) or on a scheduled basis (every 3 hours). The bot includes admin-only commands, cooldown timers, and scheduled tasks.

## ✨ Features
- Scheduled Captures: Automatically takes a picture from ESP32-CAM every 3 hours (6, 9, 12, 15, 18, 21, 0).
- Cooldown System:  
  - !armin has a 30-day cooldown (global, not per user).  
  - Admins can bypass cooldown using !admin.
- Activation System:  
  - Bot starts inactive.  
  - Use !please (admin only) to activate it.  
  - Use !terminate (admin only) to deactivate it.
- Custom Admin IDs: Only specified users can use !please, !terminate, and !admin.
- Special Command: !GROMBA sends a fixed image link.

## ⚙️ Setup
Clone the Repository:
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

Install Dependencies:

pip install -r requirements.txt

Configure the Bot by editing main.py:

Bot Token:

TOKEN = 'YOUR TOKEN HERE'

ESP32-CAM URL:

ESP32_URL = 'http://YOUR-ESP32-IP/capture'

If you have IP-forwarded your ESP32-CAM, replace with your network’s public IPv4 address.

Target Discord Channel ID:

target_channel_id = 123456789012345678

Admin User IDs:

ADMIN_USER_IDS = {123456789012345678, 987654321098765432}

▶️ Running the Bot

python main.py

Once running, the bot will:
	•	Stay inactive until !please is issued by an admin.
	•	Reset internal states daily.
	•	Capture images automatically if active.

📜 Commands

Command	Access	Description
!please	Admin	Activates the bot.
!terminate	Admin	Deactivates the bot.
!armin	Everyone	Captures an image (30-day cooldown).
!admin	Admin	Captures an image without cooldown.
!GROMBA	Everyone	Sends a fixed image link.

🛠️ Requirements
	•	Python 3.8+
	•	discord.py
	•	requests

Install dependencies with:

pip install -r requirements.txt

requirements.txt should look like this:

discord.py
requests

📌 Notes
	•	The bot will not accept commands until activated with !please (admin only).
	•	Cooldowns are global (applies to all users).
	•	Make sure your ESP32-CAM is accessible from the machine running the bot.
