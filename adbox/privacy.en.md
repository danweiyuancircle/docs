# ADBox · Privacy Policy

Effective date：2026-09-08

This Privacy Policy explains how ADBox (the "App"), developed by 单位圆的日常 ("we", "us"), handles your information. Please read it carefully before using the App. By continuing to use the App, you acknowledge and agree to this policy.

## 1. Core Principle: Local-Only Client, No Backend

The App is a debugging tool that runs locally on your iOS device to manage your own target devices (such as smart TVs / TV boxes). **We have no server and operate no backend.** All operations happen directly between your devices and your own target devices over the same local network.

- We **do not collect, upload, or store** any of your personal information on our servers (we have none).
- The App contains **no advertising, analytics, or crash-reporting third-party data-collection SDKs**, and performs no network telemetry or behavioral tracking of any kind.
- All data produced while using the App (device list, caches, logs, screenshots, transferred files, etc.) is **stored solely on your local devices**.

## 2. About the Local Plugin (Important)

To enable fast and reliable device operations, the App bundles a small plugin (an APK) that is installed via ADB onto **your own target device** on first connection and runs locally there. Please note:

- **It runs entirely locally.** The plugin starts a local service on your target device that listens only on the local network and accepts direct connections only from your iOS device.
- **It does not access the internet.** The plugin makes no network requests to any external server and reports no telemetry. It only executes the local debugging commands you initiate through the App (screenshots, reading device info, installing/uninstalling apps, file transfer, running shell commands, etc.).
- **It is protected by a random key.** Each iOS device generates its own random access token (stored in the iOS Keychain); the plugin responds only to requests carrying the correct token, preventing unauthorized access from other devices on the same network.
- You can uninstall the plugin from within the App at any time.

## 3. How the App Handles Your Data

All data flows are direct local-network connections between "your iOS device ↔ your own target device," passing through no third-party server:

| Data | Purpose | Stored | Uploaded |
| --- | --- | --- | --- |
| Device list (IP / port / alias) | Reconnect saved devices | App sandbox (local) | No |
| Access token | Plugin authentication | System Keychain (local) | No |
| App list / device info cache | Offline viewing & speed-up | Cache directory (local) | No |
| Screenshots | Saved to your album if you choose | Your album (your choice) | No |
| File transfer | Files you move between devices | On your devices | No (direct peer-to-peer) |
| Runtime logs | Troubleshooting | Local log files | No (leaves device only when you export & share) |
| Preferences | Remember your settings | App sandbox (local) | No |

Uninstalling the App removes all of the above local data.

## 4. Permissions

The App requests only the minimum permissions needed for its features:

- **Local Network**: to discover and connect to your target devices on the same local network. This is required to reach your own devices and is not used for internet access.
- **Add to Photos**: used only when you choose to "save a screenshot," to store the device screenshot in your album.

The App does not request location, contacts, microphone, camera, or other permissions.

## 5. Logs & Feedback

- The App's runtime logs are stored only on your local device and are **never uploaded automatically**.
- Logs leave your device only when you actively use "Export Logs" and choose a sharing channel (e.g., email, AirDrop). The exported content is mainly debugging-command details and public device info (such as OS version); you decide whether to send it to us to help with troubleshooting.
- Information you voluntarily provide when contacting us (such as your email and problem description) is used only to respond to your feedback.

## 6. Third Parties

- **Apple App Store**: handles distribution and any in-app purchases; related account and transaction data are processed by Apple under its own privacy policy, and we cannot access your payment information.
- External links opened by the App (such as help docs or community invites) are launched at your initiative; once opened they are handled by iOS and the destination site, with no data transfer involving the App.
- Apart from the above, the App integrates no other third-party services.

## 7. Your Rights

All your data stays local. You may delete devices, clear caches, or uninstall the App at any time to remove all local data. To delete content you voluntarily sent us via feedback, contact us at the email below.

## 8. Policy Updates

We may update this policy from time to time. Significant changes will be highlighted prominently on this page. The effective date shown at the top prevails.

## 9. Contact Us

If you have any questions about this Privacy Policy, please email tianxiake1994@gmail.com.

## Appendix: Third-Party Open Source Components

The App directly uses the following open-source components whose licenses require attribution:

1. KeyboardShortcuts 3.0.1
 License: MIT
 Copyright (c) Sindre Sorhus
 https://github.com/sindresorhus/KeyboardShortcuts/blob/3.0.1/license

2. SwiftTerm 1.10.1
 License: MIT
 Copyright (c) 2019-2022 Miguel de Icaza
 https://github.com/migueldeicaza/SwiftTerm/blob/v1.10.1/LICENSE

3. scrcpy Server 4.1 (bundled with the App, run only on the user's own TV device)
 License: Apache-2.0
 Copyright Genymobile
 https://github.com/Genymobile/scrcpy/blob/v4.1/LICENSE
