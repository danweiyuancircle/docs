# RightFlow User Guide

Last updated: October 14, 2026. Requires macOS 14 or later; the interface and features depend on your installed version. The current development build includes 7zz local archive extraction. The extraction instructions below apply only to versions that provide the feature and do not indicate that an App Store version has been released.

## 1. Enable the Finder extension

1. Open RightFlow and check the Finder extension status at the bottom.
2. If the extension is off, use the app's System Settings entry point and enable RightFlow in macOS extension management. The name and location of this system setting may vary by macOS version.
3. Return to Finder, right-click an empty area in the current folder or a selected file, and open the “轻右键” or “RightFlow” submenu.

The main app manages settings and executes actions requiring file access. The Finder extension provides the menu. Starting the app does not mean the extension is enabled.

## 2. Edit the context menu

The action rows in the main window are the menu configuration; there is no separate Save button.

- **Switches**: Turn off actions you do not need. Changes take effect the next time you open the Finder context menu.
- **Order**: Drag a row's handle to reorder it, or use “Move Up / Move Down” in the row menu.
- **Inline selectors**: Choose a default template, terminal, or editor, or open template and location management.
- **General settings**: Use the gear to access language, appearance, help, extension setup, and purchase-related options.

The menu shows applicable actions according to whether you are clicking a blank area, a file, an image, or have items awaiting paste. The number of settings rows therefore differs from the number of simultaneous Finder menu rows. The actual short menu has at most six rows. “Copy as PNG” appears automatically for a single image according to the selection.

Use Tab to reach controls and Space to toggle switches. Native menus support arrow keys and Return. If an app is no longer installed or folder authorization is invalid, select a valid app or location again.

## 3. Common actions

### Copy paths and names

Click “Copy Path” to place the target path on the system clipboard. Hold Option while clicking the same item to use a file URI instead. “Copy Filename” appears only when an item is selected.

### Create a file

Use the new-file action in an empty area of a Finder folder. Plain text is the default. When plain text is selected as the template, hold Option to create Markdown instead. You can also make Markdown the default through the inline selector.

Pro lets you choose a custom template. Template names are limited to 40 characters, extensions to 16 characters, and initial contents to 8000 characters. If the default template is deleted, choose a valid template again; a previously displayed name is not proof that the template still exists.

### Terminal and editor

Configure a valid installed terminal and use its action in an empty area of a folder. Selected files or folders can be opened through the Pro editor action. The system terminal can be the default selection. An external app is responsible for its own behavior after it is opened.

### Move to a recent location

Select a file or folder, open “Move to Recent Location,” and choose a saved location or “Choose Folder…”. Use the system picker to authorize a folder when selecting it for the first time. A location is recorded as recent after a successful move.

The free tier uses one saved location. Pro can save additional locations, with the three most recent shown in the menu. If authorization becomes invalid, select the relevant folder again. Full-disk access is neither required nor promised.

### Cut / Paste

Pro users can enable this group. Select files and use “Cut” to record the items awaiting a move. Switch to the destination folder and use “Paste” in an empty area to move them. The buffer is cleared after a successful paste. Cutting is not deletion, and turning off the switch does not undo a completed move.

### Copy as PNG

Select one supported image and use “Copy as PNG” to encode it onto the system clipboard. This does not overwrite the original or create a converted file. Oversized, damaged, or unreadable images can cause the action to fail.

## 4. Pro local archive extraction

The current development build includes extraction. You can use the action only if your installed version actually provides it.

1. Enable the Pro “Extract” action in the file-tools settings.
2. Select one supported archive in Finder.
3. Click “Extract to Folder.” The app processes it locally using 7zz and does not upload the archive contents.
4. Check the resulting folder or error message. Back up important material first and do not repeatedly click an operation that has not finished.

Common formats supported by the current development build include ZIP, 7z, RAR, TAR, GZip, BZip2, XZ, and their TAR compound extensions. This guide does not promise availability for split archives, encrypted archives, or other special formats. Refer to the version's interface and error messages for specific limitations.

This flow reuses the local 7zz processing approach from the maintainer's own [EasyArchiver project, formerly EasyZip](https://github.com/danweiyuancircle/easy-zip), rather than a similarly named competing product. The engine is 7-Zip 25.01. For licenses and source, see the [third-party open-source component appendix in the Privacy Policy](https://github.com/danweiyuancircle/docs/blob/main/rightflow/privacy.en.md#appendix-third-party-open-source-components).

Current protection limits: a source archive of at most 2 GiB, a cumulative uncompressed size of at most 10 GiB in the listing, and at most 100000 entries. Development validation has included tests with real archives, a targeted AES ZIP test, and an actual Finder ZIP operation on an arm64 Mac. This evidence does not mean that all formats, error cases, or other hardware have completed acceptance testing, or that an App Store version has been released.

## 5. Purchases and restoring purchases

Purchase status is read through Apple StoreKit. Review the actual checkout price and entitlements before purchasing, and use the app's restore option for purchases made with the same Apple account. Purchases and restoration require Apple services; file operations themselves run locally.

Publishing documentation in this repository does not mean that the app is listed on the App Store or that a version has been released. If you have purchased but still see a locked status, check the installed version and Apple account, then contact support.

## 6. Frequently asked questions

| Problem | What to do |
| --- | --- |
| No menu in Finder | Check the system extension switch, reopen RightFlow and the Finder window, then check the extension status again |
| The selected terminal or editor is unavailable | Check whether the app is still installed and choose a valid one again; a single failed scan does not mean the original configuration was deleted |
| A location is not authorized | Select the folder again using the system picker; check the drive connection and macOS permission restrictions |
| Repeated prompts to access other apps' data | Stop repeating the operation, check the version, signing, and extension status, and contact support; do not grant full-disk access merely for troubleshooting |
| A file operation fails | Check the source, destination, free space, and permissions; confirm the current state of the files before deciding whether to retry |
| Diagnostic logs are needed | Local logs may contain personal paths; redact them first, then voluntarily provide only the relevant excerpts |

Support: [GitHub issues](https://github.com/danweiyuancircle/docs/issues). Provide the version, steps to reproduce, and redacted screenshots. Do not publish personal files, keys, or payment information.

Related documents: [Privacy Policy](https://github.com/danweiyuancircle/docs/blob/main/rightflow/privacy.en.md) and [User Agreement](https://github.com/danweiyuancircle/docs/blob/main/rightflow/terms.en.md).
