That's a great next step\! Having the post-installation script ready will make your reinstall process much faster and more automated.

Below are the three separate scripts needed to perform the reinstallation process for Debian (APT), Flatpak, and Snap packages, assuming your backed-up lists are accessible on the new system (e.g., in a flash drive mounted at `/mnt/backup/`).

## ⚙️ Post-Installation Scripts

### Pre-Requisite: Place the Backup

Before running any of these scripts, you must copy the backup folder you created (e.g., `reinstall_prep_20251209_152136`) back onto your new system. A good place might be your new home directory:

```bash
# Example: Assuming the folder is on a USB drive mounted at /mnt/usb
cp -r /mnt/usb/reinstall_prep_20251209_152136 ~/reinstall_backup
```

-----

### 1\. Script for APT Packages: `reinstall_apt.sh`

This script handles the core Debian packages. It also includes an important step to reinstall any packages that may have been *marked* as manually installed but were automatically installed by dependencies (`apt-mark auto`).

```bash
#!/bin/bash

# --- Configuration ---
# Set the path to your backed-up lists
BACKUP_PATH="$HOME/reinstall_backup" 
APT_LIST=$(find "$BACKUP_PATH" -name "apt_packages_list.txt")

echo "--- Reinstalling APT Packages from List: $APT_LIST ---"

# Check if the list file exists
if [ ! -f "$APT_LIST" ]; then
    echo "🚨 Error: APT package list not found at $APT_LIST."
    echo "Please verify the BACKUP_PATH variable."
    exit 1
fi

echo "Updating package list..."
sudo apt update

echo "Installing packages listed in the backup file..."
# Use xargs to safely pass the list of packages to the install command
# The -y flag assumes 'yes' to all prompts
xargs sudo apt install -y < "$APT_LIST"

echo "Attempting to reset 'manually installed' marks..."
# Re-mark packages as manually installed (this is useful if the initial list included dependencies)
for package in $(cat "$APT_LIST"); do
    sudo apt-mark manual "$package"
done

echo "✅ APT package reinstallation complete."
```

### 2\. Script for Flatpak Apps: `reinstall_flatpak.sh`

This script iterates through the Flatpak list and installs them from Flathub (the default and most common repository).

```bash
#!/bin/bash

# --- Configuration ---
BACKUP_PATH="$HOME/reinstall_backup" 
FLATPAK_LIST=$(find "$BACKUP_PATH" -name "flatpak_apps_list.txt")

echo "--- Reinstalling Flatpak Applications from List: $FLATPAK_LIST ---"

# Check if flatpak is installed
if ! command -v flatpak &> /dev/null; then
    echo "🚨 Error: Flatpak command not found. Please install Flatpak and setup Flathub first."
    exit 1
fi

# Check if the list file exists
if [ ! -f "$FLATPAK_LIST" ]; then
    echo "🚨 Error: Flatpak list not found at $FLATPAK_LIST."
    echo "Please verify the BACKUP_PATH variable."
    exit 1
fi

# Loop through the list and install each app
while IFS= read -r app_id; do
    if [ ! -z "$app_id" ]; then # Skip empty lines
        echo "Installing Flatpak: $app_id"
        # Use -y to assume 'yes' to installation prompts
        flatpak install flathub "$app_id" -y
    fi
done < "$FLATPAK_LIST"

echo "✅ Flatpak reinstallation complete."
```

### 3\. Script for Snap Apps: `reinstall_snap.sh`

This script handles the Snap applications, using `sudo snap install` for each item on the list.

```bash
#!/bin/bash

# --- Configuration ---
BACKUP_PATH="$HOME/reinstall_backup" 
SNAP_LIST=$(find "$BACKUP_PATH" -name "snap_apps_list.txt")

echo "--- Reinstalling Snap Applications from List: $SNAP_LIST ---"

# Check if snap is installed
if ! command -v snap &> /dev/null; then
    echo "🚨 Error: Snap command not found. Please install Snapd first."
    exit 1
fi

# Check if the list file exists
if [ ! -f "$SNAP_LIST" ]; then
    echo "🚨 Error: Snap list not found at $SNAP_LIST."
    echo "Please verify the BACKUP_PATH variable."
    exit 1
fi

# Loop through the list and install each app
while IFS= read -r app_name; do
    if [ ! -z "$app_name" ]; then # Skip empty lines
        echo "Installing Snap: $app_name"
        # The --classic or --devmode flags might be needed for some Snaps, but this is the standard
        sudo snap install "$app_name"
    fi
done < "$SNAP_LIST"

echo "✅ Snap reinstallation complete."
```

-----

## 💻 Final Steps (Post-Install)

1.  **Save the Scripts:** Save the three scripts above to a convenient location (e.g., your new `~/bin` folder).

2.  **Make Executable:**

    ```bash
    chmod +x ~/bin/reinstall_apt.sh
    chmod +x ~/bin/reinstall_flatpak.sh
    chmod +x ~/bin/reinstall_snap.sh
    ```

3.  **Run in Order:**

    ```bash
    ~/bin/reinstall_apt.sh
    ~/bin/reinstall_flatpak.sh
    ~/bin/reinstall_snap.sh
    ```

### AppImages and Data

  * **AppImages:** You must **manually copy** the files listed in `appimage_files_list.txt` from your backup source to the new system.
  * **User Data:** These scripts only reinstall the applications. You must separately copy all your important user data, configuration files (often in hidden folders like `~/.config` or `~/.local`), and documents from your old home directory backup.

Do you have any specific applications that use configuration files you want to make sure you back up, or are you ready for me to summarize the entire process?