# 🛸 ChatHub — Liquid Glass P2P Messenger

Link for the app: https://safirazim-ui.github.io/ChatHUB-APP/

> **Decentralized, Peer-to-Peer Web Messaging with Apple-Inspired Liquid Glass Design System**

ChatHub is an open-source, client-side, zero-knowledge peer-to-peer (P2P) messaging application. Built entirely with vanilla HTML5, JavaScript, and Tailwind CSS, ChatHub requires **no backend server database**—all user credentials, messages, group definitions, and custom themes are persisted directly in the browser's `localStorage` and communicated via direct WebRTC data channels.

---

## 🌟 Key Features

### 💎 1. Apple-Inspired Liquid Glass Visual Engine
* **Frosted Glassmorphism:** Translucent glass slates utilizing `-webkit-backdrop-filter: blur(20px) saturate(160%)` with real-time contrast boosting.
* **Specular Light Reflections:** Multi-layered inset highlights (`inset 0 1px 1px rgba(255,255,255,0.4)`) simulating glass bezel thickness and ambient reflection.
* **Ambient Fluid Orbs:** Dynamic background radial light orbs with smooth keyframe animations that pulse and float beneath glass panels.
* **Compact Geometric Design:** Sharp, high-precision slate edges and tight-fitting text message bubbles without unneeded padding.

### 🔐 2. Decentralized Peer-to-Peer Architecture (WebRTC)
* **Direct Browser Connectivity:** Employs **PeerJS** to establish peer-to-peer WebRTC `DataChannels`.
* **Zero Database Logs:** Messages travel straight between user browsers without intermediary storage or server logging.
* **15-Minute Dynamic Group Links:** Generate auto-expiring temporary invitation URLs with built-in timestamp validation tokens.

### 🌐 3. Multilingual & Theme System
* **Dynamic Language Switcher:** Instant toggling between **English (EN)**, **Spanish (ES)**, and **Catalan (CAT)**.
* **Appearance Themes:**
  * 🌙 **Dark Glass:** Cosmic blue/indigo radial gradients with frosted slate panels.
  * ☀️ **Light Glass:** Vibrant light slate aesthetic with high-contrast readable text.
  * 📜 **Sepia Paper:** Warm retro theme with rich brown typography.
* **Custom Backgrounds:** Apply custom wallpaper image URLs on demand.

### 📱 4. Local Storage & Desktop/Mobile PWA
* **Instant Persistence:** All contacts, conversations, active settings, and theme preferences sync immediately to `localStorage`.
* **PWA Support:** Install ChatHub on mobile or desktop as a standalone app, featuring a custom 3D translucent glass cube favicon.
* **Context Actions:** Native right-click context menu on sidebar chats allowing quick **Rename** and **Delete** actions.

---

## 🚀 Quick Start & Installation

### Option 1: Direct File Usage (No Build Required)
Because ChatHub is built as a single, self-contained HTML/JS/CSS application, you don't need `npm`, Node.js, or complex compilation tools.

1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/chathub.git
   cd chathub
   ```
2. Open `index.html` directly in any modern browser (Chrome, Safari, Firefox, Edge, Brave):
   ```bash
   # On macOS
   open index.html

   # On Linux
   xdg-open index.html

   # On Windows
   start index.html
   ```

### Option 2: Serve Locally with Web Server
To test P2P WebRTC data transfer across different devices on the same network:

```bash
# Using Python 3
python3 -m http.server 8080

# Using Node.js npx
npx serve .
```
Then navigate to `http://localhost:8080` in your web browser.

---

## 🛠️ System Architecture & Data Flow

```
+-------------------+                           +-------------------+
|   User A Browser  |                           |   User B Browser  |
|  (Local Data Only)| <=======================> |  (Local Data Only)|
+-------------------+    Encrypted WebRTC P2P   +-------------------+
          |                DataChannel                    |
          v                                               v
   [ LocalStorage ]                                [ LocalStorage ]
   - User Credentials                              - User Credentials
   - Saved Chats                                   - Saved Chats
   - Preferences                                   - Preferences
```

### LocalStorage Schema Reference:
ChatHub stores its persistent state under the following keys:

| Key | Description | Example / Default |
| :--- | :--- | :--- |
| `chathub_userid` | Unique local PeerJS identifier | `user_k9a2f1x` |
| `chathub_name` | User display name | `User k9a2f1` |
| `chathub_lang` | Preferred interface language | `'en'` \| `'es'` \| `'ca'` |
| `chathub_theme` | Visual appearance theme | `'dark'` \| `'light'` \| `'sepia'` |
| `chathub_chats` | Serialized chat conversations array | `JSON Array` |
| `chathub_visited` | First-time onboarding flag | `'true'` |

---

## 📖 How to Use ChatHub

### 1. Connecting to a Friend
1. Launch ChatHub on your browser.
2. Locate your **Peer ID** in the top left under your display name (e.g., `ID: user_x82f91`). Click it to copy it to your clipboard.
3. Share your Peer ID with a friend.
4. Once your friend sends a message using your ID, a new direct chat channel will automatically open.

### 2. Creating a Group Chat
1. Click the **Group Add** icon (`group_add`) in the top sidebar header.
2. Enter your desired Group Name in the pop-up modal.
3. Click **Create Group**.

### 3. Managing Chats
* **Right-Click Menu:** Right-click on any chat item in the sidebar list to open the context menu:
  * ✏️ **Rename Chat:** Change the display title of the group or contact locally.
  * 🗑️ **Delete Chat:** Remove the conversation history from your device.

---

## 💻 Tech Stack

* **Frontend Engine:** HTML5, Modern ES6+ JavaScript.
* **Styling & Layout:** Tailwind CSS (via CDN) + CSS3 Custom Properties & Glassmorphism Backdrop Filters.
* **P2P Networking:** [PeerJS](https://peerjs.com/) (WebRTC abstraction framework).
* **Iconography & Fonts:** Material Symbols Outlined & Inter font family.

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.
