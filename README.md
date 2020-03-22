# ChatlogGrapher

Create pretty graphs of chat log history.

Supports:
- Facebook Messenger (JSON export)
- Discord (TODO: still need to implement)
- please let me know if there is another chat service that provides consistently formatted data dumps that I can add support for...

How to use:
- Download your data!
  - Facebook Messenger: instructions at https://www.facebook.com/help/1701730696756992
    - Be sure to export in JSON format and *include* your chat data!
    - Unzip your export and put the folder (should be named something like FacebookName-12345) in `data`
  - Discord: instructions at https://support.discordapp.com/hc/en-us/articles/360004027692-Requesting-a-Copy-of-your-Data
    - TODO
- Install the dependencies
  - Jupyter (Notebook), numpy, pandas, matplotlib
- Run the code
  - `jupyter notebook` and open the main notebook file
  - TODO: add direct python code that can do everything?

Inspired by https://github.com/rohanp/MessengerGrapher (which handles messages through Facebook Messenger only)
