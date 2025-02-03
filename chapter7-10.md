### @flyoutOnly true
### @hideIteration true
### @hideIteration true
# QureoMinecraft

## Let's move the agent!

This time we'll use the following blocks!

``||agent.agent inspect block ◯||``
``||logic.if  ◯◯ then||``
``||logic.=||``
``||blocks.Brick Block||``


After pressing [](https://raw.githubusercontent.com/camp-minecraft/TechkidsCampTutorial/master/images/playbutton.png) at the bottom right, press the 't' key and enter 'run' to run the program!

```template
player.onChat("run", function () {
    for (let index = 0; index < 10; index++) {
        for (let index = 0; index < 10; index++) {
            hiragana_agent.move(UP, 1)
        }
        hiragana_agent.move(DOWN, 10)
        hiragana_agent.move(RIGHT, 1)
    }
})
```
```ghost
player.onChat("run", function () {
    for (let index = 0; index < 10; index++) {
        for (let index = 0; index < 10; index++) {
            hiragana_agent.move(UP, 1)
            if (hiragana_agent.inspect(AgentInspection.Block, FORWARD) == BRICKS) {
                hiragana_agent.destroy(FORWARD)
            }
        }
        hiragana_agent.move(DOWN, 10)
        hiragana_agent.move(RIGHT, 1)
    }
})
```