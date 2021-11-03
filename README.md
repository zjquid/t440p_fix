# t440p fix for windows 10
stuff to make your t440p work properly on windows 10

*works on 21H1 as of 6/12/21*

*will be testing on windows 11 soon, if you do your own testing, let me know*

# trackpad/clunkpad swap (t450 trackpad)
* get a synaptics one of these: https://imgur.com/a/z5TgiBI
* make sure its not a fake 
* install it into the laptop
* download jbg211ww.exe driver (https://drive.google.com/file/d/1xkwAOvHzVadxZ_BQ4t5xvSwNXe6Ma8do/view?usp=sharing) or google it... i think its a p53 driver?
* install the driver (dont edit any .inf files or anyhting, just clean install)
* reboot
* download and run trackpadfix.reg
* reboot
* it should work now :)
* the two-finger scrolling is reversed by default (apple's influence knows no bounds), you can change this in *Control Panel > Mouse > UltraNav > Settings > Scrolling > Switch Direction*

## disable automatic updating of drivers!!
* when windows updates it will replace this driver for the T440p driver (which is the wrong one!)
* win + r (run)
* type gpedit.msc
* navigate to *Computer Configuration > Administrative Templates > Windows Components > Windows Update*
* click "Do not include drivers with Windows Update"
* click the "Enabled" button
* apply > ok 
* it shouldn't update drivers when windows updates now.
* CAUTION this will prevent ANY driver updates, not just the trackpad. there is probably a way around this but whatever (the hardware is old enough driver updates aren't of high priority)

## add browser buttons on the T430+ keyboards (pgup + pgdown = back and forward in browser)
* download keebfix.ahk
* download autohotkey from https://www.autohotkey.com/
* right click > copy keebfix.ahk
* win + r > shell:startup
* right click > paste into startup folder
* double click keebfix.ahk or reboot to fix the keyboard

### troubleshooting
* if windows updates the driver, make sure to go to C:\Drivers and delete the UltraNav folder
* disable automatic driver updates
* then go back to step 1
* also make sure you reboot when the steps tell you to. if windows automatically updates drivers it may update them when you reboot! so disable it!
