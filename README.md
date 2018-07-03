# tetris

俄罗斯方块局域网对战版。

启动方式使用 --help。

图片改自达内教材资源。



Licensing
=========
common is licensed under the Apache License, Version 2.0. See
[LICENSE](https://github.com/binave/tetris/blob/master/LICENSE) for the full
license text.


```
usage: java -jar [jar_path] [option]
```

> 使用参数 (option)：

>     --help,   -h
>         显示此帮助信息。
>
>     --single, -1
>         经典玩法。
>         使用方向键控制方块。
>         方向键 “上” 用于方块翻转，“空格” 为一落到底。
>         “P” 暂停。
>
>     --dual,   -2
>         同屏双人玩法。
>         主机玩家由“WDSA” 控制方块的移动和翻转，“Q” 消耗 SP 更换方块，
>         副机玩家使用方向键控制方块，“/” 消耗 SP 更换方块，
>         “空格” 暂停，“ESC” 退出游戏。
>
>     双人玩法不再是获得分数，而是通过给对手增加麻烦来搞死对方为获胜条件。
>
>     --online-server,  -a
>         局域网双人玩法，主机。
>         需要先启动，等待副机启动连接后，使用 “P” 开始，游戏中用 “P” 暂停。
>         操作方法与 “经典玩法” 相同，“左 SHIFT” 消耗 SP 更换方块。
>         获胜条件与双人玩法一致。
>
>     --online-client,  -b    [ipv4]
>         局域网双人玩法，副机。
>         需要输入主机的 ip 启动。
>         操作方法与 “经典玩法” 相同，“左 SHIFT”消耗 SP 更换方块。
>         获胜条件与双人玩法一致。


* 关于双人玩法规则：
    * 去一行，除了减行，什么效果都没有。
    * 去两行，奖励 SP 点。
    * 去三行，除了奖励 SP 点，还会把第四行转移给对手。
    * 去四行，除了奖励 SP 点，还会加速对手方块的下落。
    * “左 SHIFT” 消耗 SP 更换方块，副作用可以用来抵消加速下落。
    * 所以观察对少的状态很有必要。
    * SP 点存在存储上限，也不会继承到下一局，建议多多使用。