# 🌍 Three-Earth · 全球环境态势感知平台

[![Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js&logoColor=white)](https://threejs.org/)
[![License](https://img.shields.io/badge/License-Copyright-red.svg)](#-声明与版权)
[![Competition](https://img.shields.io/badge/Competition-第19届中国大学生计算机设计大赛-blue.svg)]()

> **Three.js-based 3D Global Environmental Situational Awareness Platform**

> **基于 Three.js 的 3D 全球环境态势感知平台**

这是一个**纯前端信息聚合项目**，综合展示了地震（USGS）、山火（NASA FIRMS）、空气质量（WAQI）、全球新闻等多种 API 接口数据，并将它们映射到 3D 地球上，旨在为环境预警与治理贡献力量。

---

## 🖼️ 项目预览

 <img width="2559" height="1436" alt="2026026546作品素材图01" src="https://github.com/user-attachments/assets/6c384aef-c771-4b0e-8bce-a92adf9da6d5" />
  <img width="2559" height="1436" alt="2026026546作品素材图02" src="https://github.com/user-attachments/assets/63a80bb5-2a1f-4af8-ad9e-b656adba0553" />
<p align="center">
 <img width="2559" height="1436" alt="2026026546作品素材图03" src="https://github.com/user-attachments/assets/216579e0-a9de-48df-974d-fc5744380f0f" />
</p>

## ✨ 核心特性 (Features)

- 🌐 **3D 全球可视化**：基于 Three.js 与 WebGL，渲染带云层、光照、星空的高精度 3D 地球。
- 🛰️ **多源 API 聚合**：纯前端接入 USGS 地震、NASA FIRMS 山火、WAQI 空气质量等实时数据。
- 📊 **态势图层切换**：支持地震、山火、空气质量图层的独立开关与图例显示。
- 🎯 **智能背向剔除**：基于相机与地球中心向量点积，自动隐藏地球背面标记，提升视觉清晰度。
- 📰 **新闻标签筛选**：支持按气候、地震、能源、公共卫生、经济、科技等标签分类查看。
- ⏱️ **自动刷新**：数据每 5 分钟自动刷新，实时同步全球态势。

## 🛠️ 技术栈 (Tech Stack)

- **3D 渲染**: [Three.js r128](https://threejs.org/)（通过 CDN / importmap 引入）
- **开发语言**: 原生 JavaScript (ES6 Module) + HTML5 + CSS3
- **地图交互**: OrbitControls（轨道控制器）
- **标签渲染**: CSS2DRenderer
- **数据源**: USGS（地震）· NASA FIRMS（山火）· WAQI（空气质量）· 新闻数据池
- **架构**: 单文件纯前端，无需构建工具，开箱即用

## 🚀 快速开始 (Quick Start)

本项目为**单 HTML 文件**，无需安装依赖，无需构建。

### 方式一：直接打开
1. 下载 `Three earth.html` 文件到本地。
2. 用支持 ES6 Module 的现代浏览器（Chrome / Edge / Firefox）直接打开即可。
   > ⚠️ 注意：由于使用了 `type="module"` 和 CDN importmap，建议通过本地服务器打开，否则部分浏览器可能因 CORS 限制导致模块加载失败。

### 方式二：通过本地服务器运行（推荐）
```bash
# 如果你安装了 Python
python -m http.server 8000

# 或者用 VSCode 的 Live Server 插件
# 右键 Three earth.html → Open with Live Server
```
然后访问 `http://localhost:8000/Three%20earth.html`。

## 📂 项目结构 (Project Structure)

```text
.
├── images/             # 存放 README 预览图的文件夹
│   ├── 1.png
│   ├── 2.png
│   └── 3.png
├── Three earth.html    # 项目唯一入口（包含全部 HTML / CSS / JS）
└── README.md           # 项目说明文档
```

## 🔌 数据接口说明 (API Sources)

| 数据源 | 用途 | 接口地址 |
| :--- | :--- | :--- |
| USGS | 全球 2.5 级以上地震 | `earthquake.usgs.gov/.../2.5_day.geojson` |
| NASA FIRMS | 全球山火热点 | `firms.modaps.eosdis.nasa.gov/api/...` |
| WAQI | 城市空气质量 | 本地模拟数据（演示用途） |
| 新闻池 | 全球环境/经济/科技新闻 | 内置模拟数据（演示用途） |

> 💡 山火与新闻数据在 API 不可用时会自动降级为内置模拟数据，保证演示效果。

## 🎮 操作说明 (Controls)

- **拖动鼠标**：旋转地球
- **滚轮**：缩放视角
- **点击彩色标记**：查看地震 / 山火 / 空气质量 / 新闻详情
- **左侧按钮**：切换地震、山火、空气质量图层
- **右侧面板**：实时监控数据列表，可收起/展开
- **图例按钮**：显示/隐藏底部图例

---
 **🚀 在线体验：[点击这里访问 3D 地球在线演示](https://moonlight0030.github.io/Three-Earth-Global-Environmental-Situational-Awareness-Platform/Three%20earth.html)**

---

## ⚠️ 声明与版权 (Disclaimer & Copyright)

**Disclaimer:** This work is my entry for the 19th China Collegiate Computing Competition (China University Student Computer Design Competition). The copyright and interpretation rights belong to me. Please indicate the source for secondary development. Unauthorized use is prohibited.

**声明：**
**此作品为本人参加第 19 届中国大学生计算机设计大赛作品，版权和解释权归本人所有。二次开发请标明出处，禁止盗用、倒卖或用于其他同类比赛。**

---
<p align="center">
  <i>如果觉得这个项目不错，欢迎点个 ⭐ Star 支持一下！</i>
</p>
