# RightFlow Privacy Policy

Last updated: October 21, 2026.

This policy explains how RightFlow handles data. RightFlow is a local macOS Finder context-menu tool provided by the maintainer of this repository. It does not require registration for a developer-operated account, provide a developer-operated file server, or use in-app advertising, third-party behavioral analytics, or automatic telemetry services. The app has file read and write permissions; “local processing” does not mean that it never reads files or requires authorization.

## 1. Data processed on your Mac

| Data | Purpose and location |
| --- | --- |
| Settings such as menu order, switches, selected terminal and editor, template contents, and language | Stored in local App Group shared settings for use by the main app and Finder extension |
| Names and paths of selected files or folders | Used to copy paths, open apps, create files, move items, and perform similar actions |
| Folder authorization bookmarks | macOS security-scoped bookmarks preserve folder access within the granted scope; bookmarks are authorization records, not copies of file contents |
| Cut buffer and operation handoff information | Paths and authorization information for items awaiting a move are recorded locally; the main app and extension hand off operations through a local shared container |
| Clipboard contents | Paths, names, or PNG images are written according to the action you select; other apps with appropriate access may read the system clipboard |
| File and image contents | Corresponding files are read or written as needed for actions such as creating files, moving items, or copying PNG images; the app does not automatically scan the entire disk |
| Local diagnostic logs | Used to investigate failed operations; may include actions, times, file names or paths, and error information; not automatically uploaded to the developer |
| Free-trial records | The first-use date and most recently observed time are stored in the local Keychain to determine the two-month trial; trial and entitlement status are shared locally with the Finder extension through the App Group, without upload to a developer server |
| Purchase entitlement status | The app verifies lifetime-purchase or subscription transactions through Apple StoreKit, reads entitlement details such as expiry or revocation, and stores entitlement status locally for the main app and Finder extension |

The current development build includes Pro local archive extraction. It uses the local 7zz engine to read the archive you select and write the results to the destination folder, without uploading the archive to a developer server. Development-build validation is not an App Store release; supported formats and interactions depend on the installed version.

Building a menu does not authorize access to arbitrary folders. File operations remain subject to the macOS sandbox, user authorization, file permissions, and system privacy protections. If authorization expires or becomes invalid, you need to select the relevant folder again.

## 2. Whether data leaves your device

RightFlow does not automatically upload files, templates, paths, bookmarks, or diagnostic logs to the developer, sell this data, or use local data to build advertising profiles.

The following actions involve other services or apps:

- **Purchases and restoring purchases**: Handled by Apple's App Store and StoreKit. RightFlow receives purchase results and entitlement information; it does not collect or store credit card numbers. For Apple's handling of purchase and account data, see [App Store & Privacy](https://www.apple.com/legal/privacy/data/en/app-store/).
- **Opening a terminal or editor**: RightFlow passes the relevant file or folder to the app you choose. That app's subsequent behavior is governed by its own privacy policy.
- **Reading these documents or submitting feedback**: GitHub hosts the pages and public issues. GitHub may process access logs, IP addresses, account information, and content you submit under the [GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

A declared network permission does not itself mean that data is being uploaded. This policy describes actual usage and does not promise that Apple, GitHub, the operating system, or external apps never connect to the internet.

## 3. Support information you choose to provide

When you contact [unitcircle@agent.qq.com](mailto:unitcircle@agent.qq.com), the maintainer reads your sender address and the problem description, attachments, or diagnostic excerpts you voluntarily provide to handle your support request. Relevant email providers transmit and retain messages under their privacy policies. The app does not automatically send support emails or attachments.

When you submit feedback through a [GitHub issue](https://github.com/danweiyuancircle/docs/issues), the maintainer reads the version information, problem description, screenshots, or logs you voluntarily provide to investigate and respond. Public issues and attachments are publicly visible and may be indexed by search engines.

Do not post personal file contents, account information, keys, payment receipts, or complete personal paths. Review diagnostic logs and redact sensitive information before sending them. RightFlow does not automatically upload other data if you choose not to upload logs.

## 4. Retention, deletion, and control

Local settings and authorization records are retained as needed for subsequent use. The first-use date and most recently observed time are retained in the local Keychain for trial eligibility and may remain after uninstalling the app. These records do not uniquely identify a person across Macs and are not a server-maintained reinstall-prevention record. The cut buffer is cleared after a successful paste. Local diagnostic logs are managed through log rotation; no fixed retention period is promised.

You can disable corresponding menu actions, remove saved locations, stop using the app, and manage system-granted permissions in macOS System Settings. Quitting or uninstalling the app does not necessarily clear App Group settings and logs, and does not automatically delete files you have created, moved, or extracted. If you need help clearing local app data, ask through the support channel without publishing specific personal paths.

GitHub retains data in public feedback. You can use GitHub's editing, deletion, and privacy-request options to manage that content. If you need the maintainer's help with support information in this repository, request assistance through the support channel without reposting sensitive information.

## 5. Policy updates and contact

We will update this policy and its update date when features or data handling change materially. Actions requiring additional authorization follow the system authorization process. This policy does not reduce your privacy rights under applicable law.

Contact the author: [unitcircle@agent.qq.com](mailto:unitcircle@agent.qq.com). You can also use [RightFlow documentation repository issues](https://github.com/danweiyuancircle/docs/issues). Do not include a personal phone number or address in public feedback.

## Appendix: Third-party open-source components

Archive extraction uses **7-Zip 25.01** as a separate `7zz` subprocess. The engine is unmodified and runs locally, without an archive upload service. This appendix describes component licensing. It does not change the data handling described above or indicate that development-build features have been released on the App Store.

| Item | Notice |
| --- | --- |
| Component and version | 7-Zip / 7zz 25.01 |
| Integration | Unmodified standalone command-line process; its code is not linked into the app |
| Licenses | Most code is LGPL-2.1-or-later; some code is BSD-2-Clause or BSD-3-Clause, and includes unRAR usage restrictions. Refer to the official license and source for individual files |
| Copyright holders | 7-Zip: Igor Pavlov, 1999–2025; LZFSE-related code: Apple Inc., 2015–2016; ZSTD-related code: Facebook, Inc. and Igor Pavlov, with Pavlov's years being 2023–2025; XXH64-related code: Yann Collet, 2012–2021, and Igor Pavlov, 2023–2025; copyright in the original unRAR code belongs to Alexander Roshal |
| Official license information and BSD / unRAR terms | https://www.7-zip.org/license.txt |
| Full LGPL 2.1 license | https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html |
| Corresponding source for this version | https://www.7-zip.org/a/7z2501-src.tar.xz |

The unRAR code may not be used to recreate the proprietary RAR compression algorithm. RightFlow integrates extraction only and does not implement RAR compression. The components' original licenses and notices continue to apply. RightFlow's user agreement does not restrict your rights to use the corresponding components and source under those licenses. App distribution materials must also retain the component license and copyright notices; links on this page do not replace obligations that apply when distributing the app.
