## 2026-04-14

### Refactor（重构）
- **技能目录重命名**（`skills/`）：
  - 移除所有技能目录的 `wangyan-` 前缀，统一简化命名
  - 涉及：`article-illustrator`、`compress-image`、`cover-image`、`format-markdown`、`gemini-image-gen`、`markdown-to-html`、`url-to-markdown`

### Changed（改进）
- **安装文档简化**（`README.md`）：
  - 更新安装命令为 `npx skills add -g`，无需全局安装 CLI
  - 新增 `--skill` 参数支持安装指定技能
  - 将技能列表改为表格格式，结构更清晰
  - 移除 README 中冗余的依赖安装说明，聚焦核心内容
- **Gemini 图片生成技能文档**（`skills/gemini-image-gen/SKILL.md`）：
  - 更新技能名称为 `gemini-image-gen`（移除 `wangyan-` 前缀）
  - 新增触发判断说明，明确触发词与不触发场景
  - 简化环境变量配置说明，移除 `.env` 文件多路径配置
  - 更新安装命令中的技能路径

## 2026-03-14

### Documentation（文档）
- **安装文档优化**（`README.md`、`skills/wangyan-gemini-image-gen/SKILL.md`）：
  - 新增 `gitcode` 镜像源和腾讯 `skillhub` 安装方式，优化国内用户安装体验
  - 调整 SKILL.md 章节顺序，将"安装技能"章节移至"使用方法"之前

## 2026-03-13

### Added（新增）
- **Gemini 图片生成技能**（`skills/wangyan-gemini-image-gen/`）：
  - 新增 `generate_image.py` 脚本，支持文生图、图片编辑、多图合成
  - 支持 OpenAI 兼容格式和 Google 原生格式两种 API 调用方式
  - 内置模型自动轮询机制，当首选模型不可用时自动切换备选模型

### Removed（移除）
- **配置加载逻辑简化**（`skills/wangyan-gemini-image-gen/scripts/generate_image.py`）：
  - 移除 `_load_openclaw_config` 函数及 openclaw.json 配置读取逻辑
  - 简化配置优先级为：CLI 参数 > 环境变量
  - 更新错误提示信息，移除 openclaw.json 相关说明

### Documentation（文档）
- **项目文档完善**（`README.md`）：
  - 新增项目介绍和技能分类说明
  - 新增 skills CLI 和 Claude Code 两种安装方法
  - 新增 Gemini 图片生成技能的依赖安装、使用方法和环境变量配置示例
- **技能文档优化**（`skills/wangyan-gemini-image-gen/SKILL.md`）：
  - 调整章节顺序，将"触发判断"移至"依赖安装"之前
  - 更新环境变量配置示例为 JSON 格式
  - 优化代码块格式和文档结构
