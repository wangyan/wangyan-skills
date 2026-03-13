# wangyan-skills


王同学的 Skills 技能合集，包括内容类技能 (Content Skills) 、生成类技能 (Generation Skills) 和工具类技能 (Tool Skills)。

## 前置要求

- 已安装 Node.js 环境

## 安装方法

### 使用 skills CLI 安装（推荐）

1. 全局安装 skills CLI 工具

```bash
npm install -g skills@latest
```

2. 交互式安装技能（可选择安装哪些技能）

```bash
# github 镜像源
skills add wangyan/wangyan-skills

# gitcode 镜像源 (推荐国内用户使用)
skills add https://gitcode.com/wang_yan/wangyan-skills.git
```

3. 手动安装指定技能

```bash
skills add https://github.com/wangyan/wangyan-skills/tree/main/skills/wangyan-gemini-image-gen
```

### 使用 Claude Code 安装

1. 注册插件市场

```bash
/plugin marketplace add wangyan/wangyan-skills
```

2. 安装指定类别插件

```bash
/plugin install content-skills@wangyan-skills
/plugin install generation-skills@wangyan-skills
/plugin install utility-skills@wangyan-skills
```

## 技能分类

### 内容类技能 (Content Skills)

### 生成类技能 (Generation Skills)

#### [wangyan-gemini-image-gen](skills/wangyan-gemini-image-gen/SKILL.md)

> 通过 Gemini 模型实现图片生成、编辑与多图合成。

**主要特性：**

- 文生图：根据文字描述生成图片
- 图片编辑：基于已有图片进行修改
- 多图合成：最多支持 14 张图片合成
- 支持 OpenAI 兼容格式和 Google 原生格式两种 API
- 内置模型自动轮询机制，提升可用性
- 可自定义 API 端点和密钥

**安装依赖：**

1. 安装 Python 3

```bash
# macOS
brew install python3

# Ubuntu/Debian
sudo apt update && sudo apt install python3 python3-pip

#CentOS/RHEL
sudo yum install python3 python3-pip
```

2. 安装 uv


```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# 使用 pip
pip install uv

# 确保 `uv` 在 PATH 中可用
uv --version
```

**安装技能：**

```bash
# 使用 skills CLI 安装技能 (推荐)
skills add https://github.com/wangyan/wangyan-skills/tree/main/skills/wangyan-gemini-image-gen

# 使用 Clawhub CLI 安装技能
clawhub install wangyan-gemini-image-gen

# 使用 skillhub 安装技能
curl -fsSL https://skillhub-1388575217.cos.ap-guangzhou.myqcloud.com/install/install.sh | bash  -s -- --no-skills
skillhub install wangyan-gemini-image-gen
```

**环境变量配置：**

```json
{
  "skills": {
    "entries": {
      "wangyan-gemini-image-gen": {
        "enabled": true,
        "apiKey": "your-api-key",
        "env": {
          "GEMINI_API_KEY": "your-api-key",
          "GEMINI_BASE_URL": "https://api.example.com/v1",
          "GEMINI_MODEL": "gemini-3.1-flash-image-preview",
          "GEMINI_API_FORMAT": "openai",
          "GEMINI_TIMEOUT": "300",
          "GEMINI_RESOLUTION": "1K",
          "GEMINI_OUTPUT_DIR": "output/images"
        }
      }
    }
  }
}
```

更多详细信息请参阅 [SKILL.md](skills/wangyan-gemini-image-gen/SKILL.md)。

### 工具类技能 (Tool Skills)

## 许可证

MIT

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=wangyan/wangyan-skills&type=Date)](https://www.star-history.com/#wangyan/wangyan-skills&Date)