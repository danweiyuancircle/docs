# Connecting adb with ADBox, and Common Questions

## Video tutorials

Open a cover or platform link to watch the video. Videos do not play inline on this GitHub documentation page.

### adb wireless debugging for Android 11+ devices

[![adb wireless debugging for Android 11+ devices](assets/cover-wireless-adb.jpg)](https://www.bilibili.com/video/BV1ZET16GEhB/)

[Bilibili](https://www.bilibili.com/video/BV1ZET16GEhB/) · [YouTube](https://www.youtube.com/watch?v=TMlN1gav29w)

### Connect adb to Android TV

[![Connect adb to Android TV](assets/cover-android-tv.jpg)](https://www.bilibili.com/video/BV1cgT16UEt1/)

[Bilibili](https://www.bilibili.com/video/BV1cgT16UEt1/) · [YouTube](https://www.youtube.com/watch?v=X3JGCyyR2jw)


## Prerequisites

Phone and TV are on the **same LAN (same Wi-Fi)**, network/ADB debugging is enabled on the TV and it allows this device to debug, and the router has no AP isolation / guest-network isolation.

| Port | Purpose |
| --- | --- |
| `5555` | ADB network debugging port — used for the first-time handshake/authorization and plugin install |

## Enable ADB on the TV / set-top box

Entry points differ by vendor. On the TV, enable **ADB network debugging** (wireless debugging, not USB debugging) per the table below:

| Brand | How to enable (reference) |
| --- | --- |
| Generic Google TV | Settings → System → About → tap Build number 7 times → Developer options → enable USB debugging & Wireless debugging |
| Xiaomi / Redmi | Settings → About → press OK on the model name 6–8 times → Account & Security → ADB debugging |
| Hisense / Vidda | My Apps → VIDDA Assistant → TV debugging authorization (or Developer mode) |
| TCL / FFALCON | Settings → System → System info → press D-pad arrows → enable Network debugging |
| Skyworth / Coocaa | Settings → Device info → D-pad Up Up Down Down Left Right Left Right → enable ADB |
| Changhong / Konka / OPPO / Sony | Enter factory menu or Developer mode, then enable network ADB |
| Tmall Box (Alibaba) | Enter System settings → D-pad Down→Right→Left→Up→Down→Right→Left→Up → enable ADB debugging |
| Huawei / Honor (HarmonyOS) | HarmonyOS uses hdc instead of standard ADB; some models disable TCP debugging out of the box and may not be supported |

After enabling debugging on the TV, note its **IP address** (in the TV's Network settings) — you'll need it on the phone in the next step.

## Connect from the phone (ADB)

### First-time connection (full flow)

1. Open the app on your phone, tap **New** on the home screen, enter the TV's **IP address** and port (default `5555`), then tap Connect.
2. **Establish connection**: handshake with the TV over ADB. On first connect the TV shows an authorization dialog — choose **Always allow** and confirm on the TV.
3. **Install accelerator plugin**: the app pushes a bundled plugin APK to the TV and installs it, showing live progress.
4. **Ready**: the plugin starts and the fast channel becomes ready; you enter the control screen and the device is saved to the home list.

### Reconnecting (fast channel)

1. Tap a saved TV on the home screen.
2. The app auto-detects the device status; if the fast channel responds and the plugin version matches → **you go straight to the control screen, no re-authorization or reinstall**.
3. If the fast channel misses (TV asleep / IP changed) → it falls back to the full ADB flow and reconnects automatically while authorization is still valid.

### Editing a saved device

Long-press a device on the home screen → the edit panel lets you change its name, IP, and port → save to reconnect at the new address.

**Port unreachable** ("cannot reach ADB port") guides you to enable debugging on the TV; **authorization rejected** keeps you on the connection page to approve on the TV — don't confuse the two.

## FAQ

Most failures come from three causes: debugging not enabled on the TV, not on the same LAN, or the IP changed. Check the items below first.

### Can't connect / "cannot reach ADB port"?

1. Confirm network/ADB debugging is enabled on the TV (see the brand table above).
2. Make sure the phone and TV are on the **same Wi-Fi / LAN**, and the router has no AP isolation / guest-network isolation.
3. Make sure the IP hasn't changed (it may change after the TV reboots or rejoins Wi-Fi); recheck it in the TV's network settings.
4. The default port is `5555`; some set-top boxes need a different port.

### No authorization dialog / I tapped Deny?

The dialog appears on the **first connection**. If it doesn't show, disconnect and reconnect; when it appears, choose **Always allow** and confirm. Tapping Deny keeps you on the connection page, and the dialog reappears on retry. Once approved, the token is saved on this device and won't prompt again.

### Why is the first connection slow?

The first time, the accelerator plugin must be installed onto the TV over ADB (download, install, launch). After that, reconnects use the fast channel and jump in within a second — no reinstall.

### It worked before but not now?

- TV asleep or rebooted → wake it and reconnect; the app auto-falls back to the ADB flow to recover.
- IP changed → long-press the device on the home screen, edit the new IP, and reconnect.
- Debugging disabled / authorization revoked on the TV → re-enable debugging and re-authorize on the TV.

### Are Huawei / Honor (HarmonyOS) TVs supported?

HarmonyOS uses hdc instead of standard ADB, and some models disable TCP debugging out of the box, so they are **not guaranteed to be supported**. Verify your model can enable network ADB debugging first.

### Is USB connection supported?

This app uses **network (wireless) ADB** over the TV's IP — not a USB cable.

### Does it upload my data / go online?

This app is a **local-only client with no backend**: no telemetry, ads, or third-party analytics. Everything happens directly between your phone and TV.
