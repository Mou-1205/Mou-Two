# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目简介

某炜的个人开发者网站，纯 HTML/CSS/JS 单文件，零框架依赖。
部署：GitHub Pages → mouy.site（main 分支自动部署）

## 技术栈

- HTML5 + CSS3 + Vanilla JavaScript
- 字体：Instrument Serif（标题）+ DM Sans（正文）+ Noto Serif SC（中文）via Google Fonts
- CSS 变量系统（`--` 前缀）
- Canvas API（墨迹擦除动效）
- IntersectionObserver（滚动渐入动画）

## 常用命令

```bash
# 本地预览（直接用浏览器打开）
start index.html

# 部署
git add . && git commit -m "描述" && git push origin main
# GitHub Pages 自动部署到 mouy.site
```

## 架构说明

单文件架构，所有 CSS 和 JS 内联在 `index.html`（~800行）：

- `<style>` 标签：CSS 变量定义 + 响应式布局 + 动画样式
- `<script>` 标签：IntersectionObserver 滚动动画 + Canvas 墨迹擦除 + 弹窗交互

关键实现：
- 滚动渐入：IntersectionObserver 监听元素进入视口，触发 `.visible` 类
- 墨迹擦除：Canvas 绘制遮罩，鼠标移动时清除像素实现擦除效果
- 弹窗动画：使用 `visibility + opacity` 而非 `display: none`（后者无法 CSS 过渡）

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

## 注意事项

- 背景图边缘用 `::after` 渐变遮罩柔化
- `display: none` 不能做 CSS 过渡，需用 `visibility + opacity`
- 页脚 ICP 备案号必须保留
- DEV.md 不推送到 GitHub（已在 .gitignore 中）
