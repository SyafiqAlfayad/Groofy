
# WhatsApp Voice Bot for Koyeb Deployment

This bot uses `whatsapp-web.js` to interact with WhatsApp via web automation.

## Deployment on Koyeb

Make sure the following are available on your runtime:
- Node.js >= 16
- `ffmpeg` and `yt-dlp` available as command line tools

### Deploy steps
1. Upload the zip file to a GitHub repository or deploy directly from ZIP.
2. Set the build command: `npm install`
3. Set the run command: `npm start`

## Session Persistence (Keep Login History)

To preserve login session between restarts on Koyeb:

- Mount a Koyeb volume to `/app/session`
- This folder is used to store the WhatsApp login session (so you only scan QR once)

Example setup (Koyeb Dashboard):
- Volume path: `/app/session`
- Volume name: `whatsapp-session-storage`

Enjoy your bot!
