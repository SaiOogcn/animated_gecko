# 🦎 程序化壁虎动画

一个基于 HTML5 Canvas 的程序化动画壁虎，使用鼠标控制爬行方向。

![Demo](https://img.shields.io/badge/Demo-Live-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)

## ✨ 特性

- **程序化动画** - 使用链式骨骼系统模拟脊柱和四肢运动
- **FABRIK 逆运动学** - 四肢使用 FABRIK 算法实现自然的腿部动作
- **多种输入模式** - 鼠标、触摸、手部追踪
- **输入平滑** - 双层平滑过滤输入抖动，使跟随更自然

## 🎮 使用方法

在浏览器中打开下面的 HTML 文件之一：

- `gecko_clean.html` — 精简演示，由鼠标/触摸控制
- `gecko_handtrack.html` — 使用 MediaPipe Hands 进行手部追踪，MediaPipe Face Mesh 进行面部识别
- `gecko_hand&tougetrack.html` — 把眨眼控制吐舌换成了吐舌控制吐舌，let's do some real things（我知道我的tongue拼错了）
- `gecko_eatbug.html` — 无聊就来吃点虫子吧，我画的可能还没那么恶心

操作说明：

- **移动鼠标 / 手指** — 控制壁虎移动
- **靠近小虫** — 壁虎会尝试捕食
- **眨眼（需要摄像头）** — 触发吐舌头动作（需要允许网页获取摄像头权限）

## 🔧 技术实现

### 骨骼系统
- **脊柱**: 14 节链式骨骼，带角度约束
- **四肢**: 每条腿 3 节骨骼，使用 FABRIK 解算

### 动画参数
| 参数 | 值 | 说明 |
|------|-----|------|
| `SMOOTH_FACTOR` | 0.15 | 输入平滑系数 |
| `DEAD_ZONE` | 3px | 输入死区 |
| `IDLE_THRESHOLD` | 2s | 闲置触发时间 |

### 视觉特征
- 淡绿色身体 (`#8BC48A`)
- 白色眼睛，位于头部两侧
- 胶囊形脚趾
- 淡粉色分叉舌头 (`#FFB6C1`)
- 身体斑点装饰

## 📁 文件结构（概览）

```
animated/
├── gecko.html            # 完整注释版本
├── gecko_clean.html      # 精简版本
├── gecko_handtrack.html  # 手部追踪 + 眨眼吐舌（MediaPipe）
├── gecko_eatbug.html     # 吃虫子演示（小虫生成、捕食逻辑）
├── rl_gecko/             # 强化学习环境与训练脚本（见下文）
└── README.md
```

## 🙏 致谢

灵感来源于 [argonautcode/animal-proc-anim](https://github.com/argonautcode/animal-proc-anim)

## 📄 License

MIT License
