# learning-system-skill

AI 领域系统学习体系 Skill，适用于 [OpenClaw](https://github.com/openclaw/openclaw) Agent。

将零散的资讯、调研、代码实战转化为体系化的 AI 领域专业知识。

## 核心理念

**输入不等于学习。** 看了 100 篇推文不代表懂了推理优化。改了 3 个 MCP bug 不代表吃透了 MCP 协议。

学习 = 输入 + 加工 + 关联 + 输出。

## 功能

- 📊 **AI 知识图谱** — 6 大领域、31+ 主题，三级掌握程度标记（🔴入门 🟡熟悉 🟢精通）
- 📝 **深度学习笔记** — 基于实战的主题深入研究，含标准化模板
- 🔄 **实战复盘** — 每次 PR/问题解决后提炼学习点
- 🔗 **关联网络** — 技术关联、实战关联、对比关联
- ⏰ **每周学习回顾** — 自动化周期性知识管理
- 🔧 **健康检查** — 分析知识图谱健康度，给出改进建议

## 知识图谱领域

```
基础理论: Transformer、Attention、Tokenization、位置编码
训练:     预训练、微调(SFT/RLHF/DPO)、分布式训练、数据工程
推理:     量化、KV Cache、推测解码、服务框架(vLLM/SGLang/TRT-LLM)
Agent:    工具调用、MCP协议、多Agent编排、记忆管理、安全
应用:     RAG、代码生成、多模态、语音、视频生成
可解释性: 机械可解释性、SAE、因果干预、探针
```

## 文件结构

```
learning-system/
├── SKILL.md                          # Skill 定义文件
├── README.md                         # 本文件
├── scripts/
│   └── health_check.py               # 健康检查脚本
└── references/
    └── weekly-review-guide.md         # 每周回顾指南
```

配合使用的笔记目录（需自行创建）：

```
notes/areas/
├── ai-knowledge-map.md               # 知识图谱
├── deep-dives/                        # 深度笔记
│   └── mcp-tool-call-design.md        # 示例笔记
└── weekly-reviews/                    # 每周回顾
```

## 使用方式

### 1. 安装

将本目录放到 OpenClaw workspace 的 `skills/` 下：

```bash
cp -r learning-system ~/.openclaw/workspace/skills/
```

### 2. 初始化笔记目录

```bash
mkdir -p ~/.openclaw/workspace/notes/areas/deep-dives
mkdir -p ~/.openclaw/workspace/notes/areas/weekly-reviews
```

### 3. 健康检查

```bash
python3 scripts/health_check.py
```

输出示例：

```
# 学习体系健康报告
生成时间: 2026-02-11 19:30

## 知识图谱
- 总主题数: 31
- 🔴 入门: 14 (45%)
- 🟡 熟悉: 15 (48%)
- 🟢 精通: 2 (6%)

## 建议
- ⚠️ 入门级主题过多，建议本周选 1-2 个深入研究
```

### 4. 配置每周回顾 Cron

在 OpenClaw 中配置 cron job，每周日晚自动触发学习回顾。

## 掌握程度标记

| 等级 | 标记 | 标准 |
|------|------|------|
| 入门 | 🔴 | 听说过，知道是什么 |
| 熟悉 | 🟡 | 读过源码或论文，能解释原理 |
| 精通 | 🟢 | 有实战经验，能独立设计和排错 |

### 升级标准

- 🔴→🟡：读过核心源码或关键论文，能向别人解释清楚
- 🟡→🟢：有真实的代码贡献或项目实战，踩过坑并解决

## License

MIT
