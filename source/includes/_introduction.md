
# Introduction

欢迎使用AVG Engine文档。AVG Engine是一个跨平台、灵活、门槛低的文字游戏引擎。引擎拥有超多开放的游戏API，使游戏作者可以很轻易从零到一开发文字游戏。你可以用来制作有声小说，甚至可以基于更高级的插件机制开发定制化的游戏特性。

AVG Engine的脚本又被成为AVScript, 是一门基于JavaScript的脚本语言。如果你有JavaScript基础，那么将很容易入门。即使你从来没有接触过编程语言，AVScript对于你而言也十分基础，简单易上手。

> 一段简单的游戏脚本 `start.avs`:

```javascript
// 加载一个场景
api.loadScene('assets/graphics/backgrounds/background.png');

// 播放背景音乐
api.playSound('assets/audio/bgm/title.mp3');

// 显示对话
api.showText('我能吞下玻璃而不伤身体');

// 显示对话并定义说话角色
api.showText('我觉得非常不错。', {
    speaker: {
        name: '小绮',
        avatar: 'assets/graphics/characters/char-1.png'
    }
});

// 隐藏对话框
api.hideText();
```
