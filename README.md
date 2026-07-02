# 猫咪咖啡店 Cat Cafe Idle

一个清新手绘风的猫咪咖啡店挂机小游戏。玩家可以制作咖啡、接待顾客、喂猫、邀请新猫咪、安排猫咪岗位，并通过升级店铺提升经营效率。

## 直接进入

- 在线游玩入口：[开始游戏](https://akiteet.github.io/cat-cafe-idle/)
- 仓库文件入口：[cat-cafe-idle.html](./cat-cafe-idle.html)

如果在线入口暂时打不开，需要先在 GitHub 仓库的 `Settings -> Pages` 中启用 GitHub Pages，并选择 `main` 分支作为发布来源。

## 在线/本地运行

这是一个纯前端单文件小游戏，不需要安装依赖。

1. 下载或克隆仓库。
2. 直接用浏览器打开 `cat-cafe-idle.html`。

也可以在本地目录启动一个静态服务器：

```bash
python -m http.server 8000
```

然后访问：

```text
http://localhost:8000/cat-cafe-idle.html
```

## 玩法简介

- `手冲`：消耗咖啡豆，制作咖啡。
- `进豆`：消耗小鱼干，补充咖啡豆。
- `喂猫`：提升心情最低的猫咪。
- `邀请`：消耗小鱼干和口碑，解锁新猫咪。
- `猫咪岗位`：给猫咪分配收银、拉花、迎宾、陪伴等岗位。
- `顾客订单`：按需求上餐，获得小鱼干和口碑。
- `店铺升级`：升级设备、菜单和猫窝，提高经营效率。

游戏会使用浏览器 `localStorage` 自动保存进度，并计算一定的离线收益。

## 功能特点

- 纯 HTML/CSS/JavaScript 实现，无框架、无构建步骤。
- 一屏式经营面板，适合桌面浏览器直接游玩。
- PNG 猫咪角色素材，不使用几何图形假猫。
- 真实猫叫音效，可通过右上角按钮开关。
- 支持本地存档、离线收益、订单队列、每日目标和升级系统。

## 文件结构

```text
cat-cafe-idle/
├── cat-cafe-idle.html
├── assets/
│   ├── cat-*.png
│   ├── cat-cafe-cats.png
│   └── audio/
│       ├── cat-soft-mew.wav
│       ├── cat-food-mew.wav
│       └── SOURCES.txt
└── README.md
```

## 素材说明

- 猫咪图片：为本项目生成并裁切整理。
- 猫叫音效：来自 OpenGameArt 的 CC0 素材，详见 `assets/audio/SOURCES.txt`。

## 技术点

- Canvas/DOM 混合式视觉布局。
- CSS Grid/Flex 一屏式布局。
- Web Audio + HTML Audio 处理按钮反馈和真实猫叫。
- `localStorage` 保存游戏数据。

## 开发说明

修改后直接刷新浏览器即可查看效果。若需要重置游戏数据，可以点击游戏内的 `重置存档` 按钮，或清空浏览器 localStorage。
