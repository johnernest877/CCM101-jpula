# Laboratory 09: Cloud Automation Engineer

## Mission Overview
This final mission focuses on eliminating manual human error in cloud operations. Acting as a Cloud Automation Engineer, I wrote a Bash script to automate data backups and used the Linux Cron scheduler to ensure the task runs autonomously every night, ensuring data reliability at scale.

## Objectives
- Understand the fundamental syntax of a Bash shell script, including variables and basic commands.
- Use a command-line text editor (nano) to write and save executable scripts.
- Modify Linux file permissions using the chmod command.
- Understand task scheduling and the syntax of a Linux crontab.
- Document automation code and Cron job configurations using Markdown.

## Commands Executed
- `mkdir app-data` (Create dummy client data)
- `nano backup.sh` (Write the automation script)
- `chmod +x backup.sh` (Grant execution permissions)
- `./backup.sh` (Test the script manually)
- `crontab -e` (Edit the cron schedule)
- `crontab -l` (Verify the scheduled job)

## Skills Learned
- Writing and formatting functional Bash scripts for automation.
- Understanding Linux file permissions and the importance of executable flags.
- Configuring the Linux crontab to schedule automated tasks based on specific time parameters.
- Documenting code functions and scheduling syntax accurately using Markdown.