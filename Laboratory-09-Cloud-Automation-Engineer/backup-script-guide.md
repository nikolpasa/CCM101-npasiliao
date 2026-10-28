# Automated Backup Script Guide

## Mission Overview
This guide documents the automated backup process created for CloudNova Technologies. The Bash script compresses application data into a timestamped backup file, while Linux Cron schedules the process to run automatically.

## 1. Bash Backup Script

File: `backup.sh`

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="/root/app-data"
BACKUP_DIR="/root/backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a tarball (.tar.gz)
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

## 2. Explanation of the Script

- `#!/bin/bash` tells Linux to execute the script using Bash.
- `SOURCE_DIR` identifies the directory containing the application data.
- `BACKUP_DIR` identifies the directory where backups are stored.
- `TIMESTAMP` generates a date and time value for unique backup filenames.
- `mkdir -p` creates the backup directory if it does not already exist.
- `tar -czf` compresses the application data into a `.tar.gz` archive.
- `echo` displays messages about the backup process.

## 3. Executable Permissions

Command:

```bash
chmod +x backup.sh
```

The `chmod +x` command grants executable permission to the Bash script. Without executable permission, Linux may display a "Permission denied" error when attempting to run the file directly using `./backup.sh`.

After changing the permissions, the script can be executed using:

```bash
./backup.sh
```

## 4. Cron Job Configuration

The following Cron expression schedules the backup script to run every night at 2:00 AM according to the server's timezone:

```cron
0 2 * * * /root/backup.sh
```

### Cron Expression Breakdown

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | Run at minute 0 |
| Hour | 2 | Run at 2 AM |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

The five fields define when the script will execute, while `/root/backup.sh` specifies the command to run.

## 5. Verification

The following commands were used to test the script and inspect the Cron configuration:

```bash
./backup.sh
ls -l /root/backups/
crontab -l
```

The backup directory should contain a timestamped `.tar.gz` archive after successful execution.

## 6. Screenshot Evidence

- `screenshots/script-execution.png` - Script execution and backup verification.
- `screenshots/cron-schedule.png` - Installed Cron job configuration.

## Conclusion

This activity demonstrates how Bash scripts and Cron can automate repetitive cloud administration tasks. Automated backups can reduce reliance on manual execution, although backup monitoring and recovery testing are still necessary.
