# What is ChatHub?
1. What It Does
Direct P2P Connections: It uses WebRTC DataChannels (via PeerJS) so messages, voice notes, photos, and videos travel directly from browser to browser without going through a central chat server.

Frosted Liquid Glass Design: Inspired by Apple's iMessage and Material Design 3, featuring translucent glassmorphic blur effects, specular reflections, and animated background lighting.

Group & Private Chats: You can chat one-on-one using unique Peer IDs or create custom Group Chats with admin moderation rights (kicking members, renaming groups).

2. Key Features
15-Minute Group Invite Links: Admins can generate secure, time-stamped dynamic invite links that expire after 15 minutes.

Voice Notes & Media Sharing: Record real-time audio voicemails with visual wave animations and share photos or videos.

Local Storage & Security: All messages, profiles, and media are saved locally in your browser (localStorage). Features optional PIN/password protection with an eye toggle to reveal your key.

Liquid Glass Top Notifications: Displays pop-up liquid glass notification banners at the top of your screen when messages arrive from non-active chats.

Installable PWA: Can be installed directly onto your phone or desktop as a standalone app, complete with its custom 3D isometric glass cube icon.

Multilingual & Custom Themes: Switch seamlessly between English, Spanish, and Catalan, toggle between Light/Dark/Sepia modes, or upload your own custom chat background. (DO NOT SHARE SENSITIVE INFO).

## How does it work?
1. 🌐 Peer-to-Peer (WebRTC) Communication
Unlike traditional chat apps (like WhatsApp or Telegram) that store your messages on central servers, ChatHub relies on WebRTC (Web Real-Time Communication) via PeerJS:

Unique Peer ID: When you launch ChatHub, your browser requests a unique ID from a lightweight handshake server.

Direct Browser Connection: When you enter a friend’s ID, your two browsers establish a direct, encrypted DataChannel.

Zero Server Storage: Messages, voice recordings, photos, and videos travel straight between you and your peer. No central database ever touches or logs your conversations.

2. 🔐 Security & 15-Minute Group Invites
Expiring Group Links: When an admin clicks "Invite Friend" in a group chat, ChatHub generates a tokenized URL containing a dynamic timestamp.

15-Minute TTL (Time-to-Live): Anyone opening the link has 15 minutes to join. After 15 minutes, the link automatically invalidates to keep group chats private and secure.

PIN & Password Lock: You can lock your profile and settings behind a PIN/Password, complete with an eye toggle (visibility) to view or hide your key whenever needed.

3. 🎨 Liquid Glass UI & Dynamic Customization
Material Design 3 & Glassmorphism: Using CSS backdrop blurs (backdrop-filter: blur(28px)), specular edge lighting, and ambient light orbs, the app creates a frosted liquid glass texture for menus, notifications, and chat bubbles.

Dynamic Color-Coded Group Bubbles: In group chats, every participant gets a custom color badge with their name and avatar attached directly to their grey liquid glass bubbles.

Themes & Backgrounds: You can toggle between Light, Dark, Sepia, or Device Auto modes, or upload your own wallpaper.

4. 📱 Progressive Web App (PWA) & Local Storage Persistence
LocalStorage System: All your active chats, settings, saved profiles, and message histories serialize directly into your browser's localStorage.

Installable App: Click the Install App button to install ChatHub directly to your home screen or desktop operating system with its custom 3D isometric glass cube icon.

## How does it look like?

