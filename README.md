# SSH Log Parser 
SSH Security Log Parser & IP Blocker

A lightweight Bash tool to monitor SSH login attempts, log offending IPs, and optionally block them while providing additional WHOIS information for auditing.

# Features
Monitor Failed SSH Logins
Extracts failed login attempts from journalctl for ssh.service.

IP Blocking
Prompts the user to block offending IPs via ufw.

Logging
All blocked IPs are logged to ssh.log using tee so the log file receives entries while the terminal prints IPs in real-time.

WHOIS Lookup
Queries blocked IPs to retrieve ownership information for auditing purposes.

Threshold-based detection
Automatically identifies IPs with repeated failed login attempts (default: 3).

# Installation
Clone the repository:

git clone https://github.com/Faisen0/SSH_log_Parser.git
cd SSH_log_Parser



Make the script executable:

chmod +x ssh_log_parser.sh

# Requirements
Ensure ufw is installed if you want to block IPs.

Optionally, ensure whois is installed for IP lookup:

sudo apt install whois


# Usage
Run the script:

./ssh_log_parser.sh


Example behavior:
The Failed Logins is/are:
192.168.1.101
192.168.1.102

After listing the IPs, you are prompted to block them:

Do you want to block these IPs? (y/n)


WHOIS lookup will print ownership info alongside each IP if enabled and save them to lookup.txt 

ssh.log contains all blocked IPs .

This file is ignored by Git (via .gitignore) to prevent accidental commits of runtime logs.


Example log entry:

192.168.1.101


GitHub Workflow

Branches are used for features like feature/firewall-block or feature/lookup.

Use commit messages referencing issues to automatically close them:

Closes #1



Pull Requests summarize features and link commits/issues.

.gitignore ensures log files are never pushed accidentally.


# Security Notes

When enabling IP blocking on a live system:

Ensure your own IP is not accidentally blocked.

Use SSH keys instead of passwords for safer authentication.

Consider running the script with sudo only when necessary.


# Future Enhancements

Automatic WHOIS logging to the log file.

Support for custom thresholds and automatic unblocking.

Integration with alerting or notification systems.

Optional reverse SSH setup for devices behind NAT/mobile networks.
