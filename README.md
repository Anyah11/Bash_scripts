#HTTPD Web Server Setup Script

This script automates the installation, configuration, and deployment of a website using the HTTPD web server. It downloads a template, deploys it to the web server directory, and ensures the server is running properly.

#Prerequisites

Ensure the following requirements are met before running the script:

Operating System: The script is designed for systems using yum package manager (e.g., CentOS, RHEL, or Amazon Linux).

User Permissions: Run the script with a user that has sudo privileges.

Network Connectivity: The server must have access to the internet to download the template.

#Script Details

Steps Performed by the Script

Variable Declaration:

PACKAGE: List of packages to install (httpd, wget, unzip).

SVC: Service name (httpd).

URL: URL of the website template to download.

ART_NAME: Name of the downloaded artifact.

TEMPDIR: Temporary directory for processing the files.

Install Required Packages:
Installs the necessary dependencies for the HTTPD service and file operations.

Start and Enable HTTPD Service:
Starts the HTTPD service and ensures it starts on boot.

Download and Deploy Website:

Creates a temporary directory.

Downloads and extracts the website template.

Copies the template files to /var/www/html/.

Restart HTTPD Service:
Restarts the HTTPD service to apply changes.

Cleanup Temporary Files:
Removes the temporary directory to save disk space.

How to Run the Script

Clone or Copy the Script:
Save the script as setup_httpd.sh.

Make the Script Executable:

chmod +x setup_httpd.sh

Run the Script:
Execute the script with sudo privileges:

sudo ./setup_httpd.sh

Verify the Deployment:

Check the HTTPD service status:

sudo systemctl status httpd

Ensure the website is accessible by visiting the server's IP address or hostname in a web browser:

http://<your-server-ip>

Expected Output

The script installs the necessary packages and starts the HTTPD service.

The website files are deployed to /var/www/html/.

The HTTPD service is restarted successfully.

Temporary files are cleaned up.
