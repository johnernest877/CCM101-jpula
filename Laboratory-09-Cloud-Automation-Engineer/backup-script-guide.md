Awesome! 

### **Step 1: Upload Your Screenshots**
Make sure you drag and drop both **`script-execution.png`** and **`cron-schedule.png`** into your `screenshots` folder in GitHub Codespaces.

---

### **Step 2: Checkpoint 6 (Technical Documentation)**
Now we need to document your work. Here is the exact Markdown code for your **`backup-script-guide.md`** file. Click the "Copy" button at the top right of the box below and paste it directly into your file:

```markdown
# Backup Script Guide

## The Bash Script
Below is the full code for the automated backup script:

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## Understanding File Permissions
**What did the `chmod +x` command do?**
The `chmod +x backup.sh` command changed the file permissions of the script to make it executable. By default, Linux treats text files as plain data for security reasons. Adding the `+x` flag explicitly grants the user permission to run the file as a program.

## Cron Schedule Breakdown
The following cron expression was added to the crontab to schedule the backup:
```text
0 2 * * * /root/backup.sh
```

**What each time-field means:**
- **Minute (0):** The task will run at the 0th minute of the hour.
- **Hour (2):** The task will run at 2:00 AM.
- **Day of Month (*):** The task will run every day of the month.
- **Month (*):** The task will run every month of the year.
- **Day of Week (*):** The task will run every day of the week.
- **Command (/root/backup.sh):** This is the exact path to the script that will be executed automatically.
```
