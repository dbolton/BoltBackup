## Planned for later releases
- Fix exclusions that include spaces in the path name. Also check quotation marks
- Label backups as partial until complete. Resume the partial backups before starting a new one
- Investigate letter mapping to network drives for backup folders
- Add error checking to excluded folders
- Finish documentation for running

## Known issues
- ShadowSpawn fails when robocopy uses a /log argument that includes quotes https://github.com/candera/shadowspawn/issues/20
- If ShadowSpawn fails, it holds on to the old drive letter  https://github.com/candera/shadowspawn/issues/22
- ShadowSpawn fails if you happen to be installing software when the backup tries to start.

## Completed
### Next version

### 0.5.1
 - You can now start Solid Backup from a path that includes spaces.
 - Always recycle the oldest backup. (Previously this did not work for multiple mirror backups to a drive encrypted by VeraCrypt.)
 - Updated dependencies.
 - Continued work toward "Standard JavaScript" code style.

### 0.5.0
 - You can now exclude files and folders that have spaces in the name.
 - Moved log file from last parameter to first parameter (on Robocopy) so that the log still displays if there are errors in later parameters (such as file and folder exclusions).
 - Began initial work to move to "Standard JavaScript" code style.

### 0.4.5
- Prevent saves and backups if there are errors on the page.
- To speed up backups, reduced retries from 2 to 1 and reduced wait time between retries from 10 seconds to 3 seconds.
- Move "Mirror" option above "Full" backup type, since the "Mirror" option is more useful.

### 0.4.4
- Change shortcut name from "SolidBackup" to "Solid Backup".
- Fix spacing on wordmark.
- Reduce retries from 5 to 2 for errors when backing up a particular file.

### 0.4.3
- Remove space from product name since it wasn't working reliably

### 0.4.2
- Improve message when auto-update finishes downloading.
- Add space to package name "Solid Backup"

### 0.4.1
- Fix logs on Windows 7 so it displays with the correct encoding.

### 0.4.0
- Change name to Solid Backup
- Update File > Presets (CofC now uses mirror option)
- Show summaries for Schedule and Advanced on first run (before settings file has been saved)
- Switch back to unsigned installer to avoid problems with auto-updates.

### 0.3.0
- Support for automatic updates
- Installer is self-signed

### 0.2.0
- Support for mirror backup type
- Exclude specific folders from backup
- Option to start in dev mode that shows the Developer Tools and resizes the window to accomodate (simplifies development)
- Backup settings for dev mode are saved to a different file from the stable version
- Enable save button after changing the source or destination folders via the "Browse" buttons
- Do not use drive letter that is still in use as a RAM disk. (If application is closed during a backup the shadow volumn RAM disk stays around until Windows restarts).
- Update display of backup log without blinking and significantly reducing CPU usage on large logs
- Support Unicode filenames in log
- Remove "ROBOCOPY" from log heading to avoid confusion

### 0.1.2
- Add Shift to shortcuts of presets to avoid accidental changes

### 0.1.1
- Show one-line summary of scheduling that displays even when the schedule settings are collapsed
- Improve radio dials interaction
	- Whole area between radio dial and label is clickable
	- Uses pulldown menu for dates instead of radio dials
	- When you click on a day of the week, the week radio dial gets selected automatically

### 0.1.0
- Save full backups
- Do sanity checks on folder locations (to avoid infinite loops)
- Do shadow copies
- Allow scheduling of backups
