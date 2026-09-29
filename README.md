# Self-defining-button-module-for-FiiO-JM21
Simple magisk module that allows you to invert/swap buttons if you use old firmware which does not have such function

Options for self-defining button function was added in FW1.0.8 firmware so now you are able to swap/invert your buttons(if you use screen rotation 180 degrees) without need to update with this module

There are 3 different versions so pick whatever you prefer

Code changes "gpio-keys.kl" file

from:

key 114   VOLUME_DOWN;

key 115   VOLUME_UP;

key 163   MEDIA_NEXT;

key 164   MEDIA_PLAY_PAUSE;

key 165   MEDIA_PREVIOUS;

to:

key 114   VOLUME_UP;

key 115   VOLUME_DOWN;

key 163   MEDIA_PREVIOUS;

key 164   MEDIA_PLAY_PAUSE;

key 165   MEDIA_NEXT;

Thats it

Had to keep key 164   MEDIA_PLAY_PAUSE to make it work, if you dont include it - pause button wont work


Was tasted only with 1.0.6 firmware so before use you can ensure yourself that your button key numbers are the same:
./adb shell su -c 'cat /system/usr/keylayout/gpio-keys.kl'
or pull file
./adb shell su -c 'cat /system/usr/keylayout/gpio-keys.kl' > gpio-keys.kl


Anyway, you take all the responsibility if you use this module and use it on your own risk(either way code is watchable and you can check if its clear)
