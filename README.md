# 某炜 — 个人网站

> 以好奇心构建，以清晰度交付。

**🔗 在线访问：[www.mouy.site](https://www.mouy.site)**

![网站效果图](assets/screenshot.png)

## 简介

某炜的个人开发者网站，纯 HTML/CSS/JS 单文件架构，零框架依赖。展示技能、成长轨迹和项目作品。

## 技术栈

- HTML5 + CSS3 + Vanilla JavaScript（无框架）
- CSS Grid / Flexbox 响应式布局
- CSS 变量系统（`--` 前缀设计令牌）
- Canvas API（墨迹擦除动效）
- IntersectionObserver（滚动渐入动画）
- Google Fonts：Instrument Serif（标题）+ DM Sans（正文）+ Noto Serif SC（中文）

## 特性

- 固定导航栏，滚动时显示分隔线
- Hero 区背景图 + 渐变遮罩柔化边缘
- 技能卡片悬停动效
- 时间轴展示成长轨迹
- 项目卡片链接到 GitHub 仓库
- 赞助弹窗（点击弹出二维码）
- 移动端响应式适配
- `prefers-reduced-motion` 无障碍支持

## 项目结构

```
Mou-Two/
├── index.html          # 主页面（HTML+CSS+JS 一体，~800 行）
├── assets/
│   ├── 背景.png        # Hero 区背景图
│   ├── 头像.jpg        # 导航栏头像
│   ├── 赞助.jpg        # 赞赏二维码
│   └── screenshot.png  # README 效果图
├── README.md
├── CLAUDE.md           # Claude Code 项目上下文
└── .gitignore
```

## 本地运行

```bash
git clone https://github.com/Mou-1205/Mou-Two.git
cd Mou-Two
# 用任意浏览器打开 index.html
start index.html
```

## 部署

GitHub Pages 自动部署，推送到 `master` 分支即生效：

```bash
git add .
git commit -m "描述"
git push origin master
```

## License

MIT
