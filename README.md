# KlokAI Chat Automation 🚀

A terminal-based automation tool for KlokApp AI chat with session token authentication and a resilient retry mechanism.

---

## ✨ Features

- **🔑 Session Token Authentication** - Direct login using KlokApp session token
- **📊 Interactive Dashboard** - Beautiful terminal UI with `blessed` and `blessed-contrib`
- **🤖 Automated Prompts** - Generate creative prompts using Groq API
- **⏳ Rate Limit Management** - Automatic cooldown when limits are reached
- **📌 Point Tracking** - Real-time monitoring of inference points
- **🔄 Automatic Retry** - Handles network and server errors
- **📡 Stream Verification** - Ensures successful message delivery
- **🌐 Proxy Support** - Uses user-provided proxy if available, defaults to system IP otherwise
- **📜 Detailed Logging** - Comprehensive monitoring and debugging

---

## 📂 Directory Structure

```
klokapp-automation/
├── package.json         # Project dependencies
├── session-token.key    # Session token for login (required)
├── groq-api.key         # Groq API key
├── proxies.txt          # Proxy configuration (optional)
├── info.log             # Log file for monitoring
├── index.js             # Main entry point
├── config.js            # App configuration
└── src/
    ├── api/             # KlokApp API functions
    ├── ui/              # UI components
    ├── services/        # External services
    └── utils/           # Utilities
```

---

## 🛠️ Installation

### 🔹 Linux/macOS

1️⃣ Open a terminal and clone the repository:
   ```sh
   git clone https://github.com/rpchubs/Klok-BOT.git
   cd Klok-BOT
   ```

2️⃣ Install dependencies:
   ```sh
   npm install
   ```

3️⃣ Configure **Proxy**:
   - Open `proxies.txt` using nano:
     ```sh
     nano proxies.txt
     ```
   - Add your proxy in the format:
     ```sh
     http://username:password@ip:port
     ```
   - Example:
     ```sh
     http://user123:pass456@192.168.1.1:8080
     ```
   - If `proxies.txt` is empty or missing, the application will use your default system IP.
   - Save the file (`CTRL + X`, then `Y`, then `Enter`).

4️⃣ Configure **Session Token**:
   ```sh
   nano session-token.key
   ```
   - Paste your `session_token` and save the file.

5️⃣ Register for **Groq API Key**:
   - Visit [Groq Console](https://console.groq.com/login) and create an account.
   - Copy your **API key** and save it:
     ```sh
     nano groq-api.key
     ```
   - Paste your API key and save the file.

## - Create session
```sh
     screen -S Klok
```

6️⃣ Run the application:
   ```sh
   npm run start
   ```


---

## 🔐 Setting Up Session Token

1️⃣ **Login to KlokApp** in your browser.
2️⃣ Open **Developer Tools** (`F12` or `Ctrl + Shift + I`).
3️⃣ Navigate to **Application** > **Local Storage** > `https://klokapp.ai`.
4️⃣ Find and copy the `session_token` value.

📌 **Example Screenshot:**

![Session Token Guide](assets/session-token-guide.png)

---

## 🎛️ Running the Automation

Start the script:
```sh
npm start
```

### 🎮 Keyboard Controls

- `S` - Start automation (requires session-token.key)
- `P` - Pause automation
- `R` - Resume automation
- `L` - Clear log file
- `I` - Show file information
- `H` - Show help
- `Q` or `Esc` - Quit application

---

## 📜 Logging & Error Handling

- **Automatic Retry** - Retries on network/server failures.
- **Exponential Backoff** - Increases wait time on consecutive failures.
- **Error Logging** - Logs all failures for debugging.
- **Automatic Recovery** - Resumes when conditions are normal.

---

## 🛠️ Additional Commands

To clear the log file:
```sh
npm run clear-logs
```

---

## 🔗 Useful Links 🌍

- [Github Repository](https://github.com/rpchubs)
- [KlokAI](https://klokapp.ai?referral_code=GVJRESB4)
- [Groq Console](https://console.groq.com/login)

---

🚀 **Happy Botting!** 🎯
