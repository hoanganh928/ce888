# Lab1 

## Installing and setting up the VM 

* (Quick) format your USB stick to NTFS

* Download in your tmp directory: [mlvm](https://docs.google.com/uc?id=0B_kDfEzMuWD6ZGJFU1VfeEY3TnM&export=download)
* Unrar the VM in your tmp directory
* Copy the VM to the USB stick
* Start the VM 
	* Double click on `mlvm.vbox`
	* Try to start the VM 
	* An error might pop up
	* Press change settings and change the network adapter to another value, and then back to NAT
* Login using mlvm/mlvm
	* Click on the vm window
	* (To exit vm mode press ctrl+alt)
	* Type "sudo reboot" to reboot the machine
	* Find your local ip address (type "ifconfig")
	* Ping google to check if you have network access
	* Open an explore window and type "\\\\mlvm\\mlvm"
		* If that doesn't work, use the local IP you got from ifconfig (`192.168...`)
			* "\\\\192.168....\\mlvm"
		* Enter your credentials (mlvm/mlvm)
	* For ease of use (so you can copy paste) start an ssh session with the vm (again using the local address)


## Creating a github account and CE888 project
* Got to [www.github.com](www.github.com)
* Create an account (if you don't have one allready)
* Create a new project called `ce888labs`
* make sure you are in your home folder and clone your git repo
	* `git clone <reponame>`


## IRC

* Open a seperate browser
* Login to IRC: [https://kiwiirc.com/client](https://kiwiirc.com/client)
* Use your username
* set `#ce888` for the channel name
* Type some random stuff one you are in
	



## Configuring the VM with extra packages



* Extra package installation
	* `sudo apt-get install enchant`
	

* Install NLTK 
  *  `sudo pip install sopel`
  * ```sudo pip install nltk```
  * ```sudo python -m nltk.downloader -d /usr/local/share/nltk_data punkt```
  * ```sudo python -m nltk.downloader -d /usr/local/share/nltk_data wordnet```
  * ```sudo python -m nltk.downloader -d /usr/local/share/nltk_data averaged_perceptron_tagger```


## Running a Sopel bot

* type `sopel` AND ENTER YOUR OWN NICKNAME+bot as nickname
```   I can't seem to find the configuration file, so let's generate it!

    Please answer the following questions to create your configuration file:

    Enter the nickname for your bot. [Sopel] ssamotbot
    Enter the server to connect to. [irc.dftba.net] irc.freenode.net
    Should the bot connect with SSL? (y/n) [n] y
    Enter the port to connect on. [6697]
    Enter your own IRC name (or that of the bot's owner) ssamotbot
    Enter the channels to connect to at startup, separated by commas. []
    ? #ce888
    ?
    Would you like to see if there are any modules that need configuring (y/n)? [n]
    Config file written sucessfully!
   ```

* Once you have reached this point, press ctrl+c to exit (once the bot is connected)
* Configure sopel modules to point the current directory
	* `cd .sopel`
	* `nano default.cfg`
	* add to the end `extra = .`
	* Save and exit 


## Bringing the labs from github
* Got your home directory (i.e. /home/mlvm)
* Do `git clone git@github.com:ssamot/ce888.git`
* Copy ce888/labs/lab1 into your local github lab directory
	* That would be somethine like ce888labs/lab1
	* Obviously create the directory if it doesn't exist 


## Lab Exercices
* I will tell everyone what to comment on in the IRC channel!
	* You will need to type messages from time to time as the lab progresses
* Using the emotion detector, find the average of each emotion present in the comments
	* Add the emotions for each message
	* Devide by the number of emotions by the number of messages received 
	* Also find the average of each emotion for each nick!
* Print the results everytime a new comment is entered and it contains some new emotional information
* Find the rolling average for each emotion
	* Calculate rolling average as ``ave = ave + a * (emotion -ave)``
	* Set `a = 0.01`
	* Find the average emotion for each nick as well
	


