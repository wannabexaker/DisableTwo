# Disable Two

### Escape the OneDrive chase.

OneDrive found your Desktop. Then your Documents. Then your Pictures.
At this point, it probably knows where you spend Christmas.

**It's time to see other clouds. Or absolutely no clouds.**

Disable Two removes **OneDrive** and **Phone Link** with one button.
Yes, this needed an entire app.

## Your new life starts here

Delete two apps. Fix your entire life.

- Find your soulmate.
- Get married.
- Become ridiculously rich and internationally famous.
- Buy a yacht with absolutely no cloud storage.
- Finally make your parents proud.

*Love, yachts and fame are not included. App removal is real.*

## One file. One button. Zero settings.

Download **`DisableTwo.exe`** and open it. That's the whole installation process.

The app is portable: its removal scripts, artwork and icon are embedded inside
the executable. You can copy just that file to another Windows PC or a USB stick.
The source folder, README and preview image are not required to run it.

It uses Windows PowerShell 5.1 and .NET Framework 4.5+ on Windows 10/11.
It does not require Python, Node.js, or a separate PowerShell script download.
Administrator access is required when you press the button.

Portable means no app installer. Removal still changes Windows settings, and
the app saves reports and backups on the PC where you use it.

## Press this to begin your yacht era

1. Make sure the OneDrive files you want to keep are downloaded locally.
2. If OneDrive backs up Desktop, Documents or Pictures, stop that folder backup
   in OneDrive settings first and keep your files locally. The app checks for
   remaining redirection and stops if it finds it.
3. Close applications whose old OneDrive paths need repair. If one is still
   running, the report tells you which detected application needs closing.
4. Open `DisableTwo.exe` and press **Uninstall both. Start my new life.**
5. Accept the Windows administrator prompt for the **same Windows account**.
6. Read the result and restart Windows after removal.

Opening the window alone does not uninstall anything.

## What actually happens

Behind the wildly unreasonable marketing department, the app:

- Checks folder locations and detected cloud-only files before uninstalling.
- Runs OneDrive's registered uninstaller after verifying its Microsoft signature.
- Removes Phone Link for existing users and checks its provisioning for new users.
- Uses a second Windows mechanism when the initial provisioning inspection fails.
- Applies the OneDrive sync restriction and the legacy phone-PC linking policy.
- Repairs recognized old paths in VoiceMeeter, SignalRGB, Premiere and Insta360
  settings when the corresponding local destinations already exist.
- Backs up changed settings and verifies configuration-file backup copies.
- Cleans identified dead OneDrive references and archives recognized installer leftovers.
- Reports success, a safe stop, incomplete removal, or items needing review separately.

**Your personal files stay.** A nonempty old OneDrive folder is kept and reported
for review. Empty old roots can be removed.

## Things the yacht brochure forgot to mention

This is not an automatic migration tool for every application on your PC.
It does not download cloud-only files, automatically fix existing Windows folder
redirection, delete your cloud data, or remove shared Windows/Office components.
Phone Link removal can remove its app-local settings and data.

OneDrive removal covers machine-wide and current-user registrations. Separate
OneDrive installations in other Windows profiles may need separate runs.
Different administrator credentials are rejected to avoid targeting the wrong profile.

Policy enforcement depends on Windows edition. Home and unrecognized editions
produce a review result. Managed devices, protected packages and other signed-in
users can block removal. Windows updates, resets or manual reinstalls can bring
components back. No promise of "every PC, forever" is hiding behind the joke.

The executable is unsigned, so Windows may show an unknown-publisher or
SmartScreen prompt.

## Reports, backups and second thoughts

Reports are saved under:

```text
%LOCALAPPDATA%\DisableTwo\report-*.txt
```

Configuration backups and their original-location manifests are under:

```text
%LOCALAPPDATA%\DisableTwo\Runs\<run-id>
```

Original policy values are recorded in `policy-backup-*.json` in the main
`DisableTwo` data folder. Reports open automatically when attention is required.

There is no one-click undo. Settings backups can be restored manually, and the
apps can be reinstalled separately. Removed Phone Link app data is not backed up.

## Publishing and source

**The app download can be a single file: `DisableTwo.exe`.**
For a minimal GitHub repository, upload that executable and this `README.md`.
No image files are required by this README. The executable can also be attached
to a GitHub Release as a standalone download.

The complete ZIP includes source code and the icon assets. If you publish the
source too, `Source/Build.ps1` rebuilds the executable using the installed
.NET Framework C# compiler. `Source/Build-Icon.ps1` rebuilds the multi-size icon.
The cartoon artwork was generated with OpenAI's image-generation tool.

## Validation

Version **2.1** uses the removal engine from version 2.0, which passed **27
isolated checks**, including backups, path handling, repeat runs and failure
reporting. Removal workflows were simulated; this is not testing across every
Windows edition. The embedded engine was checked in read-only mode, and the
native window and embedded icon were visually verified.

---

**Two apps. One button. A completely unjustified amount of optimism.**
