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
