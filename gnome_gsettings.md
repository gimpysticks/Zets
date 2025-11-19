---
title: gnome_gsettings
created: 2025-10-21
modified: 2025-10-21
---

`gsettings set org.gnome.mutter overlay-key ''`
gsettings set org.gnome.shell.keybindings toggle-application-picker "['<Alt>F2']"`
gsettings set org.gnome.desktop.wm.keybindings switch-applications "['<Alt>Tab']"`
gsettings set org.gnome.shell.window-switcher current-workspace-only true`
gsettings set org.gnome.desktop.wm.keybindings close "['<Alt>F4']"`
gsettings set org.gnome.desktop.wm.keybindings maximize "['<Super>Up']"`
gsettings set org.gnome.desktop.wm.keybindings minimize "['<Super>Down']"`
gsettings set org.gnome.desktop.wm.keybindings unmaximize "['<Super>Down']"`
gsettings set org.gnome.desktop.wm.preferences mouse-button-modifier "<Alt>"`
gsettings set org.gnome.desktop.wm.preferences resize-with-right-button true`
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-up "['<Control><Alt>Up']"` and `gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-down "['<Control><Alt>Down']"`
gsettings set org.gnome.desktop.wm.keybindings move-to-workspace-right "['<Shift><Control><Alt>Right']"`
gsettings set org.gnome.desktop.wm.keybindings move-to-workspace-left "['<Shift><Control><Alt>Left']"`
gsettings set org.gnome.shell.keybindings switch-to-application-1 "['<Super>1']"`, `gsettings set org.gnome.shell.keybindings switch-to-application-2 "['<Super>2']"`, and so on for workspaces 2-9.
gsettings set org.gnome.desktop.wm.keybindings close "['<Control>q']"`
gsettings set org.gnome.desktop.wm.keybindings close "['<Control>q', '<Control>w']"`
gsettings set org.gnome.desktop.wm.keybindings open-settings "['<Control>,']"`
gsettings set org.gnome.desktop.lockdown disable-lock-screen false` (Enables the default Super+L lock screen keybinding)
gsettings set org.gnome.shell.keybindings toggle-message-tray "['<Super>Shift>q']"`
