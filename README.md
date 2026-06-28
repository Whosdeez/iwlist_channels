# A hasty CLI bash script to display the Wi-Fi activity around you
I made this bash script on an ADHD spree because I missed the Android [WiFi Analyzer](https://olgor.com) app on Linux.

### What the script does
`sudo iw dev wlan0 scan` and greps the few lines that I was interested in. \
Because not everyone's Wi-Fi adapter is called `wlan0`, everything but the last line is dedicated to evaluate the correct interface name `iface`.

That's it!

**Language**: bash \
**Current iw version**: 6.17 \
**How to use**: copy the snippet to your `.bashrc`, save it then execute `source ~/.bashrc` and invoke `iwlist_channels` as if it were an alias. \
**Requirements**: `iw` installed, and `sudo` privileges.

### Disclaimer
The display is not formatted, based off of sloppy [grep](https://linux.die.net/man/1/grep)'s, and might break if the underlying [iw](https://linux.die.net/man/8/iw) changes its outputs. \
I will not maintain this script, so feel free to fork, copy, adapt and get inspiration from it.
