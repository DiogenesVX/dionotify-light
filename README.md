# dionotify-light
A simple utility to get the brightness change notification.
This is a small notification utility which shows a nice notification bar when changing the brightness level.
I created it for myself to use with Sway on Debian. If someone finds it useful for his/her situation, I'd be happy :).
Of course this can run basically on any distro and desktop anvironment.

# Features
   1. Get a visual notification bar when changing the brightness level.

# Screenshot
   ![Alt text](https://github.com/DiogenesVX/dionotify-light/blob/main/dionotify-light.png)

# Usage for Sway (step-by-step for new users)
   1. Download the archive, extract it, open a terminal, navigate to the extracted folder and run:
        chmod +x dionotify-light
        mkdir -p ~/.config/sway/icons
        cp icons/* ~/.config/sway/icons
        cp dionotify-light ~/.config/sway

   2. Put the following lines into your ~/.config/sway/config
   
        bindsym --locked XF86MonBrightnessUp exec --no-startup-id 'brightnessctl -n s 3+ && ~/.config/sway/dionotify-light'
        bindsym --locked XF86MonBrightnessDown exec --no-startup-id 'brightnessctl -n s 3- && ~/.config/sway/dionotify-light'
          
  Of course you may choose a different key combination or/and location for the script, don't forget to reload the Sway configuration afterwards. 
   
   2. Make sure you have the following packages installed:
   
          grep
          coreutils
          util-linux
          libnotify-bin
          pulseaudio-utils
