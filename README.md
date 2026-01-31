# 🦎 程序化壁虎动画

一个基于 HTML5 Canvas 的程序化动画壁虎，使用鼠标控制爬行方向。

![Demo](https://img.shields.io/badge/Demo-Live-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)

## ✨ 特性

- **程序化动画** - 使用链式骨骼系统模拟脊柱和四肢运动
- **FABRIK 逆运动学** - 四肢使用 FABRIK 算法实现自然的腿部动作
- **鼠标跟随** - 壁虎会平滑地跟随鼠标移动
- **吐舌动画** - 随机触发的 Y 字型粉色舌头动画
- **闲置动作** - 无输入时自动执行随机小动作（头部摆动、小距离移动）
- **输入平滑** - 过滤鼠标抖动，使动画更流畅
- **触屏支持** - 支持移动设备触摸操作

## 🎮 使用方法

直接在浏览器中打开 `gecko_clean.html` 文件即可。

- **移动鼠标** - 控制壁虎爬行方向
- **静止 2 秒** - 壁虎会开始自主做小动作

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

## 📁 文件结构

```
animated/
├── gecko.html        # 完整注释版本
├── gecko_clean.html  # 精简版本
└── README.md
```

## 🙏 致谢

灵感来源于 [argonautcode/animal-proc-anim](https://github.com/argonautcode/animal-proc-anim)

## 📄 License

MIT License
