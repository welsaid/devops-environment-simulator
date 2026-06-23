# Devops Environment Setup Simulator

## Overview
A simulated DevOps project structure built entirely from the linux terminal

## Skills used
- Linux file & directory management
- Vim editor
- User & group management
- File permission & ownership
- Bash scripting
- Command chaining with &&

## Project Structure
```
/opt/devops-project/
|── README.md
|── config/
|   |── app.conf
|   └── db.conf
|── logs/
|   └── setup.log
└── scripts/
    └── validate.sh
```

## How to run
1. Clone the repository
2. Navigate to the project directory
   cd /opt/devops-project
3. Run the validation script
   bash /opt/devops-project/scripts/validate.sh

## Expected output
```
Checking project structure...
README.md config logs scripts
app.conf db.conf
setup.log
validate.sh
Validation complete
```
## Commands used
```bash
# Create directory structure
mkdir -p /opt/devops-project/{config,logs,scripts}

# Create and edit files
vim config/app.conf
vim config/db.conf
vim logs/setup.log
vim scripts/validate.sh

# Change ownership
chown -R devops-user /opt/devops-project

# Change permissions
chmod 700 scripts/validate.sh

# Confirm everything
ls -l /opt/devops-project
ls -l /opt/devops-project/config
cat /opt/devops-project/README.md

# Chain commands
ls /opt/devops-project && ls /opt/devops-project/config && cat /opt/devops-project/README.md
```
