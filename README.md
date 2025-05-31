# Discord-Style PGP UI for Tampermonkey

A lightweight **PGP (Pretty Good Privacy)** user interface inspired by Discord's style — fully client-side, runs as a Tampermonkey userscript on [discord.com](https://discord.com).

---

## Features

- Generate RSA 2048-bit public/private key pair in-browser  
- Manage friends (contacts) with public keys: add, edit, delete  
- Encrypt messages to friends using their public keys  
- Decrypt messages using your private key  
- Copy friend’s public key easily  
- Save your entire profile (keys + friends) as a JSON file by downloading it  
- Load your profile by uploading a JSON file  
- Clean, Discord-like UI with togglable panel on the page  

---

## Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/) (or a similar userscript manager) in your browser.  
2. Create a new userscript and paste the entire script code into it.  
3. Save the script and navigate to [discord.com](https://discord.com).  
4. Click the **PGP** button at the bottom right to open the UI.

---

## Usage

- **Generate Key Pair:** Enter your name and click "Generate Key Pair".  
- **Add Friend:** Enter friend’s name and their public key, then click "Add Friend".  
- **Encrypt Message:** Select a friend, enter a message, and click "Encrypt". The encrypted message will appear below.  
- **Decrypt Message:** Paste an encrypted message and click "Decrypt" to see the plaintext.  
- **Save Profile:** Click "Save Profile (Download)" to download your keys and contacts as a JSON file.  
- **Load Profile:** Click "Load Profile (Upload)" to upload a previously saved JSON profile.

---

## Security Notice

- All cryptographic operations happen **locally in your browser**; no data is sent anywhere.  
- Keep your private key safe and never share it.  
- The profile JSON contains your private key and friends’ public keys — treat it securely.

---

## How it works

- Uses the Web Crypto API for RSA-OAEP key generation, encryption, and decryption.  
- Saves and loads profile as JSON files via browser download/upload (no `localStorage`).  
- UI styled with embedded CSS mimicking Discord’s color scheme.

---

## Development & Contributions

Feel free to fork and customize this script. Pull requests and issues are welcome!
