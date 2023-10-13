# X-Ui To Marzban Migrate Script

 | Simply Transfer Your Users From X-Ui to Marzban

## Table of Contents
- [About](#about)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Linux](#Linux)
- [Windows](#windows)

Make Sure To Change these variables before runing the script.
```python
# Define Variables for Both Panels

# X-Ui Panel

X_DOMAIN = "YOUR_DOMAIN"
X_PORT = "YOUR_PORT"
X_USERNAME = "YOUR_USERNAME"
X_PASSWORD = "YOUR_PASSWORD"
X_HTTPS = False  # Set to True to use HTTPS, False to use HTTP

# Marzban Panel

M_DOMAIN = "YOUR_DOMAIN"
M_PORT = "YOUR_PORT"
M_USERNAME = "YOUR_USERNAME"
M_PASSWORD = "YOUR_PASSWORD"
M_HTTPS = False  # Set to True to use HTTPS, False to use HTTP
```

## About

This script is designed to automate the management of user templates using the Marzban API. It securely logs into an admin panel, retrieves a list of user templates, adds new ones, modifies existing templates, and can also delete user templates when needed. It provides detailed logging for each operation, making it a valuable tool for efficiently managing user accounts in a web-based environment.

## Getting Started

First of all you need to enable Marzban API which you can use this command below
```bash
echo 'DOCS=True' | sudo tee -a /opt/marzban/.env
```
or manually open the .env file with this command
```bash
nano /opt/marzban/.env
```
and then add this line to the file
```python
DOCS=True
```
Finally Restart The Marzban
```sh
marzban restart
```
### Prerequisites
Python 3.0+ with requests library required. you cant run the script on python 2.0
### Linux
```bash
# Clone the Repository
git clone https://github.com/ItsAML/MarzbanUserTemplateManagment.git

# Change Directory
cd MarzbanUserTemplateManagment

# Install pip (if not already installed)
wget -qO- https://bootstrap.pypa.io/get-pip.py | python3 -

# Install Dependencies
python3 -m pip install -r requirements.txt

# Run the Script
python3 main.py
```
### Windows
```bash
# Clone the Repository
git clone https://github.com/ItsAML/MarzbanUserTemplateManagment.git

# Navigate to the Repository Directory
cd MarzbanUserTemplateManagment

# Install Python (if not already installed)
# Download and install Python from https://www.python.org/downloads/
# Ensure you add Python to your system's PATH during installation

# Install Dependencies
pip install -r requirements.txt

# Run the Script
python main.py
```