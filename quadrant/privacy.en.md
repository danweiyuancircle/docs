# Quadorder Privacy Policy

Updated: October 18, 2026.

This policy covers the Quadorder iOS, iPadOS, and macOS apps provided by danweiyuancircle. Quadorder organizes tasks in four quadrants. It requires no app account and includes no in-app advertising, third-party behavioral analytics, or developer-operated cloud sync service.

## 1. Data processed on your device

| Data | Purpose and location |
| --- | --- |
| Task titles, notes, quadrants, order, dates, reminder times, and repeat rules | Store task state in Application Support within the local app container |
| Completed task snapshots, completion times, and repeat-task links | Display the last 30 days of completion history and determine whether a task can be restored |
| Language, appearance, reminder identifiers, and review-prompt counters | Store preferences locally to retain settings, maintain the app's reminders, and control review prompts |
| Purchase results and unlock entitlement | Verify the one-time unlock on the device through Apple StoreKit |
| A JSON file you select for import | Read and validate it locally to replace current tasks and completion history |

Quadorder does not automatically upload your tasks, notes, or backups to the developer, sell this data, or use task content for advertising profiles. There is no developer-operated account system; deleting local tasks does not require an account-deletion request.

## 2. Reminders and system permissions

**iOS / iPadOS:** When you enable task reminders, the app may request access to Reminders and notifications. With Reminders access, it creates or updates task titles, notes, and due times in its own list and retains identifiers for those entries. It does not import or display your other reminder lists. When notifications are allowed, it uses local notifications and avoids adding a duplicate alarm to the corresponding system reminder. Local notifications also work when only notification access is allowed.

The system grants full Reminders access; the app's actual use is limited to entries it tracks. Its list uses the system's default Reminders account or an available local account. If the default account uses iCloud or another online service, that account may sync reminder entries to other devices. This does not provide cloud sync for the Quadorder task board. See [Apple's Reminders account guide](https://support.apple.com/en-ie/guide/iphone/iph8739025dd/ios).

**macOS:** The app requests notification access and schedules local notifications. It does not request Reminders access or create system reminders. If an earlier version already had Reminders permission and stored entry identifiers, the app attempts to remove entries it previously created and retries failed cleanup during later synchronization.

Notifications may display task titles and notes. Lock-screen and Notification Center visibility depends on your system preview settings. You can revoke access or disable previews in system settings. Denying reminder permissions does not prevent basic task management. Local notifications whose scheduled time has passed are not replayed.

## 3. Export, backup, and restore

JSON exports contain task titles, notes, dates, reminder times, repeat rules, order, completion history, and task-link identifiers. Backups are not anonymous and receive no additional encryption from the app. Files are saved to your chosen location, without automatic delivery to the developer. If you choose cloud storage, a network location, or another app, that service's rules govern subsequent storage, sync, and transfer.

Restoring a backup replaces local tasks and completion history rather than merging them. It does not restore purchase entitlements, language, appearance, or system permissions. The replacement cannot be undone in the app; history outside the retention window is removed during restoration. Export current data before restoring. Old backup files may retain records already removed from the app; you control how long those files are kept.

## 4. Apple, documentation, and voluntary feedback

Apple App Store / StoreKit handles purchases, payments, and purchase restoration. The app receives product and entitlement information needed to verify access, but not payment-card numbers or your Apple Account password. See [App Store & Privacy](https://www.apple.com/legal/privacy/data/en/app-store/).

GitHub hosts this website and documentation repository. Website visits and public Issues are subject to [GitHub's Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). Public Issue content and attachments are visible to others.

You may voluntarily email [tianxiake1994@gmail.com](mailto:tianxiake1994@gmail.com). We receive your email address, message, and any version details, screenshots, or files you attach, solely to handle your request, investigate the issue, and reply. Email providers transmit and store messages. Remove unnecessary personal information before sending. Full task backups, Apple passwords, card details, and complete payment receipts are not required.

## 5. Retention, deletion, and controls

Active tasks remain until you delete or replace them. On launch or return to the foreground, the app removes completion history outside the last 30 days. This is not a promise of scheduled background deletion and does not remove exported backups, emails, or copies in other systems.

You can delete tasks, manage local backups, and control notification and Reminders permissions in system settings. Platform behavior determines whether app containers, preferences, and system backups remain after uninstalling. Removing the macOS application does not necessarily remove app data. System reminders and exported files may also remain. Contact support for help removing residual local data.

Support email is retained for the time needed to handle the request. After it is resolved, you may use the address above to request deletion of feedback information we hold, except records that applicable law requires us to retain. We cannot delete copies held by Apple, GitHub, email providers, cloud services, or other recipients on your behalf; use their controls and privacy-request channels.

## 6. Updates and contact

We will update this policy and its date when our data practices materially change. New system permissions follow the system authorization process. This policy does not reduce rights granted by applicable law.

Privacy and support contact: [tianxiake1994@gmail.com](mailto:tianxiake1994@gmail.com). See also the [User Agreement](terms.en.html) and [Support](support.en.html).
