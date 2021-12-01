

<p>
  <img src='https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white' alt='Windows'>
  <img src='https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black' alt='Linux'>
  <img src='https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0' alt='MAC OS'>

  <h2>Splinterlands Trader Bot</h2>

  <p>
	A trading bot written in Python that makes a profit by buying underpriced cards and quickly reselling them.
  </p>
</p>

<details open="open">
  <summary>Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About the project</a>
      <ul>
        <li><a href="#built-with">Built with</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#operating-system">Operating System</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li>
      <a href="#setting-it-up">Setting it up</a>
      <ul>
        <li><a href="#account-information">Account Information</a></li>
        <li><a href="#process-parameters">Process Parameters</a></li>
      </ul>
    </li>
    <li>
      <a href="#how-to-use">How to use</a>
    </li>
    <li><a href="#things-to-note">Things to note</a></li>
    <li><a href="#common-errors-and-how-to-fix-them">Common errors and how to fix them</a></li>
    <li><a href="#faqs">FAQs</a></li>
    <li><a href="#donations">Donations</a></li>
  
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
# About The Project

Splinterlands Trader Bot is a free tool programmed in Python that aims to make a steady profit by buying underpriced cards in the Splinterlands market and quickly reselling them.

It does so by using the Splinterlands API and interacting directly with the Hive Blockchain.

It mimics a human-like reasoning to evaluate potential offers, filters them according to a set of adjustable parameters, and selects the best among them. After that, it proceeds to buy the card, and as soon as the purchase is confirmed, it posts it again with a higher price, but still lower than the minimum price posted (in order to resell quickly).

The bot works because of two main reasons:
* Since it's constantly checking the market, it will find all profitable operations as soon as they are posted.
* Even though the margin of each operation might be small (which could discourage a human user), the bot will keep on buying and selling, and the profit will keep adding up.

Some of its features:
- Fully automated buying and selling.
- Constant maintenance of the posted cards, updating the price if necessary.
- Adjustable minimum balance, so you can set exactly up to how much money the bot will use to buy cards.
- A lot of configurable parameters to adjust the bot's behaviour.
- It never takes a coffee break!

How do I (the developer) make money? The bot is free to download, and you never need to pay any money. Every time the bot successfully sells a card, it will transfer 20% of the profit it made to my account. What does this means?
- You don't need to pay at all until the bot makes a profit.
- The 20% is applied to the profit, which takes into account the sale fee. The exact value of the profit is `sale_price * (1-sale_fee) - buy_price`, so you will never lose money.
- You will keep 80% of the operation profit.

## Built With

This project is built with [Python3.10](https://www.python.org/downloads/)

<!-- GETTING STARTED -->
# Getting Started

To get a local copy up and running follow these simple steps.

## Prerequisites

Splinterlands Trader Bot is completely free to use and there are no setup costs.

- Windows, Mac, Linux
- A good internet connection
- Python 3.10 installed (although some support is included for older versions)
- Hive account username and private key

## Operating System

The bot can be run on the following OS:
  1.  Windows (you can use the PowerShell)
  2.  Linux (you can use any terminal)
  3.  Mac (you can use any terminal)

# Installation

## Windows

1. Download and install [Git](https://git-scm.com/) and [Python3.10](https://www.python.org/)
2. Clone the repo: 

      ```sh
      git clone https://github.com/chief-gant/SplinterlandsTraderBot.git
      ```

3. Go to repo directory
      ```sh
      cd SplinterlandsTraderBot
      ```

4. Install the required libraries by running: 
      ```sh
      pip install -r requirements.txt
      ```
   
## Linux User
Install the package with 

```sh 
sudo su
```

Debian / Ubuntu: 
1. Install Git and Python if you don't have them:

	```sh
	apt install git && apt install python3-pip
	```

2. Clone the repo: 

      ```sh
      git clone https://github.com/chief-gant/SplinterlandsTraderBot.git
      ```

3. Go to repo directory
      ```sh
      cd SplinterlandsTraderBot
      ```

4. Install the required libraries by running: 
      ```sh
      pip install -r requirements.txt
      ```

Fedora Linux / Centos
1. Install Git and Python if you don't have them:

	```sh
	dnf install git && dnf install python3-pip
	``` 

2. Clone the repo: 

      ```sh
      git clone https://github.com/chief-gant/SplinterlandsTraderBot.git
      ```

3. Go to repo directory
      ```sh
      cd SplinterlandsTraderBot
      ```

4. Install the required libraries by running: 
      ```sh
      pip install -r requirements.txt
      ```

Arch Linux
1. Install Git and Python if you don't have them:

	```sh
	pacman -S git && pacman -S install python3-pip 
	``` 

2. Clone the repo: 

      ```sh
      git clone https://github.com/chief-gant/SplinterlandsTraderBot.git
      ```

3. Go to repo directory
      ```sh
      cd SplinterlandsTraderBot
      ```

4. Install the required libraries by running: 
      ```sh
      pip install -r requirements.txt
      ```

## Mac

1. Download and install [Git](https://git-scm.com/) and [Python3.10](https://www.python.org/)
2. Clone the repo: 

      ```sh
      git clone https://github.com/chief-gant/SplinterlandsTraderBot.git
      ```

3. Go to repo directory
      ```sh
      cd SplinterlandsTraderBot
      ```

4. Install the required libraries by running: 
      ```sh
      pip install -r requirements.txt
      ```

# Setting it up

In order for the bot to work, it requires to complete two files, `process_parameters.json` and `account_info.json`.

## Account information

A file named `account_info.json.sample` is uploaded in the repo. However, it doesn't have information of any real account, so it won't do anything. You have to rename this file to `account_info.json` (delete the ".sample" part). Then you have to edit the file in a text editor and change the information to that of the account you want to use the bot with.

After "username", complete with your username between quotes (") without the "@". In my case, for example, it would look like:
```
"username": "chief-gant",
```

Then, after "active_key" you have to input that username's active key. This is needed in order to automatically buy, post and update the price of the cards. This should look like:
```
"active_key": "JKjkasjklJ86asd7NoyMyActualKey786JKSkkajIijka9KaO"
```

Your key is never shared with anyone or stored in any part of the process. <b>Never share your key with anyone else.</b> If someone asks you for your key, <b> do not trust this person</b>.

## Process parameters

With this file you can control various aspects of the bot. The repo includes a file `process_parameters.json.sample` with settings that I found optimal, but you are welcome to change them and try out alternatives. You have to rename this file to `process_parameters.json` (delete the ".sample" part), and then you can change whatever setting you want. If you leave them as is, it will work nonetheless.

About the parameters:
1. `fixed_price_interval`: since the bot is always checking for the posted card to have the minimum price available, this parameter defines how often it changes the price. The unit is minutes. If this is set to be 0, every single time a lower priced post appears, the bot would reduce the price to match it (as long as it can do without losing money on the operation); in that case, the price would be easy to manipulate by other users. Therefore, I recommend having a large interval, like 300 minutes (which translates to 5 hours).
2. `minimum_balance`: this defines how much money the bot can't use, so you can leave a portion of your DECs for other purposes. The unit is dollars. For example, if you set it to 10, the bot will never make a purchase that would let the balance drop below 10. During the execution, when the bot prints the available Balance, it will first substract the `minimum_balance` you set. In the example, if you have $15 and you set a minimum balance of $10, it wil show: `Balance: $5.00`. In the file included this is set to 0, you should change it as you see fit (maybe start with lower amounts while you check out how it works).
3. `min_abs_gain`: The absolute value of the profit to be made by an operation to be considered viable. The unit is dollars. If you leave a big number, the bot will take longer to find suitable offers. You can start with a bigger number and then lower it if you don't like to wait. The upside of the lower priced operations is that they appear more frequently and they sell quicker. In the file included, this is set to 0.1 (10 cents).
4. `min_rel_gain`: The relative value of the profit to be made by an operation to be considered viable. It's highly recommended to not go lower than 7-8% with this parameter. If the parameter is set, for example, to 5%, it will buy cards that are approximately 5% underpriced, which doesn't make them necessarily good offers (they might not sell as quickly as a more underpriced offer). In the file included it is set to 0.1 (10%), which is what I personally use.
5. `min_post_number`: The minimum number of offers a card should have in order to be considered. If a card has a low amount of posts, this means the circulation is low, so the price might not be stable. If there are only a bunch of offers, the bot could fail to determine the "real price" and think an offer is underpriced. Therefore, this number should be no less than 40 approximately. In the file included it is set to 50, which is what I personally use.


# How to use

In a command prompt, you should check what version you have and what's the exact command name by trying the following:
```sh
python --version  # If this prints out 3.10.x you're all set (use command python)
python3 --version  # If this prints out 3.10.x you're all set (use command python3)
python3.10 --version  # If this prints out 3.10.x you're all set (use command python3.10)
```

If you have an older version:
* If your version is 3.9.x, use whatever command worked for you in the previous step, with the file `splinterlands_trader_bot-39.pyc`
* If your version is another one, please try to upgrade to Python3.10, and if you can't you should <a href="https://github.com/chief-gant/SplinterlandsTraderBot/issues">open an issue</a> (I will add support for previous versions in the near future)

By now you should now the command (`python`|`python3`|`python3.10`) that works and the file you should use (`splinterlands_trader_bot.pyc` if you have Python3.10).

Go into the Splinterlands Trader Bot directory and run the command with the file. For example:

```sh
python splinterlands_trader_bot.pyc
```
```sh
python3 splinterlands_trader_bot.pyc
```
```sh
python3 splinterlands_trader_bot-39.pyc  # If you have Python3.9
```

# Things to note

- You can change the process parameters during the process execution, only by changing the file and saving it modified. The modifications will take place as soon as the current iteration ends.

- BE PATIENT. The cards should sell fairly quickly, but if they don't, just give it some time. Some operations are done in less than 10-15 minutes, while other take a whole week. Keep in mind that during the season, the prices fluctuate, so for example, if it's the last few days, it will be harder to sell.

- The bot will generate two files, `bot_activity.txt` and `bot_activity_readable.txt`. In the first one, it keeps a log of every operation it starts, and also any price update it makes. <b>Don't modify it</b>. Doing so could cause unexpected results, or the bot could completely fail to work. The second one is not used by the bot, it's for your reading pleasure.

- The bot keeps a log of every operation it starts (by purchasing and posting the card) and it updates the price if needed. It's not recommended to try and sell those cards manually, since you might sell the at a price too low, and therefore end up losing money.

- Make sure your input a private key in `account_info.json` and not a seed phrase.

- Each card should be only posted once at a time. Sometimes the API takes a little longer to delete a post of a card already bought, and could lead to this warning message. Don't worry, it should fix itself.

# Common errors and how to fix them

```When executing pip install... a giant error code appears```: sometimes a few key items needed to make Python and these modules work are missing.
* For Windows, follow these two steps in order to solve this:
  1. Install `Windows SDK` and `MSVC` following <a href="https://www.scivision.dev/python-windows-visual-c-14-required/">these instructions</a>.
  2. Download <a href="http://slproweb.com/products/Win32OpenSSL.html">OpenSSL</a> for Windows (the regular version, not the light one) and install in your main disk (e.g "C:\OpenSSL-Win64"). DO NOT INSTALL IN PROGRAM FILES - it won't work.
* For Linux, run:

```sh
sudo apt-get install libssl-dev
```

* For Mac, run:
```sh
brew install openssl
brew link openssl --force
```
---
```RuntimeError: Bad magic number in .pyc file```: The bot needs Python 3.10 to run. I will try and add scripts that are compatible with previous versions, but in the meantime please upgrade to Python 3.10 as instructed in the installation steps. Here's a handy guide to download a specific Python version for <a href="https://linuxize.com/post/how-to-install-python-3-9-on-debian-10/">Linux Debian</a> and <a href="https://linuxize.com/post/how-to-install-python-3-9-on-ubuntu-20-04/">Linux Ubuntu</a>.

---
```ModuleNotFoundError: No module named 'XX'```: This means you don't have a certain module installed. To fix it, you should execute `pip install -r requirements.txt` (this will install all necessary modules) or `pip install XX` where XX would be the module name which appears in the error message.

---
```Problems while loading process parameters```: The bot is having problems when reading `process_parameters.json`. To make sure it works, download it again from the repo and then modify it again, making sure you don't the structure or the value types (e.g. if the original value is a number, make sure to input a number).

---
```Error while loading account info```: The bot is having problems when reading `account_info.json`. To make sure it works, download it again from the repo and then modify it again. Check that the username doesn't start with @, and it's between quotes ("). Check that the active_key is also between quotes.

---
```Username XX not found```: The username wasn't found in the Splinterlands API. Check that the username you completed in `account_info.json` is OK, and it doesn't start with a @. For more information on how to complete `account_info.json`, check the <a href="#account-information">Account Information</a> section.

# FAQs

```The message "No good offers found" keeps appearing. What can I do?```
- Wait. There won't be good offers constantly, but the idea is that the bot will check non-stop and quickly take advantage of whatever offer appears.
- You can also try and lower the requirements in `process_parameters.json`. I recommend you read the <a href="#process-parameters">Process Parameters</a> section for more info on what to modify and how.

```The message "There was a problem while buying the card" keeps appearing. What does this means?```
- Some posts are "garbage posts", when you try to buy them they don't actually exist. Other times, the card was already bought but the post still appears in the API, because it takes some time to update. All you can do is wait for the card to disappear from the API, it shouldn't take a lot of iterations.

```The message "We cant go any lower with the price of..." keeps appearing.```
- The bot will never set a price as low as to lose money. Sometimes some cards appear that are underpriced, even more so than the card the bot already bot. All there is to do is wait, the prices fluctuate and it will probably will go up again at some point.

# Donations

If you enjoyed using the bot, any and all donations are welcome. You can donate through the Splinterlands app, or to a BSC wallet.

| Platform | Information |
|:---:|:---:|
| Splinterlands | Username: @chief-gant
| BSC Wallet | BSC Address: 0x1ea7F8108d0681204b1a4458AAB8Ce0b19841042
