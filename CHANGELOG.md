# 📝 Changelog (更新日志)

All notable changes to the personal calendar sync project will be documented in this file.

## [1.1.0] - 2026-06-08

### Added
- 支持在 `testnote` 仓库中通过 GitHub 网页端手动触发工作流 (`workflow_dispatch`)。

### Changed
- 优化了 GitHub Actions 构建触发规则：为 `sync-to-calendar.yml` 流水线添加了路径限制 (`paths` filter)。
  - **影响**：现在仅在 `todo/` 或 `obsidian/日历/` 目录发生变动时触发构建，日常非待办笔记修改将不再产生 Actions 运行。
  - **效果**：极大节约了 GitHub Actions 免费计算额度，同时消除了快速连续编辑笔记时造成的大量部署取消警告与通知轰炸。

### Documented
- 在 `README.md` 的“安全性与消费控制说明”部分，添加了第 3 条“智能构建触发优化”的说明。

---

## [1.0.0] - 2026-06-08

### Added
- 初始化个人日历自动同步系统。
- 新增 `parse-tasks.js` 任务提取解析脚本。
- 新增 `sync-to-calendar.yml` 自动化流水线。
- 新增 GitHub Pages 用于提供静态订阅源。
