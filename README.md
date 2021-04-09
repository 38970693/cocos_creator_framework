
# cocos creator 框架 -- kxCreator

## 3.0支持

已完成3.0版本的适配，3.0的改动巨大，但框架上层的逻辑代码需要调整的内容较少，主要是适配typescript严格的代码检查，目前所有的示例都已经通过测试，详细可查看`creator3.0`分支，该分支需要用creator3.0打开

## 资源管理重构

计划 2021-2-10 之前完成对资源管理底层的初步重构，重构有几大目标：
* 使接口兼容2.4之前和之后的cocos资源底层
* 为cc.Asset注入引用计数功能，使框架使用的体验与新资源底层保持一致
* 性能与内存占用的优化

## 写在前面

> 我对框架对一点理解，所谓框架，浅薄一点地说，只是将一些常用的代码进行封装，方便我们少写一点代码，更快地完成功能开发。但有的框架用起来舒坦，有的用起来令人令人感觉繁琐、压抑。希望这一堆代码，可以提高你的开发效率，并规避一些繁琐易错的问题。

有2个问题，是我们在平时编码的时候总是会困扰我们的问题，一个是生命周期的管理问题，一个是数据的读写问题。这两个问题决定了我们能否轻松地实现各种功能，对于生命周期管理问题，最好的方式是不用管理，让框架自动帮我们做这件事，同时也能支持让我们手动控制某些我们希望控制的地方。

## 核心框架

* 资源管理
  * ResLoader：资源的加载和卸载，支持资源依赖的识别
  * PrefabPool：Prefab的简单池子，用于优化大量重复创建的对象
* 网络框架
* UI框架
* 通用
  * EventManager: 事件机制的支持
  * TaskQueue: 任务队列的支持（确保有序地执行逻辑)
* todo: 热更新
* todo: 新手引导框架

## 示例项目

* 基础示例
  * 网络功能示例 参考 Scene/example_net 场景
  * 资源管理示例 参考 Scene/example_res 场景
  * UI示例 参考 Scene/example_ui 场景
  * ...
* 完整游戏示例

## 工具

...
