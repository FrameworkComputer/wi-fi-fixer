# wi-fi-fixer
Linux Wi-Fi script for detecting and fixing common Intel wifi issues

## (Check back periodically for updates) 


## Detects and fixes common issues with Intel wifi on GNOME environments:

- If the wifi radio is off.
- Restarts NetworkManager (tested on Ubuntu/GNOME).
- Airplane mode.
- If modules are not loaded - detects and loads them.
- Once setup manually in the script, it will tell you if you're connected to the wrong Wi-Fi WAP.

^^ Do a Ctrl F and look for assigned_wap="Your-SSID-Here", change to your default Wi-Fi WAP in quotes, save the file - this will be [automatic in the near future](https://[sdfsd](https://github.com/ctsdownloads/wi-fi-fixer/wiki/To-Do) ^^^

## Examples

In Airplane mode:
[![asciicast](https://asciinema.org/a/557456.svg)](https://asciinema.org/a/557456)

No driver modules loaded for Intel wireless:
[![asciicast](https://asciinema.org/a/557452.svg)](https://asciinema.org/a/557452)

WiFi Connected to the wrong WAP (router):
[![asciicast](https://asciinema.org/a/557458.svg)](https://asciinema.org/a/557458)

Updated..Added Power Save Indicator (useful if unsure):
[![asciicast](https://asciinema.org/a/557462.svg)](https://asciinema.org/a/557462)


## Install and configure

1 - git clone https://github.com/ctsdownloads/wi-fi-fixer.git

2 - cd wi-fi-fixer

3 - chmod +x wifi-fixer-bash-script.sh

3 - Open wifi-fixer-bash-script.sh in a text editor, locate 
assigned_wap="Your-SSID-Here"
Change the SSID to the name of your WiFi access point. Save the file, close the text editor.


## Runn the script easily

1 - From a terminal, paste:
```
cd wi-fi-fixer/ && chmod +x wifi-fixer-bash-script.sh && sh wifi-fixer-bash-script.sh
```

2- Profit, it's all set and it does the heavy lifting for you from here.

## Troubleshooting

- Can't find NetworkManager errors? This was tested on Ubuntu GNOME. Should work on any GNOME desktop (MATE?). You can edit and replace sudo systemctl restart NetworkManager with whatever works best for your desktop environment.

- It's telling me I'm on the wrong WAP! Well, are you? If you didn't edit the file and follow step 3 above, do so.
