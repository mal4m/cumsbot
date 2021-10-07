Cums Bot is a simple JSON program for Nightbot for Twitch.

Randomly picks 2 phrases to stitch together, with a "cums" counter in between.

Access your custom Nightbot commands at [https://nightbot.tv/commands/custom](https://nightbot.tv/commands/custom)

Command: 
```sh
!cums
```
Message:
```sh
$(eval a="$(urlfetch json https://raw.githubusercontent.com/mal4m/cumsbot/main/cums_start)".split(";");a[Math.floor(Math.random()*a.length)])$(count)$(eval a="$(urlfetch json https://raw.githubusercontent.com/mal4m/cumsbot/main/cums_end)".split(";");a[Math.floor(Math.random()*a.length)])
```

Code essentially fetches a random line separated by a `;`. Be sure to exclude the `;` from the last line to prevent empty request errors.
