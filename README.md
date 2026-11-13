# 面试准备 Skills

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

仓库提供三个独立的 skill，分别用于后端技术面试模拟、AI 应用开发面试模拟和简历批量出题。

## 逐轮模拟面试：backend-interview-simulator

[查看 skill](skills/backend-interview-simulator/SKILL.md)

AI 扮演后端技术面试官，每次只问一个问题，根据候选人的回答决定追问方向，结束后给出有回答证据支撑的评估报告。

- 支持日常实习、暑期实习、校招和社招 1–3 年；支持 Java、C++、Go 单语言或混合语言。
- 可选择六种面试官风格、严格或即时引导纠错模式，以及是否加入编码题。
- 可提供简历和岗位 JD，让项目深挖、技术题和最终反馈贴近目标岗位。
- 面试中记录已考察主题、薄弱点和待追问内容；支持暂停、恢复和提前结束。
- 技术知识库、面试官风格和评分规则放在该 skill 的 [references/](skills/backend-interview-simulator/references/) 中，按需加载。

安装后可以说：

```text
开始一场模拟面试。我是应届生，想练习 Java 后端面试。
```

面试中可以说“继续”“跳过”“结束”“换个风格”或“反馈”。

## AI 应用开发模拟面试：ai-dev-interview-simulator

[查看 skill](skills/ai-dev-interview-simulator/SKILL.md)

AI 模拟 AI 应用开发岗位面试，根据候选人的回答逐轮追问，结束后给出评分和反馈。

- 考察 LLM、Agent、RAG、MCP、Embedding、向量数据库及 AI 编程工具。
- 支持实习、校招和社招 1–3 年，可选择面试官风格和纠错模式。
- 可提供简历和岗位 JD 定制项目深挖与技术题，也可加入 Prompt 设计、Agent 流程设计或 RAG 实现等实操题。

安装后可以说：

```text
开始一场 AI 应用开发模拟面试。我想练习 Agent 和 RAG 项目深挖。
```

## 简历批量出题：resume-interview-question-generator

[查看 skill](skills/resume-interview-question-generator/SKILL.md)

候选人给出想分析的简历条目，AI 一次性生成主问题和追问文档，减少逐轮模拟面试的对话时间。只给项目/实习经历或只给专业技能都可以，不要求整份简历，也不限技术栈。

- 出题时只看面试官可见的简历条目。项目/实习题不受 JD 影响；专业技能题以简历为主，可少量加入 JD 强调但简历未写的技术问题，并标明来源。
- 先保存纯问题稿，再根据候选人的选择读取项目代码、文档等材料补充回答；材料中的隐藏细节不会反向变成面试题。
- 可选择“只要问题”或“问题和简短参考回答”；缺少依据的项目细节标为“待补充”。
- 按简历条目分组，主问题下列出可能的追问；默认在调用时当前工作目录的 `./resume/` 新建 UTF-8 Markdown 文档，不覆盖旧文件。

安装后可以说：

```text
根据下面这些简历条目，一次性生成面试主问题和追问文档：……
```

需要回答时可以直接说“问题和参考回答一起生成”，并提供项目代码、文档或补充说明。

## 安装

把当前仓库的 GitHub 链接和下面的请求一起发给支持 skills 的 AI 工具。

```text
请从我提供的 GitHub 仓库安装这三个 skill：
1. skills/backend-interview-simulator/
2. skills/ai-dev-interview-simulator/
3. skills/resume-interview-question-generator/
请将每个目录完整安装到当前工具的 skills 目录，并确认三个 skill 都能使用。
```

只需要其中一个时，在请求中明确指定对应的 skill 名称和目录。

## 项目结构

```text
.
├── skills/
│   ├── ai-dev-interview-simulator/
│   │   ├── SKILL.md                           # AI 应用开发模拟面试
│   │   └── references/                        # AI 应用开发知识库与规则
│   ├── backend-interview-simulator/
│   │   ├── SKILL.md                           # 逐轮模拟面试
│   │   └── references/                        # 模拟面试所需的知识库与规则
│   └── resume-interview-question-generator/
│       └── SKILL.md                           # 简历批量出题
├── README.md
└── LICENSE
```

## 贡献指南

欢迎补充题库、改进追问逻辑或修正文档。提交 PR 前请检查所改 skill 的触发范围和生成结果。题库内容可参照 [现有知识库](skills/backend-interview-simulator/references/common-backend-knowledge-base.md)。不要提交真实简历、项目代码或其他候选人资料。

## 许可证与致谢

本项目采用 [MIT License](LICENSE)。技术知识库部分引用了 [JavaGuide](https://github.com/Snailclimb/JavaGuide) 的高频面试题整理，仅作为面试考察点使用，不改变其原有许可。感谢 JavaGuide 和 [xiaolincoding](https://xiaolincoding.com/) 提供的公开资料。

AI 应用开发模拟面试 skill 来自 [Hazenix/ai-dev-interview-simulator](https://github.com/Hazenix/ai-dev-interview-simulator/tree/13010073f1473fa393752a5aee675c9ff764ce51)，适用相同的 MIT 许可证。
