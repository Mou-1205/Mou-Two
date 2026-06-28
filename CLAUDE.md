# Mou-Two — 个人网站

## 项目简介

某炜的个人开发者网站，纯 HTML/CSS/JS 单文件，零框架依赖。
部署：GitHub Pages → mouy.site（master 分支自动部署）

## 技术栈

- HTML5 + CSS3 + Vanilla JavaScript
- 字体：Instrument Serif（标题）+ DM Sans（正文）+ Noto Serif SC（中文）via Google Fonts
- CSS 变量系统（`--` 前缀）
- Canvas API（墨迹擦除动效）
- IntersectionObserver（滚动渐入动画）

## 文件结构

```
Mou-Two/
├── index.html          # 主页面（HTML+CSS+JS 一体，~800行）
├── assets/
│   ├── 背景.png        # Hero 区背景图
│   ├── 头像.jpg        # 导航栏头像
│   ├── 赞助.jpg        # 赞赏二维码
│   └── screenshot.png  # README 效果图
├── README.md
├── DEV.md              # 开发文档（本地，不推送）
└── .gitignore
```

## 设计系统

| 变量 | 值 | 用途 |
|------|-----|------|
| `--bg` | `#f6f4f0` | 页面背景 |
| `--accent` | `#4a7c59` | 主题绿 |
| `--text-primary` | `#1a1a17` | 标题文字 |
| `--text-body` | `#4a4a45` | 正文文字 |
| `--radius` | `14px` | 卡片圆角 |

## 开发规范

- 单文件架构，所有 CSS 和 JS 内联在 `index.html`
- 使用 `const`/`let`，不用 `var`
- 动画必须支持 `prefers-reduced-motion`
- 滚动触发动画使用 IntersectionObserver，不用 scroll 事件监听
- 外部链接加 `target="_blank" rel="noopener noreferrer"`
- 中文内容，中文 HTML `lang="zh-CN"`

## 部署

```bash
git add .
git commit -m "描述"
git push origin master
# GitHub Pages 自动部署到 mouy.site
```

## 注意事项

- 背景图边缘用 `::after` 渐变遮罩柔化
- `display: none` 不能做 CSS 过渡，需用 `visibility + opacity`
- 页脚 ICP 备案号必须保留
- DEV.md 不推送到 GitHub（已在 .gitignore 中）
