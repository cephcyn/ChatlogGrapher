# ChatlogGrapher

Create pretty graphs of chat log history.

Supports:
- Facebook Messenger (JSON export)
- Discord (GDPR data request, TODO: DiscordChatExporter???)
- Google Hangouts (Takeout)
- please let me know if there is another chat or chat log scraper service that provides consistently formatted data dumps that I can add support for!

How to use:
- Download your data
  - Facebook Messenger
    - instructions at https://www.facebook.com/help/1701730696756992
    - Be sure to export in JSON format and *include* your chat data!
    - Unzip your download, make sure the folder is named something like "facebook-Name12345", and put it in `data`
  - Discord (GDPR request)
    - instructions at https://support.discordapp.com/hc/en-us/articles/360004027692-Requesting-a-Copy-of-your-Data
    - Unzip your download, rename the folder named "package" to something like "discord-YourUsername", and put it in `data`
    - NOTE that Discord data export only includes your sent messages, not received messages!!!!
  - Google Hangouts
    - instructions at https://support.google.com/accounts/answer/3024190?hl=en
    - Be sure to *include* your Hangouts (chat) data!
    - Unzip your download, rename the folder named "Takeout" to something like "google-YourUsername", and put it in `data`
- Install the dependencies
  - Jupyter (Notebook), numpy, pandas, matplotlib
- Run the code
  - `jupyter notebook` and open the main notebook file
  - TODO: add direct python code that can do everything?

Potential future features?
- Support for group chat data (> 2 person chats)

Inspired by https://github.com/rohanp/MessengerGrapher (which handles messages through Facebook Messenger only)
