---
created: 2026-01-20
---
# NFS Mount Point Backup Setup

**Date:** 2026-01-20  
**Task:** Create one-time backup script for NFS mounts, scheduled for 6AM

## Active NFS Mount Points
The following mount points from server 192.168.4.2 are backed up:
- /mnt/videos
- /mnt/pictures
- /mnt/movies
- /mnt/diskimages
- /mnt/music
- /mnt/backup
- /mnt/Documents

## Backup Configuration
- **Source:** Active NFS mounts in /mnt/
- **Destination:** /media/sticks/HD710_PRO
- **Script Location:** ~/bin/backup_server
- **Schedule:** Daily at 6:00 AM
- **Method:** rsync with --delete flag

## Script Features
- Automatically detects active NFS mount points from 192.168.4.2
- Creates timestamped log files in backup destination
- Excludes .Trash-* and lost+found directories
- Uses rsync for efficient incremental backups
- Logs all operations with timestamps

## Systemd Service & Timer
- **Service:** /etc/systemd/system/backup-server.service
- **Timer:** /etc/systemd/system/backup-server.timer
- **First Execution:** Wed 2026-01-21 06:00:00 EST

## Management Commands

### Check timer status
```bash
systemctl status backup-server.timer
systemctl list-timers backup-server.timer
```

### View backup logs
```bash
journalctl -u backup-server.service
# Or check log files in /media/sticks/HD710_PRO/backup_*.log
```

### Manual execution
```bash
~/bin/backup_server
```

### Stop/disable timer
```bash
sudo systemctl stop backup-server.timer
sudo systemctl disable backup-server.timer
```

### Remove timer (one-time backup)
After the backup completes, you can remove the timer if it was meant to run only once:
```bash
sudo systemctl stop backup-server.timer
sudo systemctl disable backup-server.timer
sudo rm /etc/systemd/system/backup-server.{service,timer}
sudo systemctl daemon-reload
```

## Notes
- Timer is set to run daily at 6AM (remove after first run if one-time only)
- Backup uses --delete flag, so files deleted from source will be deleted from backup
- Each mount point gets its own subdirectory in the backup destination
- Logs are created with format: backup_YYYYMMDD_HHMMSS.log
