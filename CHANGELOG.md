## 2026-03-13

### Added（新增）
- **Gemini 图片生成技能**（`skills/wangyan-gemini-image-gen/`）：
  - 新增 `generate_image.py` 脚本，支持文生图、图片编辑、多图合成
  - 支持 OpenAI 兼容格式和 Google 原生格式两种 API 调用方式
  - 内置模型自动轮询机制，当首选模型不可用时自动切换备选模型
