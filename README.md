# HTTPD Web Server Setup Script

This script automates the installation, configuration, and deployment of a website using the HTTPD web server.

## Prerequisites

- CentOS, RHEL, or Amazon Linux with `sudo` access.
- Internet connectivity.

## How to Run

1. Save the script as `setup_httpd.sh`.
2. Make it executable:
   ```bash
   chmod +x setup_httpd.sh
3. Run the script with sudo:
   sudo ./setup_httpd.sh
4. Verify:
   Check service status:
     sudo systemctl status httpd

##What It Does
- Installs dependencies: httpd, wget, unzip.
- Starts and enables the HTTPD service.
- Downloads and deploys the website template.
- Restarts HTTPD and cleans up temporary files.
