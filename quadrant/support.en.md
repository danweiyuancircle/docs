# Quadorder Support

Updated: October 18, 2026.

Support email: [tianxiake1994@gmail.com](mailto:tianxiake1994@gmail.com).

Include your app version, iOS / iPadOS / macOS version, steps, expected result, and actual result. Redacted screenshots can help. Task content is not required. Do not send Apple passwords, card details, complete payment receipts, or unchecked task backups. No new account is required to receive support.

## Basics

- Place tasks in four quadrants by importance and urgency. Today shows tasks due today or overdue.
- Free capacity is 4 active tasks per quadrant; the one-time unlock increases it to 8. Apple's confirmation screen shows the purchase price.
- Settings offers Chinese / English, appearance, and Restore Purchases.
- A repeating task generates its next occurrence when completed. An earlier restoration is refused if it would overwrite later completions or edits.
- Done retains the last 30 days of completion history. Older entries are removed on launch or return to the foreground. Use JSON backups for longer retention.

## A reminder did not appear

Check that the task has both a date and a reminder time, and that the time is still in the future. Local notifications whose scheduled time has passed are not replayed.

**iPhone / iPad:** Check Quadorder's notification access, sound, and preview settings in system settings. If you use system Reminders, also check Reminders access. Local notifications can work with notification access alone. System reminders may sync through the default account, but this does not sync another device's Quadorder task board.

**Mac:** Allow Quadorder notifications in System Settings and enable the banners and sounds you need. The Mac app sends local notifications directly and does not require Reminders access.

On either platform, also check Focus modes, sound settings, and device conditions. Return to the app after changing permissions so it can recheck access and synchronize reminders. If the issue persists, send the scheduled date and time, system version, and error message; the task text is not needed.

## Backup and restore

Choose Export backup in Settings → Local data and save it somewhere you control. The file includes task titles, notes, and completion history and has no additional encryption from the app. Your chosen services handle cloud storage and sharing.

Export current data before restoring. Choose Restore from backup, select a Quadorder JSON export, and confirm. This replaces current tasks and completion history without merging and cannot be undone in the app. It does not restore language, appearance, system permissions, or the purchase entitlement. Invalid, damaged, or unsupported backups are rejected. Do not edit a backup to bypass validation.

## Purchase or restoration problems

Use the Apple Account that made the purchase, check your connection, then select Restore Purchases in Settings. Backup files cannot restore the unlock. If the product price has not loaded, use Retry on the purchase screen. Do not pay again to troubleshoot an entitlement problem.

Use [Apple's refund service](https://reportaproblem.apple.com/) for refunds or billing. If the app recognizes the purchase but capacity is incorrect, email the app version and a description of the problem.

## Data-read errors or cleanup

If data cannot be read, avoid repeatedly deleting the app or overwriting backups. Preserve existing files, record the error, and contact support. Removing the Mac application may leave local app data behind; system reminders and exported backups may also remain. Ask support for cleanup steps for your platform.

[Privacy Policy](privacy.en.html) · [User Agreement](terms.en.html) · [中文](support.zh.html)
