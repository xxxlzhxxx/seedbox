# SeedBox · 种子盒

一个用来搭建可交互世界、让角色在里面行动的开源项目。

## 第一个例子

原创广场上有喷泉、长椅和一间书店。角色读取场景里的路网，从入口出发，经过喷泉走到书店。这个命令行例子展示场景作者和角色开发者如何协作。

把同一 GitHub 账号或组织下的 seedbox-worlds 和 seedbox-agents 克隆到同一目录，在该目录运行（Python 3.8+）：

```sh
python3 seedbox-agents/walk.py seedbox-worlds/plaza.json entrance bookshop
```

预期输出为 `入口 → 喷泉 → 书店`。

## 仓库导航

| 仓库 | 内容 | 适合谁贡献 |
| --- | --- | --- |
| [seedbox-worlds](../../../seedbox-worlds) | 场景文件、地点与路网格式、示例广场 | 场景作者 |
| [seedbox-agents](../../../seedbox-agents) | 读取场景和执行角色移动的参考实现 | Agent 与游戏开发者 |

## 参与

新增场景可以从 plaza.json 复制一份，给地点取稳定的 ID，列出可步行的连接，再用 walk.py 验证入口到目的地的路线。修改场景格式时，请在 PR 里附一个场景和预期输出，方便两个仓库一起验证。

后续方向包括 glTF 场景预览、浏览器角色控制和模型工具调用。当前首版实现地点之间的命令行寻路。

代码与示例使用 MIT 许可证。
