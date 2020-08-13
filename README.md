# ChatlogGrapher

Create pretty graphs of chat log history!

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
  - Jupyter (Notebook), numpy, pandas, matplotlib, gensim, nltk
  - TODO: create a nice handy environment.yml to do this for you
- Run the code
  - `jupyter notebook` and open the main notebook file
  - TODO: add direct python code that can do everything?

Potential future features?
- Support for group chat data (> 2 person chats)

Inspired by https://github.com/rohanp/MessengerGrapher (which handles messages through Facebook Messenger only)

## Examples

![Graph of how many people I talk to each day](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/people_count_dates.png "Graph of how many people I talk to each day over time")


![Graph of how many people I've talked to at some times of day](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/people_count_times.png "Graph of how many people I've talked to at some times of day")


![Graph of how many messages I send each day](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_count_dates.png "Graph of how many messages I send each day")


![Graph of how many messages I've sent at some times of day](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_count_times.png "Graph of how many messages I've sent at some times of day")


![Graph of the distribution of all message lengths recorded](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_length.png "Graph of the distribution of all message lengths recorded")


![Graph of how many total messages I've exchanged with the top 6 people I contact over time](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_count_cumulative_top6.png "Graph of how many total messages I've exchanged with the top 6 people I contact over time")


![Graph of how actively I've exchanged messages with the top 6 people I contact](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_count_active_top6.png "Graph of how actively I've exchanged messages with the top 6 people I contact")


![Graph of what times of day I've exchanged messages with the top 6 people I contact](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_count_times_top6.png "Graph of what times of day I've exchanged messages with the top 6 people I contact")


![Graph of what times of day I've exchanged messages with specific people](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_count_times_selected.png "Graph of what times of day I've exchanged messages with specific people")


![Graph of the message length distributions for messages I've exchanged with specific people](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_length_selected.png "Graph of the message length distribution for messages I've exchanged with specific people")


![Graph of what times of day I've exchanged messages with specific people (Normalized for how many messages I've sent them in total over the time period)](https://raw.githubusercontent.com/cephcyn/ChatlogGrapher/master/outputs/messages_normcount_times_selected.png "Graph of what times of day I've exchanged messages with specific people (Normalized for how many messages I've sent them in total over the time period)")
