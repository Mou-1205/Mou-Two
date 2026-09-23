# 某炜 — 个人网站

> 以好奇心构建，以清晰度交付。

**🔗 在线访问：[www.mouy.site](https://www.mouy.site)**

![网站效果图](assets/og.jpg)

## 简介

某炜的个人开发者网站，纯 HTML/CSS/JS 单文件架构，零框架依赖。展示技能、成长轨迹和项目作品。

## 技术栈

- HTML5 + CSS3 + Vanilla JavaScript（无框架）
- CSS Grid / Flexbox 响应式布局
- CSS 变量系统（`--` 前缀设计令牌）
- Canvas API（墨迹擦除动效）
- IntersectionObserver（滚动渐入动画）
- Clipboard API（邮箱复制）
- localStorage（生日点击计数）
- 自托管字体（无 Google Fonts 外链）：
  - Instrument Serif（拉丁标题）
  - DM Sans（拉丁正文，可变字重 400–500）
  - Noto Serif SC（中文，**仅站内 440 字子集**，缺字回退系统字体）

## 特性

- 固定导航栏，滚动时显示分隔线
- Hero 区背景图 + 渐变遮罩柔化边缘
- 关于我弹窗（头像、技能标签、生日倒计时、坐标卡片）
- 生日卡片点击计数器（localStorage 本地存储）
- 技能卡片（3 类：底层与系统、全栈与移动端、工具与工程化）
- 项目卡片用 SVG 插画封面（Blog 书桌静物 / 个人站水墨晕染）
- 赞助弹窗（点击弹出二维码）
- 自定义 404 页面
- Konami Code 彩蛋（↑↑↓↓←→←→BA）
- 移动端响应式适配
- `prefers-reduced-motion` 无障碍支持
- Esc 关闭弹窗、键盘可达
- Umami 数据统计

## 项目结构

```
Mou-Two/
├── index.html              # 主页面（HTML+CSS+JS 一体）
├── 404.html                # 自定义 404 页面
├── assets/
│   ├── fonts/              # 自托管 woff2（约 260KB）
│   │   ├── InstrumentSerif-400.woff2
│   │   ├── InstrumentSerif-400-italic.woff2
│   │   ├── DMSans.woff2
│   │   └── NotoSerifSC.woff2   # 仅站内用字子集
│   ├── 背景.png            # Hero 区背景图（原图，不压缩）
│   ├── 头像.jpg            # 导航栏头像
│   ├── 赞助.webp           # 赞赏二维码
│   ├── 备案图标.png        # 公安备案图标
│   └── og.jpg              # Open Graph 分享图（1200×630）
├── README.md
├── DEV.md                  # 开发文档
└── .gitignore
```

> **字体子集注意**：`NotoSerifSC.woff2` 只包含当前页面用到的字。文案若新增汉字，需要按新字表重新子集化，否则新字会回退到系统字体。

## 本地运行

```bash
git clone https://github.com/Mou-1205/Mou-Two.git
cd Mou-Two
# 用任意浏览器打开 index.html
start index.html
```

## 部署

线上站点：宝塔面板 `my.mouy.site`（`www.mouy.site`），推送到 GitHub `main` 后由 Git Webhook / 面板同步到站点目录。

```bash
git add .
git commit -m "描述"
git push origin main
```

## License

MIT
