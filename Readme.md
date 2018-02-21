# WinguCloud

A python sctipt to automate Wingu

## Note from the author
I would sugest using virtual environments when working with these tools

I used [DonneMartin's Dev Setup](https://github.com/donnemartin/dev-setup) chain to prepare my mac

##Using this repo

```
> brew install python3
> mkvirtualenv wingu-cloud --python=python3

> mkdir -p ~/projects/wingu/cloud
> cd ~/projects/wingu/cloud
> git clone https://github.com/TachyonicProject/wingu-demo .

> workon wingu-cloud
> pip install -r requirements.txt
```

 
##Check your settings
### Check the basics
Open `config.py` in your favourite editor and ensure you put the correct values in the fields provied
The important ones to note are:

```
USERNAME = "your.wingu.login@email.address"
PASSWORD = "YourSuperSecretPasswordForWingu"
PROJECT_ID = "This is your project workspace id - available from the Winu User Interface"
HEAT_URL = "https://orchestration.wingu.co.za:8004/v1/${PROJECT_ID}"
```

###One More Check:

In `start.py` - Make sure the template_url exists, and is pointing to the right file - the default one spins up a django webserver

## Start you Engines
Wanna get going?

```
> workon wingu-cloud
> python start.py
```

Enjoy some coffee / tea / whiskey while the automation does it's magic.

You can track the progress through the web interface.

## Destination reached
Had enough, and want to clean up?

```
> workon wingu-cloud
> python stop.py
```
