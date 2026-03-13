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
- **配置文档更新**（`skills/wangyan-gemini-image-gen/SKILL.md`）：
  - 更新配置表格，移除 openclaw.json 字段列
  - 替换 JSON 配置示例为环境变量配置示例
