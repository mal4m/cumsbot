# Cums Bot
**Cums Bot** is a simple JSON script for **Nightbot** for Twitch.

Randomly picks 2 phrases to stitch together, with a "cums" counter in between.
> [Phrase 1][Number][Phrase2]

For example...
> Thanks for the cum, partner! (162 cums are in the machine.)

## Installation
Access your custom Nightbot commands at [https://nightbot.tv/commands/custom](https://nightbot.tv/commands/custom)

### Command: 
```sh
!cums
```
### Message:
```sh
$(eval a="$(urlfetch json https://raw.githubusercontent.com/mal4m/cumsbot/main/cums_start)".split(";");a[Math.floor(Math.random()*a.length)])$(count)$(eval a="$(urlfetch json https://raw.githubusercontent.com/mal4m/cumsbot/main/cums_end)".split(";");a[Math.floor(Math.random()*a.length)])
```
The code essentially fetches a random line separated by a `;`, one from the `cums_start` list, then another from the `cums_end` list. <br /> Be sure to exclude the `;` from the last line to prevent empty request errors.

### Userlevel:
Set to the desired permission level for the command. The default is "Everyone", meaning anyone in the chat can use the command.

### Cooldown:
Set to however long you desire the "refractory period" to be, to avoid spamming the command in the chat.
