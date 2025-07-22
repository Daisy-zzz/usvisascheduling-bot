#  US Visa Scheduling Bot

  
An automated bot for monitoring US visa appointment availability and handling the login process for the US visa scheduling system.

Please note that this bot is only applicable for regions using CGI platform for visa appointments.


##  Features

  

-  **Automated Login**: Handles the two-step login process including username/password authentication and security questions

-  **Captcha Solving**: Uses GPT-4o-mini to automatically solve captchas

-  **Appointment Monitoring**: Continuously monitors for available appointment slots

-  **Telegram Notifications**: Sends notifications when appointments become available

-  **Session Persistence**: Maintains login sessions across runs using browser profiles

-  **Waiting Room Handling**: Automatically handles high-traffic waiting rooms

  

##  Prerequisites

  

- Python 3.7+

- OpenAI API key

- Telegram bot token and chat ID (for notifications)

  

##  Installation

  

1. Clone the repository:

```bash

git clone https://github.com/tpm2dot0/usvisascheduling-bot

cd usvisascheduling-bot

```

  

2. Install dependencies:

```bash

pip install -r requirements.txt

```

  

3. Fill your OpenAI API Key at `.env`
  

4. Edit `credential.json` with your visa scheduling account details
  

5. Update notification settings:

- Edit `visa_checker.py` and replace the `NOTIFY_URL` with your Telegram bot details:

```python

NOTIFY_URL = "https://api.telegram.org/bot<YOUR_BOT_TOKEN>/sendMessage?chat_id=<YOUR_CHAT_ID>&text=hasSlot"

```

  

##  Usage

  

Run the bot:

```bash

python  visa_checker.py

```