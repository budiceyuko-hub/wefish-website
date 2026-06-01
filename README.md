# 钓遇 WeFish — 官方网站

> 每一次出钓，都是一场相遇

## 项目概述

钓遇 APP 官方品牌展示站点。纯静态 HTML 单页网站，部署于 GitHub Pages，自定义域名 dywefish.com。

## 技术栈

| 项 | 详情 |
|----|------|
| 类型 | 纯静态 HTML5 + CSS3 + Vanilla JS |
| 构建工具 | 无（直接编辑部署） |
| 外部依赖 | 零（无 CDN、无 npm、无框架） |
| 部署 | GitHub Pages + 自定义域名 |
| 域名 | dywefish.com（CNAME 记录） |

## 项目结构

```
wefish-website/
├── index.html              # 主页（1497行）
├── privacy.html            # 隐私政策
├── agreement/
│   └── index.html          # 用户协议
├── terms/
│   └── index.html          # 服务条款
├── privacy/
│   └── index.html          # 隐私政策（备用入口）
├── CNAME                   # GitHub Pages 域名绑定
├── assets/
│   ├── images/
│   │   └── logo.png        # APP Logo
│   └── icons/
│       ├── fish.svg         # 鱼类图标
│       ├── social.svg       # 社交图标
│       └── weather.svg      # 天气图标
└── README.md               # 本文档
```

## 页面结构（index.html）

| 区块 | 锚点 | 内容 |
|------|------|------|
| 导航栏 | `#navbar` | 固定顶部，品牌名 + 导航链接 |
| 英雄区 | `#top` | Canvas 粒子动画 + 标题 + 统计数据 |
| 核心功能 | `#features` | 出钓指数 / 钓点地图 / 钓友社区 |
| 指数算法 | `#index` | 6维出钓指数评级说明 |
| 钓点地图 | `#spots` | 地图动效 + 2394个钓点 |
| 社区 | `#community` | 钓友互动展示 |
| 下载区 | `#download` | 邮箱预约通知 |
| 页脚 | Footer | 版权 + 备案号占位 |

## CSS 设计系统

| 变量 | 值 | 用途 |
|------|-----|------|
| `--orange` | `#FF6B35` | 品牌主色 |
| `--orange-light` | `#FFB693` | 品牌辅色 |
| `--blue` | `#2196F3` | 强调色 |
| `--bg-dark` | `#0A0F1E` | 主背景 |
| `--bg-card` | `rgba(255,255,255,0.05)` | 卡片背景 |
| `--text-primary` | `#FFFFFF` | 主文字 |
| `--text-secondary` | `rgba(255,255,255,0.65)` | 次要文字 |
| `--radius-card` | `20px` | 卡片圆角 |
| `--radius-btn` | `50px` | 按钮圆角 |

## JavaScript 功能清单

| 功能 | 位置 | 说明 |
|------|------|------|
| Canvas 粒子动画 | L1363-1417 | 120个橙/蓝色粒子向上飘动 |
| 地图钓点动效 | L1421-1443 | 12个钓点带渐变延时 |
| 滚动渐入动画 | L1446-1459 | IntersectionObserver |
| Toast 提示 | L1462-1467 | 弹窗提示系统 |
| 邮箱验证+订阅 | L1474-1483 | 正则校验 + 提示 |
| 导航滚动效果 | L1486-1493 | 滚动加深背景 |

## 如何修改

### 改内容（文字/图片）
直接编辑对应 HTML 文件，提交推送即可生效。

### 改样式
所有 CSS 内联在 `<style>` 标签中（L14-966）。修改后刷新浏览器查看效果。

### 改 JS 动效
所有 JS 内联在 `<script>` 标签中（L1362-1494）。

### 部署
```bash
git add -A
git commit -m "更新描述"
git push origin main
```
GitHub Pages 自动部署，约 1-2 分钟后生效。

### 新增页面
1. 复制 `privacy.html` 作为模板
2. 修改内容和标题
3. 在 `index.html` 导航栏添加链接

## 待办

- [ ] 备案通过后，页脚填上 ICP 备案号
- [ ] 备案通过后，域名 DNS 从 GitHub Pages 切到腾讯云服务器
- [ ] 页脚添加 APP 备案号
- [ ] 下载区接入真实下载链接（替换邮箱预约）

## 相关项目

- 钓遇 APP 本体（独立项目）
- 上架备案清单：`D:\TXclaw\Claw\钓遇APP上架备案清单.md`
