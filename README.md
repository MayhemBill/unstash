# unstash

I did this purely to spite V, I wouldn't recommend using it unless you know what you're doing :D -Bill

Requires OpenSSH installed as well as safestrat (in-case of emergency)
NOTE: These are not depends as this can also be run in Terminal but OpenSSH used when no homescreen icons are shown.

This is a BASH script file designed to restore basic functionality to homescreen when you use Cydia to stash on semi-untethered builds 
(Only 9.3.3 is affected currently)

A quick breakdown of what goes on in the script:

The script checks for any previous stashing procedures have been completed. Coolstars, StashMyApps9, and Cydia are the three check currently.
After all checks pass (meaning no stashing besides Cydia) the script will begin to return /Applications to it's original state.

First step is to create a backup of Applications called stash_bck.tar.bz2 and then store it in /var/mobile/Downloads.
Second step is it'll break the symlink from stash to /Applications, and then move the Applications folder back to /Applications.
Third step is to attempt to push the proper permissions back onto any broken application folders. (This doesn't use chmod, as this carries over when moved. Uses chown)
Once complete, uicache is killed and then an automatic respring initializes. Unlocking should show the homescreen again.

Any support or comments regarding this can go directly to team_vec1phyr@yahoo.com

NOTE: This tool is entirely for my self-education, the code is only public for feedback and if anyone would like to improve it or test it out themselves in a sense of
stability post-run.

If you have no idea how to run shell-scripts. Please do not use this tool. Thanks
~V
