# 项目记忆 — 珞莎美妆工作室工作台

## 项目概述
- 纯前端单页HTML应用（beauty-workbench.html），无框架依赖
- 用户：龙丽莎，珞莎美妆工作室店主 + 抖音美妆自媒体博主
- 偏好移动端使用（iPhone Safari）
- 数据使用localStorage持久化，STORAGE_KEY当前为 `beauty_wb_v5`

## 技术架构
- 单文件HTML应用（约942行，114KB）
- PWA配置：manifest.json + sw.js（network-first策略，cache v2）
- 入口：index.html → 重定向到 beauty-workbench.html
- 15个视图模块，侧边栏可折叠分组导航

## 关键设计决策
- 搜索筛选修复方案：searchVals全局对象 + restoreSearchFocus()渲染后恢复焦点
- 脚本统一数据结构：合并shootDrafts+scripts为统一scripts数组，含storyboard字段
- 数据迁移：loadData()中自动检测旧数据结构并迁移
- 饼图：pieChartFloat()支持点击扇区筛选 + 联动更新

## 部署
- CloudStudio沙箱部署，当前链接: https://6736465c3ec046fb8a39c1283cbff847.bj2.agentos-app.net
- 每次更新后sw.js cache版本号需递增

## 用户偏好
- 粉色系美妆风格
- 对内容管理要求高，特别在意脚本模板和素材组织
- 不喜欢死板的UI，偏好有动感和交互感的设计
- 要求功能实用，不喜欢假的AI（宁可要可编辑模板也不要假AI）
