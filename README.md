# IPS Surveyor App

Android app for the **International Passenger Survey 2026-27**, conducted by the Indian Statistical Institute for the Ministry of Tourism, Government of India.

This repository hosts the installable app files. There is no source code here.

---

## Download

### ➡️ **[Download the latest version](https://github.com/IDEAS-ISI/ips-app-release/releases/latest)** ⬅️

Open that link, scroll down to **Assets**, and tap one of the `.apk` files.

### Which file do I tap?

| File name contains | Choose this if |
|---|---|
| **`arm64-v8a`** | **Almost everyone.** Any phone bought roughly 2017 or later. Try this one first. |
| `armeabi-v7a` | Only if `arm64-v8a` refuses to install — older or low-end phones. |

Picking the wrong one does no harm. It simply won't install, and you can go back and tap the other.

---

## Installing

1. Tap the `.apk` file from the link above. Chrome will download it.
2. Open the download (from the notification, or **Downloads** in your file manager).
3. Android will warn that the file came from outside the Play Store. Tap **Settings**, turn on **Allow from this source**, then go back.
4. Tap **Install**.

You only need step 3 the first time.

---

## Updating

**You do not normally need this page after the first install.** The app checks for updates on its own, once a day, and shows a prompt when a new version is available. Tap **Download** and follow the installer.

Installing an update **keeps all your data**. Surveys already on the phone, including ones not yet synced, are preserved.

---

## ⚠️ Never uninstall the app to fix a problem

Uninstalling **permanently deletes every survey stored on the phone**, including completed ones that have not yet been synced to the server. This cannot be undone and the responses cannot be recovered.

If something is wrong:

1. Connect to Wi-Fi or mobile data and let the app **sync** first.
2. Confirm the sync finished and no responses are still pending.
3. Only then contact your supervisor.

---

## Troubleshooting

**"App not installed" or "package appears to be invalid"**
Usually the wrong file for your phone. Go back and try the other `.apk`.

If it still fails and you already have the app installed, **stop and contact your supervisor.** Do not uninstall to force it through — you will lose unsynced surveys. This error can also mean the update was signed differently from the copy on your phone, which is a problem your supervisor needs to report, not something to work around.

**The download won't open**
Check you have enough free storage, then re-download.

**No update prompt appears**
The check runs once a day and needs a working connection. You can always install the latest version manually from the link above.

---

## For supervisors

- Releases are published automatically by the build pipeline. Each release is tagged `v<version>-build.<number>-<date>-<commit>`.
- The app compares its build number against the `build.<n>` in the newest release tag, so **every published release offers itself as an update to every installed device.** Use the separate test-build workflow for anything not meant for the field.
- All APKs are signed with the same key. A signature-mismatch error in the field means an APK was built or published outside the normal pipeline — investigate before telling anyone to reinstall.
