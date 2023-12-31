# SafeLink Discord Bot

## Description
SafeLink is a Discord bot designed to enhance server security by scanning messages for potentially harmful URLs. It checks for short URLs, which are often used in phishing and scamming attempts, and analyzes other URLs using the VirusTotal API to detect malicious links.

## Features
- **Short URL Detection**: Automatically detects and alerts about the usage of short URLs in messages.
- **Malicious Link Detection**: Scans URLs using the VirusTotal API and alerts if the link is potentially harmful.
- **Moderator Notification**: Notifies moderators when a short URL is detected for immediate action.
- **Channel Specific**: Operates only in specified Discord channels for targeted monitoring.

## Setup
1. **Prerequisites**:
    - Python 3.8 or higher
    - Discord API account and a bot token
    - VirusTotal API key

2. **Installation**:
    - Clone the repository or download the source code.
    - Install required packages: `pip install discord.py requests python-dotenv`

3. **Configuration**:
    - Create a `.env` file in the root directory.
    - Add your Discord Bot Token and VirusTotal API Key:
      ```
      DISCORD_TOKEN=your_discord_token_here
      VIRUSTOTAL_API_KEY=your_virustotal_api_key_here
      ```
    - Modify the `SPECIFIC_CHANNEL_ID` list in the script to include the IDs of the channels where the bot should operate.
    - Update the `MODERATOR_IDS` list with the Discord IDs of the moderators.

4. **Running the Bot**:
    - Execute the script: `python safelink.py`
    - The bot should now be running and monitoring the specified channels.

## Usage
- The bot automatically scans all messages in the specified channels.
- If a short URL is detected, the bot sends a warning message and notifies the moderators.
- For other URLs, the bot checks their safety via VirusTotal and alerts if any malicious link is found.

## Contributing
Contributions, issues, and feature requests are welcome. Feel free to check [issues page](link-to-your-issues-page) if you want to contribute.

## License
[MIT](link-to-your-license)
