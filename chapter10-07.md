### @flyoutOnly true
### @hideIteration true
### @hideIteration true
# QureoMinecraft

## エージェントをうごかしてみよう！

こんかいはつぎのブロックをつかうよ！

``||loop.もし真ならくりかえし||``

``||agent.エージェントに〇へおかせる||``

``||agent.エージェントを〇に〇ブロックいどうさせる||``

``||agent.エージェントをじぶんのいちにもどす||``

みぎしたの![](https://raw.githubusercontent.com/camp-minecraft/TechkidsCampTutorial/master/images/playbutton.png)をおしたあと、tキーをおしてgoとrunをいれてプログラムをうごかしてみよう！

```template
player.onChat("go", function () {
    while (true) {

    }
})
player.onChat("run", function () {

})
```

```ghost
player.onChat("go", function () {
    while (true) {
        hiragana_agent.move(FORWARD, 1)
        hiragana_agent.place(DOWN)
    }
})
player.onChat("run", function () {
    hiragana_agent.teleportToPlayer()
})

```