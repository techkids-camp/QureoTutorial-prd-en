# QureoMinecraft

## Let's make the agent move!

This time we'll use the following block!

``||agent.agent destroy 〇||``

How much should we change each number?

After pressing [](https://raw.githubusercontent.com/camp-minecraft/TechkidsCampTutorial/master/images/playbutton.png) at the bottom right, press the 't' key and enter 'run' to run the program!

```template
player.onChat("run", function () {
    hiragana_agent.teleport(pos(0, 0, 0))
})

```

```ghost
player.onChat("run", function () {
    hiragana_agent.teleport(pos(0, 0, 0))
    hiragana_agent.destroy(FORWARD)
})

```