# ChatlogGrapher

Create pretty graphs of chat log history! Can combine information from multiple chat services all at once.

Supports:
- Facebook Messenger (JSON export)
- Discord (GDPR data request)
- Google Hangouts (Takeout)

## How to use

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
  - Make sure you have Conda installed
  - Set up the Conda environment: `conda env create -f environment.yml`
  - Activate the conda environment: `conda activate chatloggrapher`
  - If you don't want to have Conda installed... make sure you have the dependency packages installed: JupyterLab, numpy, pandas, matplotlib, gensim, nltk
- Run the code
  - Set up `aliases.json` to map multiple names/nicknames/usernames to each person's actual name
    - This is especially relevant for Discord, since Discord usernames are almost always different from someone's actual name and will also always include the 4-digit username ID.
    - If you have contacted the same person on multiple platforms where they may be listed under multiple names/usernames, make sure that those names are tied all to the same single name in the aliases file.
    - See the default lines in there for examples of how to write those lines.
    - Map any name/username to "null" to ignore it entirely.
  - Run `jupyter lab` and open the main notebook file `data_processing.ipynb`
  - Run the cells in order!

## Other Info & Credits

Potential future features?
- Support for Facebook group chat data (> 2 person chats)
- Support for DiscordChatExporter data
- Support for any other chat or chat log scraper service that provides consistently formatted data dumps!
- Put the code that's currently in `data_processing.ipynb` into an independent Python file of its own, or something that can be more easily run!

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
