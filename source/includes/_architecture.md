# Architecture

`AVG Engine` 总共分为两个部分。分别是 `avg.engine` 和 `avg.renderer`. 


`avg.engine` 该部分主要实现了整个游戏引擎的数据以及状态管理功能。并且所有的游戏API接口原型都在这部分进行暴露。

`avg.renderer` 是一个对 `avg.engine` 的实现部分。它依赖`avg.engine`的类型定义以及数据管理，并负责了游戏的绘图、渲染、API详细实现。游戏的前端效果都在这部分进行。

<aside class="notice">
因为两个项目的剥离，使得渲染和数据的耦合降低。也满足更高级的开发者基于avg.engine开发renderer, 定制自己的前端实现。
</aside>


## Scripting

脚本系统是引擎为游戏逻辑提供的基础API，这些API包括对话处理、流程控制、声音处理、图像处理、场景处理、变量处理、存档处理等部分。

脚本系统在运行的时候会预先从游戏的脚本目录（默认情况下位于`assets/data/scripts`）下读取入口脚本文件（默认是`start.avs`）。具体的执行流程如下：

`IO -> Transpiler -> VM -> Engine`

