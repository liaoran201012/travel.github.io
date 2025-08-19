# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个符合 Google Ads 要求的旅行优惠落地页平台，支持中英文内容。项目为静态 HTML/CSS/JavaScript 网站，专为旅行推广活动设计，包含 Google Ads 所需的合规页面。

## 文件结构与架构

### 核心落地页
- **travel.html** - 主要落地页面，包含旅行优惠和品牌展示
- **travel - 副本.html/txt** - 落地页的备份版本

### 合规页面（Google Ads 要求）
所有合规页面使用一致的样式设计，完全响应式：
- **privacy-policy.html** - 隐私政策，包含数据收集披露
- **terms-of-service.html** - 服务条款和联盟关系披露
- **disclaimer.html** - 旅行信息和第三方服务免责声明
- **cookie-policy.html** - 符合 GDPR/CCPA 的 Cookie 使用政策
- **subscription-terms.html** - 订阅服务条款
- **about-us.html** - 公司信息和团队详情
- **contact-us.html** - 联系表单和商务信息

### 资源文件
- **zimages/** - 旅行目的地图片（paris-city.jpg, tokyo-city.jpg, newyork-city.jpg, venice-city.jpg）

### 项目文档
- **README.md** - 项目概述和合规特性
- **修改说明.md** - 品牌名称和推广术语的修改说明
- **图片说明.md** - 图片规格和要求
- **推广链接动画代码分布说明.md** - 推广组件代码放置指南
- **推广链接.txt** - 推广组件脚本集合

## 开发命令

项目使用静态 HTML 文件，无需构建系统：

### 本地开发
```bash
# 本地服务器运行（任何 HTTP 服务器）
python -m http.server 8000
# 或者
npx serve .
```

### 文件编辑
- 直接编辑 HTML/CSS/JS 文件
- 无需编译或构建过程
- 刷新浏览器即可看到更改

## 核心架构模式

### 响应式设计
- 移动优先的 CSS 方法
- 所有页面统一断点设置
- 触摸友好的交互元素

### 推广组件集成系统
主落地页预设了 8 个推广组件代码插入位置：
1. **HERO 区域** - 页面顶部吸引区
2. **功能区域** - 功能描述后
3. **目的地轮播** - 热门目的地后
4. **品牌区域** - 每个服务品牌卡片前
5. **用户评价** - 用户评价后
6. **旅行提示** - 旅行建议后

### 合规架构
- 所有合规页面通过内联 CSS 共享一致样式
- 标准化的页头/页尾结构
- 各页面集中化联系信息变量
- 整站集成联盟披露声明

### 品牌名称处理
代码库已修改移除特定品牌名称：
- "Tiqets" → "Attraction Booking Platform"
- "Airalo" → "Global eSIM Service"
- "Kiwi.com" → "Flight Search Platform"
- 推广术语替换为中性语言

## 内容管理

### 多语言支持
- 主要内容为中文，包含英文元素
- 元描述和标题针对搜索优化
- 针对中国市场的文化考量

### 图片管理
- 标准图片尺寸：300x200px（目的地），400x200px（服务）
- 图片存储在 zimages/ 目录
- 网页性能优化

### 推广代码集成
推广脚本准备就绪，可在标记位置插入，包含详细注释说明：
- 放置目的
- 推荐组件类型
- 具体插入脚本代码

## 维护说明

### 定期更新内容
- 所有合规页面的联系信息
- 法律合规内容审查
- 推广代码 URL 验证
- 图片资源优化

### Google Ads 合规性
- 所有必需法律页面齐全并已链接
- 联盟关系明确披露
- 隐私政策符合 GDPR/CCPA 要求
- 联系信息易于访问

### 文件依赖
- 无外部依赖或包管理器
- 所有样式和脚本内联以确保最大兼容性
- 独立部署就绪