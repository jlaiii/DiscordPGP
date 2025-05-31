# Discord-Style PGP UI Full (Fixed Save/Load)

A Tampermonkey userscript that adds a Discord-style PGP interface directly inside [discord.com](https://discord.com), enabling you to generate RSA key pairs, manage friends' public keys, and encrypt/decrypt messages securely — all with fixed save/load profile functionality.

---

## Features

- **Discord-themed UI** integrated directly on discord.com
- Generate RSA 2048-bit key pairs for encryption/decryption
- Manage a contact list ("friends") with names and public keys
- Encrypt messages to friends with their public keys
- Decrypt received encrypted messages using your private key
- Copy public keys and encrypted messages with one click
- Edit and delete friends from your contact list
- Save/load your PGP profile (keys, name, friends) locally with fixed persistence
- Lightweight, no external dependencies, runs entirely in-browser
- Easy toggle button to open/close the PGP UI panel

---

## Installation

1. Install a userscript manager extension in your browser, such as:
   - [Tampermonkey](https://www.tampermonkey.net/)
   - [Violentmonkey](https://violentmonkey.github.io/)
   - [Greasemonkey](https://www.greasespot.net/)

2. Create a new userscript and paste the contents of this script.

3. Save and reload discord.com. You should see a **PGP** button at the bottom-right corner.

---

## Usage

### Generate Keys

1. Click the **PGP** button to open the panel.
2. Enter your name and click **Generate Key Pair**.
3. Your public key will appear, and your key pair is saved locally.

### Manage Friends

- Add friends by entering their name and public key, then click **Add Friend**.
- Edit or delete existing friends from the list.
- Copy a friend's public key to share it easily.

### Encrypt Message

1. Select a friend from the dropdown.
2. Type your message in the "Encrypt message" box.
3. Click **Encrypt** to get the encrypted text.
4. Copy the encrypted message and send it securely.

### Decrypt Message

1. Paste an encrypted message into the "Decrypt message" box.
2. Click **Decrypt** to reveal the original message.

### Save and Load Profile

- Use **Save Profile** to store your keys and contacts in browser localStorage.
- Use **Load Profile** to restore your saved data.
- The script automatically loads your profile on page load if saved.

---

## Technical Details

- Uses Web Crypto API for RSA-OAEP 2048-bit key generation and encryption/decryption.
- Stores data locally using `localStorage` under the key `pgpDiscordProfile`.
- UI styled to match Discord's dark theme and user experience.
- Clipboard integration for easy copy-paste of keys and messages.

---

## Permissions

- No special permissions required beyond access to `discord.com`.
- Runs entirely client-side, no data is sent externally.

---

## Contributing

Feel free to open issues or submit pull requests for improvements or bug fixes.

---
