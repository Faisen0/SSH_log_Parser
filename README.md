# Project Objectives
The goals of this project were designed to combine practical scripting, security monitoring, and GitHub workflow skills. Specifically, I aimed to:
- Build a functional security tool
- Track failed SSH login attempts.
- Identify offending IPs and optionally block them.
- Practice GitHub workflow and version control
- Create a repository with proper structure, README, .gitignore, and license.
- Use feature branches for each addition.
- Make all changes via pull requests.
- Write clear, descriptive commits and link them to issues for tracking.
- Practice project management skills
- Track tasks and improvements through GitHub Issues.
- Organize work visually with a Kanban board.
- Simulate code review even as a solo developer to evaluate and improve my own work.
- Improve documentation and communication
- Clearly communicate known issues and future enhancements.
- Tag stable versions (e.g. v1.0.0) and write release notes summarizing features and fixes.
- Learn how to maintain a clean, stable main branch while developing new features.



# Known Issues
Firewall configuration required: ufw must be set up properly to allow IP blocking.

WHOIS lookup may fail: Some IPs may not return ownership info or may take longer depending on network conditions.

Log file permissions: Running the script without sufficient permissions may prevent writing to 

# Future Improvements
Automatic WHOIS logging: Store WHOIS information for blocked IPs in the log file for auditing.

Configurable thresholds: Allow custom thresholds for failed SSH attempts before blocking.

Enhanced review output: Summarize blocked IPs, failed attempts, and WHOIS info at the end of script runs.

Notification integration: Send alerts via email or messaging platforms when new IPs are blocked.

Web dashboard: Optional interface for monitoring failed SSH attempts and blocked IPs visually

## Project Board

You can track the progress of this project on the [Kanban board](https://github.com/users/Faisen0/projects/2/views/1).