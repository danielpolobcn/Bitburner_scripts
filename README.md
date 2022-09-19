# Bitburner_scripts
## Scripts for Bitburner v2
This repository contains several scripts I developed for Bitburner v2 during my beginner days. <b>Bitburner is a funny hacking game, very useful for learning Javascript basics</b>. In order to advance through the game, players are compelled to try to automate processes and constantly improve their scripts. You can get it for free from the Github repository (https://danielyxie.github.io/bitburner) or from Steam too.<br>
All the scripts below are written for NS1 and must be saved as "name.script" in your home server.

### Inspector
This script returns information about money, security, RAM and difficulty to crack for a target server. This is convenient when you are manually looking for the proper next candidate to hack within your current hacking ability. The script relies on an argument to indicate the target server to be inspected, i.e. "run inspector.script n00dles". It is suggested to set an alias for a more convenient use (i.e. alias inspect="run inspector.script").

### Cracker
This script attempts to open as many ports as necessary and then nuke any target server, on the assumption that you are creating or buying port-opening programs from cheapest to most expensive, this is: brutessh.exe -> ftpcrack.exe -> relaysmtp.exe -> httpworm.exe -> sqlinject.exe . If you lack any of the required programs for your target server, you will get an error message indicating the missing file. It is suggested to set an alias for a more convenient use (i.e. alias crack="run cracker.script").

### Basic hack
This is the most simple script for hacking servers indefinitely. The script will check before any hacking attempt if the requisites for maximum security and minimum money are met, and run "weaken" and/or "grow" before launching further hacking attempts when necessary.

### Deployer 0
Very convenient after you install any augmentations, this script will nuke all servers with no ports to that can be accessed for your "home" server, and put them to work hacking the server with the most money among them. Just go to the university to rise your hacking level to 40 and then run this script. The <br>"basic-hack"</br> script is necessary for this to run properly.
