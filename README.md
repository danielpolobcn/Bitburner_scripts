# Bitburner_scripts
## Scripts for Bitburner v2
This repository contains several scripts I developed for Bitburner v2 during my beginner days. <b>Bitburner is a compelling hacking game, very useful for learning Javascript basics</b>. In order to advance through the game, the players are required to try to automate processes and constantly improve their scripts. You can get it for free from the [Github repository](https://danielyxie.github.io/bitburner) or from Steam too.<br>
The scripts below are written for NS2 and must be saved as "name.js" in your home server.

### Inspector
This script returns information about money, security, RAM and difficulty to crack for a target server. This is convenient when you are manually looking for the proper next candidate to hack within your current hacking ability. The script relies on an argument to indicate the target server to be inspected, i.e. "run inspector.js n00dles". It is suggested to set an alias for a more convenient use (i.e. alias inspect="run inspector.js").

### Cracker
This script attempts to open as many ports as necessary and then nuke any target server, on the assumption that you are creating or buying port-opening programs from cheapest to most expensive, this is: brutessh.exe -> ftpcrack.exe -> relaysmtp.exe -> httpworm.exe -> sqlinject.exe . If you lack any of the required programs for your target server, you will get an error message indicating the missing file. It is suggested to set an alias for a more convenient use (i.e. alias crack="run cracker.js").

### Basic hack
This is the most simple script for hacking servers indefinitely. The script will check before any hacking attempt if the requisites for maximum security and minimum money are met, and run "weaken" and/or "grow" before launching further hacking attempts when necessary.

### Split hack
Instead of executing the weaken / grow / hack cycle itself, this script runs as many threads as possible of one-shot scripts which require less RAM than every thread of the basic-hack script (1.75 Gb instead of 2.4 Gb). This will grant more threads attacking the target when the executing server has 32 Gb or more RAM. The one-shot scripts only require one line of code (i.e. await ns.weaken(ns.args[0]);) and will be copied automatically from your home server to the executing server. All the available RAM in the executing server will be allocated for this attack, therefore you may not want to launch this script from your home server without changing this script first to preserve some minimum free RAM to run other scripts.

### Deployer
This is a script to be called recurrently as your hacking abilities keep growing. Regardless of your skill and owned programs at any time, the script builds a list of suitable new servers within your reach, cracks them and puts them to work hacking themselves. For this purpose, the split-hack script will be called when possible (the executing server having 32+ Gb of RAM), otherwise the basic-hack is summoned. You are also warned when the new server has no RAM or no money to siphon. <b>Dependencies: Cracker, Basic-hack, Split-hack.</b>
