# Initia_Governance_bot
Governance Bot which will make your work easier
# Initia Voting Script

This script simplifies the voting process on the Initia testnet. It checks for active proposals and sends their details to a specified Telegram chat using API requests. Users can then vote by selecting options in the Telegram chat. The script captures these responses and submits the votes accordingly.

**Note:** This script does not perform automatic voting. It facilitates the voting process by integrating with Telegram for user input.

<img width="362" alt="image" src="https://github.com/web3validator/Initia_Governance_bot/assets/59205554/6281bad0-e3cb-4f46-b673-3bea7a66f1fa">

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
0 * * * * /home/admin/Initia_Goverannce_bot/initia_vote.sh
 ```

Replace /home/admin/Initia_Goverannce_bot with the actual path to the script.

Save and exit the crontab editor.

## Logging
The script does not produce log files by default. To log the output, you can modify the crontab entry:

 ```
0 * * * * /home/admin/Initia_Goverannce_bot/initia_vote.sh >> /home/admin/Initia_Goverannce_bot/initia_vote.log 2>&1
 ```
## Notes
Ensure the BOT_TOKEN and CHAT_ID are kept secure and not exposed in public repositories.
Change PASWD if using keyring-backend os to the appropriate password.
For more information or assistance, please refer to the [Initia documentation.](https://docs.initia.xyz/)
