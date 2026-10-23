# Si2C

Si2C（Silicon to Carbon，硅基模型写给碳基读者）是一套 agent skill，用于指导 LLM 编写人类可读的中文技术文档。

Si2C 面向技术写作和改稿场景，帮助模型把调查材料整理成可发布文章。

## 它解决什么问题

LLM 技术文档常见三类症状：

- **佶屈聱牙**：长句拗口，主体和关系不清。
- **黑话太多**：内部术语妨碍读者理解。
- **容易发散**：过程噪音掩盖结论和证据。

## 核心原则

- **自包含**：不打开外链，读者也能理解核心结论和依据。
- **focus**：只保留支持结论、解释决策或帮助复核的内容。

focus 不等于一律缩短。无关过程应删除，关键背景和证据应补全。

## 适用范围

Si2C 适用于：

- bug 排查报告
- 故障分析和根因分析
- 技术调查
- 排查复盘
- 将 agent 工作底稿整理成可发布文章

## 文件结构

```text
Si2C/
├── SKILL.md
├── REFERENCE/
│   └── writing-reference.md
├── README.md
└── LICENSE
```

- `SKILL.md`：主规则、写作流程和完稿自检。
- `REFERENCE/writing-reference.md`：按需读取的实例、术语表和文体模板。

## 安装

将仓库安装到 agent skill 目录：

```bash
git clone https://github.com/q9good/Si2C.git ~/.agents/skills/Si2C
```

也可以使用你的 agent 支持的等价目录。

## 使用

写作或修改上述文体时，让 LLM 读取 `SKILL.md`。
需要实例、术语处理、证据打包、信息状态、改稿核对或结构选择时，再读取参考文件。

## 许可证

本项目使用 [MIT License](LICENSE)。
