# Install from Pypi

```
python3 -m pip install keep_presence
```


### Run

```
keep-presence

# or

python3 -m keep_presence
```

# Install with Snap

```
sudo snap install keep-presence
```

<a href="https://snapcraft.io/keep-presence" target="_blank">
  <img alt="Get it from the Snap Store"
       src="https://snapcraft.io/static/images/badges/en/snap-store-black.svg"
       align="center"
       height="50">
</a>

### Run

```
keep-presence
```

# Manual installation

```

python3 -m pip install pynput

python3 src/keep-presence.py
```

## Optional arguments

```
-h, --help                        show this help message and exit
            
-s SECONDS, --seconds SECONDS     Define in seconds how long to wait after a user is
                                  considered idle. Default 300.

-p PIXELS, --pixels PIXELS        Set how many pixels to move. Default 1.

-c, --circular                    Move in a circle. Default move diagonally.

-m MODE, --mode MODE              Available options: keyboard, mouse, both and scroll. 
                                  

-r RANDOM RANDOM, --random RANDOM RANDOM
                                  Usage: two numbers (ex. -r 3 10). Execute actions based on a 
                                  random interval between start and stop seconds. 
                                  Note: Overwrites the seconds argument.

```

## FAQ: 

### How can I stop the program after a certain amount of time?

Linux offers the timeout command, which allows you to set a maximum runtime for any command.

Example:

```
timeout 30s keep-presence
```

### Launch on Startup:

1. GNOME: Open "Startup Applications Preferences" (search for it in Activities).
2. KDE Plasma: Search for "Startup Applications" in the Kickoff menu.
3. Click "Add" to create a new entry.
4. In the "Command" field, enter the command to run keep-presence with your desired options. Here's just an example:
5. `keep-presence --circular --seconds 180 --pixels 1`
6. Change the command to fit your needs.

**Using Systemd:**

Alternatively, you can use Systemd to manage Keep-Presence as a startup service. Refer to the official Systemd documentation for detailed instructions on how to set this up.
