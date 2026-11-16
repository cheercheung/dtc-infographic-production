# DTC 信息图生产

在 Codex 中打开本文件夹，读取 [[AGENTS|自动整理与 Git 同步规则]]，按 [[SOP|制作 SOP]] 操作

首次把 [[prompts/infographic|制图提示词]] 发给 Codex，保存该会话；后续把源 MD 和 keywords 发到同一会话，Codex 自动保存输入、生成图片、输出一句话总结并整理输出

```text
DTC信息图生产/
├── AGENTS.md
├── README.md
├── SOP.md
├── SOP.html
├── prompts/
│   └── infographic.md
├── 输入/
│   └── <日期-主题>/      原始 MD 与相关附件，由 Codex 自动建立
├── 输出/
│   └── <日期-主题>/      成图、总结、使用提示词与任务记录，由 Codex 自动建立
└── 示例/
    └── ugc-team-4x5-en.png
```

## Git 同步

本目录对应公开仓库：[dtc-infographic-production](https://github.com/cheercheung/dtc-infographic-production)，默认分支为 `main`

后续每次由 Codex 按 AGENTS.md 自动提交、推送并核对远端结果；用户无需手动归档或填写交接表

历史 SOP 依据：Evo 中的信息图交接讨论及 2026-11-14 DTC 爆款复刻分发会议，本目录保留实际执行所需文件，不依赖原电脑的 vault 路径
