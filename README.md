# Bitburner_scripts
## Scripts for Bitburner v2
This repository contains several scripts I developed for Bitburner v2 during my beginner days. <b>Bitburner is a funny hacking game, very useful to learn Javascript basics</b>. In order to advance through the game, players are compelled to try to automate processes and constantly improve their scripts. You can get it for free from the Github repository (https://danielyxie.github.io/bitburner) or from Steam too.<br>
All the scripts below are written for NS1 and must be saved as "name.script" in your home server.

### Inspector
This script returns information about money, security, RAM and difficulty to crack for a target server. This is convenient when you are manually looking for the proper next candidate to hack within your current hacking ability. The script relies on an argument to indicate the target server to be inspected, i.e. "run inspector.script n00dles". It is suggested to set an alias for a more convenient use (i.e. alias inspect="run inspector.script").

### Cracker
This script attempts to open as many ports as necessary and then nuke any target server, on the assumption that you are creating or buying port-opening programs from cheapest to most expensive, this is: brutessh.exe -> ftpcrack.exe -> relaysmtp.exe -> httpworm.exe -> sqlinject.exe . If you miss any of the required programs for your target server, you will get an error message indicating the missing file. It is suggested to set an alias for a more convenient use (i.e. alias crack="run cracker.script").
