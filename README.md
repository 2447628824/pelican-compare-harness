# Pelican Compare Harness

鹈鹕骑自行车 · 多 AI 编程工具对比

这个仓库用同一个「鹈鹕骑自行车」的需求，分别让四个 AI 编程工具各生成一个单文件 Three.js 场景，用来横向对比不同工具的实现效果与代码风格。每个页面都是一个独立、无构建步骤的 HTML 文件，直接用浏览器打开即可。

## 工具对照

| 目录 | 工具 | 入口文件 | 页面标题 |
| --- | --- | --- | --- |
| `ca/` | CodeArts | `pelican-bicycle.html` | 鹈鹕骑自行车 · Three.js 程序化场景 |
| `cc/` | Claude Code | `index.html` | 鹈鹕骑自行车 · Pelican Cyclist |
| `cx/` | Codex | `pelican-bicycle.html` | 鹈鹕单车 · Three.js 程序化场景 |
| `trae/` | Trae | `pelican-bicycle.html` | 鹈鹕骑自行车 · Three.js |

## 目录结构

```text
pelican-compare-harness/
├── ca/
│   └── pelican-bicycle.html
├── cc/
│   └── index.html
├── cx/
│   └── pelican-bicycle.html
└── trae/
    └── pelican-bicycle.html
```

## 使用方法

页面通过 CDN 加载 Three.js，打开时需要联网。

1. 直接双击对应的 HTML 文件，在浏览器中打开；
2. 也可以启动本地静态服务：

   ```bash
   python -m http.server 8000
   ```

   然后访问 `http://localhost:8000/ca/pelican-bicycle.html` 等路径。

所有页面都支持鼠标拖拽旋转视角、滚轮缩放（基于 OrbitControls）。

## 说明

- 四个目录来自四个工具对同一需求的独立实现，仅用于对比，不代表某个工具优于其他工具。
- 除入口 HTML 外，仓库中可能包含少量工具生成的配置文件，可忽略。
