# Mobile Access - PhotoDewey Extension

Browse and upload photos in your PhotoDewey library from your phone. Pair once
with a QR code; after that your phone connects directly to your PC with no cloud
storage involved.

---

## Features

- Scan a QR code in PhotoDewey Settings to pair your phone with your library
- Browse folders and albums, view photos at full resolution
- Download photos to your phone
- Upload photos from your phone directly into a library folder
- Offline-capable PWA: previously viewed thumbnails load without a connection
- No intermediary storage - photos travel directly between your phone and PC

---

## How it works

The mobile app is a Progressive Web App (PWA) served from `photodewey.eu/app/`.
When your phone scans the QR code it gets a one-time session token. After that,
your phone and PC establish a direct peer-to-peer WebRTC connection. Photo data
never passes through the server - only the small signaling messages needed to set
up the connection do.

---

## Setup

1. Install the extension from the PhotoDewey **Extension Shop** (Help > Extension Shop),
   or drop `PhotoDewey.Mobile.dll` into `%AppData%\PhotoDewey\Extensions\` and restart.
2. Open **Settings > Mobile Access**.
3. On your phone, navigate to `https://photodewey.eu/app/` and tap **Pair with QR code**.
4. Point your phone's camera at the QR code shown in Settings.
5. Your phone connects automatically once PhotoDewey is running and the PC is reachable.

---

## Reconnecting

After the initial pairing the session token is saved on your phone. PhotoDewey
reconnects automatically whenever both devices are online. No re-scanning is needed
unless you tap **Forget device** on the phone or regenerate the token in Settings.

---

## Privacy

The photodewey.eu server handles only the WebRTC handshake (SDP offer/answer and
ICE candidates). It never receives, stores, or proxies any photo data. All photos,
thumbnails, and metadata travel directly between your phone and your PC. The session
token is stored only on your phone and in PhotoDewey's settings on your PC.

---

## Plugin Version

1.0
