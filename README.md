# wangyan-skills


王同学的 Skills 技能合集，包括内容类技能 (Content Skills) 、生成类技能 (Generation Skills) 和工具类技能 (Tool Skills)。

## 前置要求

- 已安装 Node.js 环境

## 安装方法

### 使用 skills CLI 安装（推荐）

1. 交互式安装

```bash
# github 镜像源
npx skills add -g wangyan/wangyan-skills

# gitcode 镜像源 (推荐国内用户使用)
npx skills add -g https://gitcode.com/wang_yan/wangyan-skills.git
```

2. 安装指定技能

```bash
# github 镜像源
npx skills add -g wangyan/wangyan-skills \
  --skill gemini-image-gen

# gitcode 镜像源 (推荐国内用户使用)
npx skills add -g https://gitcode.com/wang_yan/wangyan-skills.git \
  --skill gemini-image-gen
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

| 技能 | 描述 |
|------|------|
| 整理中... | — |

### 生成类技能 (Generation Skills)

| 技能 | 描述 |
|------|------|
| [gemini-image-gen](skills/gemini-image-gen/SKILL.md) | 通过 `Nano Banana` 实现文生图、图片编辑与多图合成，支持 OpenAI 兼容和 Google 原生两种 API 格式，可自定义端点和密钥 |

### 工具类技能 (Tool Skills)

| 技能 | 描述 |
|------|------|
| 整理中... | — |

## 许可证

MIT

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=wangyan/wangyan-skills&type=Date)](https://www.star-history.com/#wangyan/wangyan-skills&Date)