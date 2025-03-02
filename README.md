# TeleBot-Taxi
## Driver Bot - User Documentation

This document outlines how to use the Driver Bot in Telegram to automate bidding on driving jobs.

**I. Getting Started**

1.  **Find the Bot:** Search for your bot's username in Telegram and start a private chat.
2.  **Use `/start`:** Send the `/start` command to initiate the bot setup.

**II. Setting Up Preferences**

After sending `/start`, the bot will guide you through the following steps:

1.  **Share Your Location:**
    * The bot will present a "Share Location" button.
    * Tap the button to share your current location. This is crucial for calculating drive times to pickup locations.

2.  **Set Your Car Type(s):**
    * The bot will prompt you to enter your car type(s).
    * You can enter multiple car types, separated by commas (e.g., `sedan, suv, maxi`).
    * Valid car types are: `sedan`, `suv`, `maxi`, `wheelchair`, `baby`, `any`, `11 seater`.
    * Using `any` will allow the bot to bid on all jobs regardless of car type.
    * If you enter an invalid car type, the bot will ask you to re-enter the car type correctly.

3.  **Activate the Bot:**
    * After setting your car type(s), the bot will show "Activate Bot" and "Deactivate Bot" buttons.
    * Tap "Activate Bot" to start the bot.

**III. Adding the Bot to Groups**

1.  **Add the Bot to Groups:** Add the Driver Bot to the Telegram groups where you want it to monitor for job postings.
2.  **Use `/add_group` in Each Group:** In each group, send the `/add_group` command. This tells the bot to monitor that specific group for jobs.

**IV. Using the Bot**

1.  **Automatic Bidding:** Once activated and added to groups, the bot will automatically monitor for new job postings.
2.  **Job Parsing:** The bot will parse the job postings to extract information like pickup location, car type, and ready time.
3.  **Bid Decision:** The bot will check if the job matches your preferences (car type, maximum distance).
4.  **Automatic Bidding:** If the job matches, the bot will automatically send a bid ("1") in the group.
5.  **Private Notifications:** The bot will send you a detailed notification in your private chat, including:
    * Pickup and dropoff locations
    * Car type
    * Ready time
    * Payment type
    * Drive time
    * The group where the bid was placed.

**V. Commands**

* **`/start`:** Initiates the bot setup process (share location, set car type, activate).
* **`/add_group`:** Adds the current group to the bot's watched groups.
* **`/activate`:** Manually activates the bot (if you prefer not to use the button).
* **`/deactivate`:** Manually deactivates the bot (if you prefer not to use the button).

**VI. Deactivating the Bot**

1.  **Tap "Deactivate Bot":** In your private chat with the bot, tap the "Deactivate Bot" button.
2.  **Use `/deactivate`:** Alternatively, you can send the `/deactivate` command.

**VII. Location Updates**

* The bot will automatically request your location every 2 minutes.
* Make sure your device's location services are enabled and that Telegram has permission to access your location.

**VIII. Troubleshooting**

* **Bot doesn't respond:** Check your internet connection and ensure the bot is still running.
* **Bot doesn't bid:** Check the logs (if you have access to them) or review your preferences to ensure they match the job postings.
* **Location updates don't work:** Check your device's location settings and Telegram's permissions.
* **Bot doesn't add groups:** Ensure the bot has permission to read messages in the groups and that you are using the `/add_group` command correctly.
* **Geocoding Errors:** If the bot cannot get the coordinates of the pickup location, make sure the location name in the job post is spelled correctly.

**IX. Important Notes**

* **Keep your bot token private.** Never share it with anyone.
* **Ensure your device has a stable internet connection.**
* **Keep your bot's Python script running.** If the script stops, the bot will stop functioning.
* **Respect Telegram's terms of service and group rules.**
