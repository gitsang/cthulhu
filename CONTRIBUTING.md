# Contributing Guide

感谢你为 Cthulhu handbook 做贡献。

本仓库的目标是维护一个可持续扩展、可检索、可审阅的克苏鲁神话资料库。提交前请先阅读：

- `docs/design/handbook-design.md`
- `docs/plan/handbook-execution-plan.md`
- `docs/style-guide.md`

## 1. Contribution Types

- 新增条目：新增神祇、生物、地点、典籍、遗物、仪式等。
- 条目修订：修正事实、补充来源、统一格式。
- 结构优化：目录、索引、交叉引用、模板改进。

## 2. Workflow

1. 明确修改范围（建议一次只处理一个子域）。
2. 按 `docs/style-guide.md` 编写或修订内容。
3. 自查字段完整性与交叉引用。
4. 在 `CHANGELOG.md` 记录变更。
5. 提交变更并在说明中写清“做了什么 + 为什么”。

## 3. Entry Template

可复制以下模板用于实体类条目：

```md
#### 名称 (English Name)

分类：

理智损失：

##### 别名/称号

- 

##### 简介



##### 关键特征

- 

##### 遭遇或召唤条件

- 

##### 关联势力

- 

##### 出现作品

- 《》 ( )

##### 相关条目

- 
- 

##### 参考来源

- 原典：
- 扩展：
```

## 4. Required Quality Gates

提交前请确保：

- 字段完整：包含必填块，尤其是“相关条目”“参考来源”。
- 引用规范：作品格式为 `《中文名》 (English Title, Author)`。
- 交叉引用：每个条目至少 2 个相关条目。
- 来源区分：原典与扩展设定分开列出。
- 结构一致：标题层级和列表格式符合 style guide。

## 5. Scope Control Rules

- 迁移任务优先“结构重排”，避免同时大改语义。
- 若需要重写设定解释，请单独提交并说明依据。
- 不要在一次改动中混合“结构迁移 + 大量新内容”。

## 6. Change Log Rule

每个逻辑变更集（通常对应一次 commit）都应更新 `CHANGELOG.md`，最少包含：

- 日期（`YYYY-MM-DD`）
- 变更类型（新增/修订/迁移/规范/工具）
- 涉及路径（同一变更涉及多个文件时合并为一条）
- 关键说明（一句话说明目的）

## 7. Review Checklist (for reviewers)

- 该改动是否符合计划阶段目标。
- 是否引入 schema 漂移。
- 是否存在悬空交叉引用。
- 是否缺失来源或引用格式错误。
- 是否影响 `readme.md` 入口导航的清晰性。
