# Initia_Governance_bot
Governance Bot which will make your work easier
# Initia Voting Script

This script automates the voting process on the Initia testnet. It checks for active proposals and sends them to a specified Telegram chat. The script then waits for user input or votes automatically when the voting period is about to end.

## Prerequisites

1. [Install Go](https://golang.org/doc/install) if not already installed.
2. Install the Initia binaries and ensure they are in your PATH.
3. Install `jq` for JSON processing:
    ```bash
    sudo apt-get install jq
    ```

## Setup

1. **Clone the repository or download the script:**
    ```bash
    git clone https://github.com/web3validator/Initia_Goverannce_bot.git
    cd Initia_Goverannce_bot
    ```

2. **Edit the script (`initia_vote.sh`):**
    ```bash
    nano initia_vote.sh
    ```
    Update the following variables with your specific values:
    - `PROJECT`
    - `VOTE_ADDRESS`
    - `BIN`
    - `NODE_HOME`
    - `CHAT_ID`
    - `BOT_TOKEN`
    - `KEYRING`
    - `PASWD`

3. **Make the script executable:**
    ```bash
    chmod +x initia_vote.sh
    ```

## Running the Script

To run the script manually:
```bash
./initia_vote.sh
 ```
## Automate with Crontab
Open crontab:

 ```
crontab -e
 ```
Add the following line to run the script every hour:

 ```
0 * * * * /path/to/your/repository/initia_vote.sh
 ```

Replace /path/to/your/repository/ with the actual path to the script.

Save and exit the crontab editor.

## Logging
The script does not produce log files by default. To log the output, you can modify the crontab entry:

 ```
0 * * * * /path/to/your/repository/initia_vote.sh >> /path/to/your/repository/initia_vote.log 2>&1
 ```
## Notes
Ensure the BOT_TOKEN and CHAT_ID are kept secure and not exposed in public repositories.
Change PASWD if using keyring-backend os to the appropriate password.
For more information or assistance, please refer to the [Initia documentation.](https://docs.initia.xyz/)
