<div align="center">

<a href="#start">
  <img src="./docs/assets/carry-design-cover.svg" alt="Carry Design：Lens 透镜、Lattice 点阵、Overture 序曲，三套原生 Web 设计系统" width="100%" />
</a>

<br />

<sub>CARRY DESIGN · NATIVE WEB DESIGN SYSTEMS</sub>

<h1>给界面，一套自己的物理法则。</h1>

<p><strong>玻璃会折射。粒子会汇聚。光圈会开合。</strong></p>

<p>三套从零构建的原生 Web 设计系统。<br />
让材质有质感，让动作有逻辑，让每一次交互都值得感受。</p>

<p>
  <a href="#start">开始体验</a>
  &nbsp; · &nbsp;
  <a href="#systems">探索三套系统</a>
  &nbsp; · &nbsp;
  <a href="#architecture">了解架构</a>
  &nbsp; · &nbsp;
  <a href="#development">开发与构建</a>
</p>

<a href="./LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-1c1d22?style=flat-square" /></a>
<img alt="Native Web: HTML CSS JavaScript" src="https://img.shields.io/badge/Native_Web-HTML_%2F_CSS_%2F_JS-1c1d22?style=flat-square" />
<img alt="Graphics: WebGL2 and WebGPU" src="https://img.shields.io/badge/Graphics-WebGL2_%2F_WebGPU-1c1d22?style=flat-square" />

</div>

---

<a id="systems"></a>
## 三个世界，各有一套章法。

在 **Lens** 中，光决定材质的样子。  
在 **Lattice** 中，点决定世界的形状。  
在 **Overture** 中，镜头决定故事如何展开。

它们共享原生 Web 这一块画布，却拥有各自完整的视觉语法、组件系统、交互规则和交付方式。

|  | **01 · Lens / 透镜** | **02 · Lattice / 点阵** | **03 · Overture / 序曲** |
| :--- | :--- | :--- | :--- |
| **灵感** | 玻璃 · 液体 · 光 | 点 · 集 · 映射 | 摄影 · 歌剧 · 时装 |
| **核心体验** | 真实折射、弹性触感、光学反馈 | GPU 粒子形变、依赖瀑布、证明生长 | 光圈开幕、相纸显影、织物共振 |
| **组件** | 18 类公共组件 + 4 组数据展示 | 14 张可交互组件卡 | 46 个组件，7 个家族 |
| **图形** | WebGL2 · Canvas · CSS | three.js · WebGL2 | WebGPU → WebGL2 → 静态呈现 |
| **交付** | 独立 ESM 包与单文件展示 | ES modules 与单文件展示 | 原生运行时、品牌工坊与单文件展示 |
| **深入了解** | [Lens 使用指南](lens/START-HERE.md) | [Lattice 使用指南](lattice/README.md) | [Overture 使用指南](overture/README.md) |

<a id="start"></a>
## 先看一眼。再亲手试试。

体验这样一套设计，最好直接打开它。

### 01 · 启动完整展示

```bash
git clone https://github.com/carry-yu-0239/carry-design.git
cd carry-design
node serve.mjs
```

然后在浏览器中打开 **http://127.0.0.1:4300/**。

只需 Node.js 和现代浏览器。根目录的 `serve.mjs` 是一个原生 Node.js 静态服务器，无须在根目录安装依赖；也可执行 `node serve.mjs 8080` 改用其他端口。

### 02 · 直达你喜欢的世界

| 体验 | 本地地址 / 文件 | 特点 |
| :--- | :--- | :--- |
| **一次曝光 · 总览** | [`index.html`](index.html) · [本地打开](http://127.0.0.1:4300/) | 一次连贯游览三个世界 |
| **Lens · 完整展示** | [`lens/lens-showcase-standalone.html`](lens/lens-showcase-standalone.html) | 单文件；完整光学控件、图表、实验室与声音 |
| **Lens · 材质实验室** | [`lens/lens.html`](lens/lens.html) | 现场调节折射、雾化、色散和弹性 |
| **Lattice · GPU 演示** | [`lattice/dist/lattice-showcase.html`](lattice/dist/lattice-showcase.html) | 单文件；实时粒子、定理之瀑、证明树 |
| **Lattice · 组件目录** | [`lattice/dist/catalog/index.html`](lattice/dist/catalog/index.html) | 14 张可交互组件卡与设计变量 |
| **Overture · 完整展示** | [`overture/dist/overture-showcase.html`](overture/dist/overture-showcase.html) | 单文件；影像、动效、字体与视频一并内嵌 |
| **Overture · 设计目录** | [`overture/dist/catalog/index.html`](overture/dist/catalog/index.html) | 46 个组件、九段现场演示、设计规范 |
| **Overture · 品牌工坊** | [`overture/dist/studio.html`](overture/dist/studio.html) | 编辑品牌画面，导出 PNG / WebM |

这些仓库链接便于查看文件；**可交互体验请使用本地服务器地址**，例如将文件路径接在 `http://127.0.0.1:4300/` 后。三份完整单文件 HTML 也可独立保存并直接打开，其中 Lattice 的 Google Fonts 会在离线时回退到系统字体。

<div align="center">

*向下滚动，场景随之改变。鼠标、触摸、键盘，每一种输入都有自己的回应。*

</div>

---

<a id="lens"></a>
## 01 / Lens · 透镜

### 玻璃，终于像玻璃。

一块玻璃，应该改变光的方向。  
一次触碰，应该让材质有所回应。

Lens 将**玻璃、液体、光**组织为统一的交互语言。背景进入纹理，折射由 WebGL2 实时计算；玻璃随着拖动拉伸、回弹，亮边与光泽也跟着改变。文字与输入仍由原生 DOM 承担，清楚、可选中、可使用键盘。

**你能感受到：**

- **真实光学**：圆角有符号距离场（SDF）、近似 Snell 折射、RGB 色散、雾化采样与 Fresnel 边缘光；多层玻璃可逐层合成。
- **弹性动作**：指针捕获、方向性拉伸、阻尼回弹；滑杆、开关、拖放选择和透镜共享物理反馈。
- **有分寸的声音**：13 种原创合成短音效，外加随拖动速度变化的连续摩擦音；默认静音，由用户主动开启。
- **原生交互**：语义化按钮、键盘导航、焦点状态与减弱动态设置；WebGL2 不可用时使用 CSS 材质。
- **随手调整的材质实验室**：Thick / Clear / Soft 三种预设，以及折射、模糊、色散、弹性和场景选项。

<details>
<summary><strong>展开：18 类组件与 4 个数据展示组合</strong></summary>

<br />

| 组件分组 | 可使用的组件 |
| :--- | :--- |
| 操作与导航 | `button`、`icon-button`、`toggle-tile`、`tabs`、`dock`、`menu` |
| 输入与选择 | `switch`、`choices`、`slider`、`stepper`、`search` |
| 容器与反馈 | `panel`、`lens`、`card-list`、`notification` |
| 光学交互 | `progress`、`drop-select`、`xy-slider` |

数据展示包括 **line-chart、bar-chart、ring-chart、records-table**。四个示例由 `mountShowcaseCharts()` 统一挂载、共享数据和过滤状态；它们不属于独立的 `createComponent()` 工厂。

[查看组件清单](lens/lab/design-system/COMPONENTS.md) · [交互规范](lens/lab/design-system/INTERACTIONS.md) · [完整 API](lens/lab/design-system/README.md)

</details>

### 把透镜带到你的页面。

Lens 的可复用实现位于 [`lens/lab/design-system/`](lens/lab/design-system/)。这是一个有 TypeScript 声明、无运行时依赖的原生 ESM 包，可以直接复制进静态网站。

```html
<link rel="stylesheet" href="./design-system/tokens.css">
<link rel="stylesheet" href="./design-system/components.css">

<div id="stage" style="min-height: 280px; padding: 32px"></div>

<script type="module">
  import {
    createComponent,
    createGlassSystem
  } from "./design-system/index.js";

  const stage = document.querySelector("#stage");
  const button = createComponent("button", {
    label: "触碰光",
    onPress: () => console.log("Hello, Lens.")
  });

  stage.append(button.element);

  const system = createGlassSystem(stage, {
    material: "thick",
    scene: "aurora"
  });

  // 页面卸载时：
  // system.destroy();
  // button.destroy();
</script>
```

`createComponent()` 负责可访问控件，`createGlassSystem()` 将光学渲染、物理手势与声音接入同一舞台。运行时通过 `setMaterial()`、`setScene()` 和 `jelly.setIntensity()` 调节体验。

**继续探索**　[完整展示](lens/lens-showcase-standalone.html) · [设计规则](lens/lab/design-system/SCOPE.md) · [TypeScript API](lens/lab/design-system/index.d.ts)

---

<a id="lattice"></a>
## 02 / Lattice · 点阵

### 万千粒子，自成章法。

一个点，可以是一颗星。  
无数个点，可以是一段文字、一座模型、一条证明。

Lattice 让页面里的文字、图形与结构拥有同一种构成方式：**点集**。输入、滚动和拖动，让一个点集自然映射到另一个点集。它的画面由 GPU 实时计算，3D 旋转、粒子运动与相机运镜都在同一个空间里发生。

**一套点阵，可以做很多事：**

- **Field · 点场**：桌面最多 65,536 个模拟点，移动端 25,600 个。粒子经弹簧归位，穿过 ABC 流，再重组为新的点集；指针能够推开、搅动或“融化”它们。
- **Sets · 点集**：5×7 点阵字、洛伦兹吸引子、三叶结、晶体、克莱因瓶、斐波那契球等，都是可切换的构形。
- **Cascade · 定理之瀑**：将有向无环依赖图化成向下流淌的证明链；悬停高亮前提与推论，点击继续生长证明。
- **ProofTree · 证明树**：结论作为根，前提与公理逐层伸展；切换定理时，整棵树随之转场。
- **Stage · 舞台**：一张 WebGL 画布、一组相机站点、滚动驱动的镜头语言，以及按需运行的渲染循环。

展示内容包含 **43 条实分析结果的依赖关系**。你也可以换成课程知识树、项目依赖图或任何自定义 DAG。

### 从一组点，开始。

核心 ES module 入口是 [`lattice/src/index.js`](lattice/src/index.js)；`Stage`、`Field`、`Cascade`、`ProofTree`、点集生成器和 DOM 控件均从这里导出。源码依赖 three.js，构建后的展示页已将其打包。

```js
import { Stage, Field, sets, WORLDS } from "./lattice/src/index.js";

const stage = new Stage(canvas, [
  {
    id: "hero",
    el: ".hero",
    pos: [0, 0, 10],
    look: [0, 0, 0]
  }
], WORLDS.night);

const field = new Field(stage);
field.useSets(sets);

stage.add(field);
field.onResize(stage);

field.keep(
  (L) => L.shape(sets.lorenz(field.N, 2)),
  { is3d: true, alpha: 0.22 }
);
```

这一示例用于已有 canvas、`.hero` 容器，并通过构建工具或 import map 解析 three.js 模块的工程。需要完整页面挂载与资源管理时，可直接参照 [展示源码](lattice/showcase/main.js)。

点阵的 DOM 控件保留原生输入与焦点：按钮、滑块、开关、标签页、加载器、文字、命令面板等，共有 **14 张组件目录卡**。音效由 Web Audio 合成，默认关闭。`?record` 模式可使用确定性时间推进，便于逐帧捕获动画。

**继续探索**　[单文件演示](lattice/dist/lattice-showcase.html) · [组件目录](lattice/dist/catalog/index.html) · [系统设计](lattice/DESIGN.md) · [实现与验证](lattice/VERIFICATION.md)

---

<a id="overture"></a>
## 03 / Overture · 序曲

### 好戏，从一次开合开始。

光圈打开，画面登场。  
影像显现，故事展开。  
松开指尖，余韵还在。

Overture 从摄影、歌剧和时装出发，把**开幕、显影、共振**发展为一套完整的网页与品牌设计语言。它既能呈现大场面的光影，也能照顾一个按钮按下的瞬间。

### 三种动作，贯穿整套系统。

| 动作语法 | 运动原语 | 在哪里发生 |
| :--- | :--- | :--- |
| **开幕 · Aperture** | `Overture.motion.iris()` | 光圈开合、浮层登场、主题切换、快门反馈 |
| **显影 · Develop** | `develop()` · `flip()` · `count()` | 影像揭示、数字变化、列表重排与相纸切换 |
| **共振 · Spring** | `Overture.motion.spring()` | 拖动回弹、胶片收放、相纸摆动与丝绸余振 |

五种弹簧预设——`snap`、`settle`、`stage`、`resonance`、`swing`——在不同尺寸与交互中维持连续的运动质感。八种合成交互声可按需开启。

### 从舞台，到暗房，再到品牌。

- **46 个组件，7 个家族**：导航与动作、表单与选择、浮层与披露、反馈与进度、内容与数据、影像与 GPU、品牌与版式。
- **三套主题**：Stage（暗场）、Paper（印纸）、Nocturne（夜场）；可在同一页面内切换。
- **两种光温**：暖光用于照亮内容；冷光用于聚焦与取景。朱红标记选择与关键动作。
- **影像组件**：追光照片墙、显影图像、胶卷暗盒、对比透镜、丝绸曲面与 GPU 光圈舞台。
- **品牌工坊**：使用现成的版式和影像工具组合画面，支持 PNG / WebM 导出。
- **完整离线展示**：独立 HTML 内嵌 CSS、JavaScript、字体、图片、three.js 和 720p 宣传片。

<details>
<summary><strong>展开：46 个组件的完整分类</strong></summary>

<br />

| 家族 | 数量 | 组件 |
| :--- | :---: | :--- |
| 动作与导航 | 8 | CueButton、IconButton、TextLink、StageTabs、ChapterNav、Breadcrumb、Pagination、CommandPalette |
| 表单与选择 | 10 | TextField、TextArea、Select、ChoiceGroup、Check、Switch、Range、Stepper、TagInput、Dropzone |
| 浮层与披露 | 5 | Accordion、Dialog、Drawer、Tooltip、Popover |
| 反馈与进度 | 5 | Toast、Notice、Progress、Loading、EmptyState |
| 内容与数据 | 2 | EditorialTable、Timeline |
| 影像与 GPU | 10 | ApertureStage、ContactSheet、FlashlightFocus、PinnedPhotoWall、FilmCanister、DevelopImage、FocusGallery、CompareLens、SilkResonance、CuePlayer |
| 品牌与版式 | 6 | Wordmark、TypeSpecimen、PullQuote、Poster、BrandComposer、CurtainTransition |

组件来源：[`overture/src/catalog-data.mjs`](overture/src/catalog-data.mjs)。

</details>

### 一行挂载，精彩就位。

将 [`overture/dist/`](overture/dist/) 中的 `overture.css`、`overture.js` 和 `assets/` 复制到你的站点，即可通过原生 JavaScript 挂载组件。

```html
<link rel="stylesheet" href="./overture.css">
<script src="./overture.js"></script>

<div id="exposure"></div>

<script>
  Overture.configure({ assetBase: "./assets/" });

  const range = Overture.mount("Range", "#exposure", {
    label: "曝光",
    value: 70,
    onChange: ({ value }) => console.log(value)
  });

  // 组件卸载时：
  // range.destroy();
</script>
```

GPU 图形优先尝试 WebGPU，再回退至 WebGL2；常规内容与控件保留静态呈现能力。详见 [公开 API 与集成规范](overture/project/guidelines/30-api.md)。

**继续探索**　[单文件演示](overture/dist/overture-showcase.html) · [光影实验](overture/dist/light-studies.html) · [品牌工坊](overture/dist/studio.html) · [动效规格](overture/MOTION-SPEC.md)

---

<a id="architecture"></a>
## 细节之下，自有秩序。

三套设计系统的实现彼此独立。每一套都有自己的组件、变量、渲染机制和构建流程；总览站点则负责把它们串成一次连续的体验。

```text
carry-design/
│
├── index.html                 # 「一次曝光」总览与场景导航
├── exposure/                  # 三套体系的首屏、集成展示与加载动效
│   ├── page.js                # 展示页与总览站点之间的生命周期通信
│   └── loaders.js             # Lens / Lattice / Overture 专属加载动画
│
├── lens/                      # 01 · 光学材质与弹性交互
│   ├── lens-showcase-standalone.html
│   └── lab/
│       ├── design-system/     # ESM 包、18 类组件、token、类型与示例
│       │   ├── index.js       # 对外入口
│       │   ├── runtime.js     # 渲染、手势、声音统一挂载
│       │   ├── internal/      # WebGL 渲染与物理实现
│       │   └── examples/
│       └── tests/
│
├── lattice/                   # 02 · 点集、数学结构与 GPU 舞台
│   ├── src/
│   │   ├── gl/               # Field / Sets / Cascade / ProofTree / Stage
│   │   ├── dom/              # 语义化点阵控件
│   │   ├── core/             # 时钟、弹簧、声音、主题
│   │   └── data/             # 定理依赖数据
│   ├── showcase/             # 完整展示页源码
│   ├── catalog/              # 组件目录源文件
│   ├── tools/                # 构建、检测与逐帧捕获
│   ├── project/              # 生成的设计系统输入资料
│   └── dist/                 # 单文件展示与目录成品
│
├── overture/                  # 03 · 影像、品牌与舞台式交互
│   ├── src/
│   │   ├── core.js           # 组件注册与基础协议
│   │   ├── dynamics.js       # 光圈、显影、弹簧运动核心
│   │   ├── engine.mjs        # three.js / TSL 图形引擎
│   │   └── catalog-data.mjs  # 46 个组件的统一清单
│   ├── project/              # 设计变量、规范、组件资料与素材
│   ├── tools/                # 编译、内嵌与校验
│   ├── tests/
│   └── dist/                 # 独立运行时、页面与完整展示
│
├── ds-viewer/                 # 设计系统目录生成器
├── docs/assets/              # README 封面图形
├── serve.mjs                  # 根目录 Node.js 静态服务器
└── LICENSE                   # MIT
```

### 一次曝光，是如何连起来的？

根目录 [`index.html`](index.html) 承担串场、导航、语言与动效偏好；[`exposure/`](exposure/) 负责各体系的首屏和组件集成页。

- 三个世界各有专属的加载动画，来自 `exposure/loaders.js`。
- 展示页与容器通过 `exposure/page.js` 传递进度、就绪、暂停和声音状态。
- 滚动负责衔接相邻场景；实际材质、点阵与影像效果仍由各系统自身绘制。
- 总览页可切换中英文与动效模式。完整动效也可以通过 `?motion=full` 请求。

### 技术路线，各有取舍。

| | Lens | Lattice | Overture |
| :--- | :--- | :--- | :--- |
| **UI 基础** | 原生 DOM + CSS | 原生 DOM + CSS | 原生 DOM + CSS |
| **图形实现** | WebGL2 光学渲染器 | three.js + GPUComputationRenderer | three.js / TSL + WebGPU / WebGL2 |
| **运动模型** | 阻尼弹簧、透镜形变 | 共享时钟、弹簧、点集映射 | 光圈、显影、解析弹簧 |
| **源码入口** | [`index.js`](lens/lab/design-system/index.js) | [`index.js`](lattice/src/index.js) | [`core.js`](overture/src/core.js) |
| **样式与变量** | CSS + JS / JSON token | CSS token 与组件样式 | `project/tokens.json` 生成 CSS |
| **可复用方式** | 本地 ESM 包 | ES modules / 打包复用 | `Overture.mount()` / 静态资源 |
| **独立展示** | 单 HTML | 单 HTML | 单 HTML |

**真实内容，交给原生 HTML；光、粒子与运动，交给各自的渲染器。** 这也让键盘输入、文字选取、常规布局与浏览器的可访问能力能够继续发挥作用。

---

<a id="development"></a>
## 从欣赏，到自己动手。

预构建的展示页已放在仓库中。要修改组件、调节画面或重新打包，可以分别进入对应的工作目录。

### Lens · 调整光与材质

```bash
cd lens/lab

npm start       # http://127.0.0.1:4173/
npm test        # Node.js 测试
npm run check   # 静态检查
npm run build   # 重建 Lens 展示页和单文件产物
```

此工作区无第三方运行时依赖；组件包可作为本地 `@lens/design-system` 引入。设计变量源、组件实现和底层光学渲染器均位于 `design-system/`。

### Lattice · 重组一整个世界

```bash
cd lattice

npm install     # 安装本地构建需要的 three.js、esbuild 等
npm run dev     # 启动本地开发服务
npm run build   # 重建单文件展示、project/ 与组件目录
```

`three.js` 固定使用 0.186.1 并打包进成品。按需运行 `node tools/smoke.mjs`、`node tools/check-dist.mjs`、`node tools/check-catalog.mjs` 检查交互与构建结果；`node tools/capture.mjs` 可生成逐帧截图。

### Overture · 打造自己的舞台

```bash
cd overture

npm start        # http://127.0.0.1:4198/
npm run build    # 构建运行时、目录和单文件展示
npm test         # 状态与运动模型测试
npm run verify   # 构建与资源一致性检查
```

依赖的脚本、字体、照片和固定版本的 three.js 均保存在仓库中。若修改嵌入单文件的图片或视频，先按 [构建说明](overture/README.md) 更新 `src/embed/` 中的素材副本。

### DS Viewer · 把设计系统整理成一本可操作的手册

[`ds-viewer/`](ds-viewer/) 是零依赖的目录生成器。它读取组件预览、设计变量、规范和资产，生成可在本地查看的设计系统页面。

```bash
# 在仓库根目录执行
node ds-viewer/build.mjs lattice
node ds-viewer/build.mjs overture
```

生成结果位于各自的 `dist/catalog/index.html`。每张组件卡在独立 iframe 中运行；对大量 WebGL 预览，查看器还会按视口管理图形上下文，避免同时打开过多 GPU 场景。

> **改源码，重建成品。** `dist/` 和生成的 `project/` 内容以构建脚本为准；在源文件中修改组件与设计变量，才能让展示、目录和复用代码保持一致。

---

## 让交互，适应每一种使用方式。

好的动画，应该在需要的时候出现。

- **鼠标与触摸**：支持拖动、滚动、触点操作与实时材质反馈；具体行为依组件定义。
- **键盘与语义**：控件保留原生 HTML 的输入、焦点和无障碍状态；各系统提供键盘交互路径。
- **动效选择**：设计系统包含 `prefers-reduced-motion` 适配；总览及部分完整展示默认播放完整动效，并提供切换入口。
- **声音选择**：Lens、Lattice、Overture 的交互音效均由代码合成；默认关闭。
- **图形兼容**：Lens 在缺少 WebGL2 时使用 CSS 玻璃材质；Overture 按 WebGPU、WebGL2、静态画面依次选择；Lattice 需要 WebGL2 支持。
- **离线使用**：三份单文件演示可独立打开。Lens 与 Overture 的运行资源内嵌；Lattice 的可选 Web 字体离线回退系统字体。

有关各平台的测试覆盖与具体边界，可查看 [Lens 验证](lens/lab/design-system/VERIFICATION.md)、[Lattice 验证](lattice/VERIFICATION.md) 和 [Overture 验证](overture/VERIFICATION.md)。

---

## 取走灵感。留下你的作品。

你可以先体验三套系统，再挑选需要的组件、图形或动作，将它们带进自己的网页、产品原型、作品集或视觉实验。

| 想做什么 | 从这里开始 |
| :--- | :--- |
| 做一套真正折射背景的玻璃 UI | [Lens ESM 包](lens/lab/design-system/) · [API](lens/lab/design-system/README.md) |
| 让文字、数据和模型在粒子之间变形 | [Lattice 点集实现](lattice/src/gl/) · [使用指南](lattice/README.md) |
| 把摄影感和戏剧化转场引入品牌网页 | [Overture 组件](overture/src/) · [接入说明](overture/project/guidelines/30-api.md) |
| 生成自己的组件目录与设计系统文档 | [DS Viewer](ds-viewer/README.md) |
| 直接研究整站转场与三套加载动画 | [首页](index.html) · [Exposure](exposure/) |

### 开源许可与素材

代码采用 **[MIT License](LICENSE)**，可在保留许可证与版权声明的前提下使用、修改与分发。原许可证中的版权归属为 **© 2026 DayDreamInAReverie**。

随附第三方资源遵循各自许可证：

- **three.js**：MIT。见 [Lattice 许可证](lattice/THREE-LICENSE.txt) 与 [Overture 许可证](overture/project/components/lib/THREE-LICENSE.txt)。
- **Bodoni Moda / Manrope**：SIL OFL。许可文本位于 [`overture/project/fonts/`](overture/project/fonts/)；部分其他页面通过 Google Fonts 加载字体。
- **Overture 示例影像**：部分照片及视觉参考使用 AI 生成素材；来源与版本见 [`overture/SOURCES.md`](overture/SOURCES.md)。

---

<div align="center">

<sub>ONE EXPOSURE · THREE DESIGN SYSTEMS</sub>

<h3>光，有方向。点，有秩序。每一次触碰，都有回响。</h3>

<p><strong><a href="#start">再次探索 ↑</a></strong></p>

<sub>Made for the native web. Crafted to be explored.</sub>

</div>
