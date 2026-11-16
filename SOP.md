---
type: sop
title: DTC 信息图制作 SOP
updated: 2026-11-15
---

# DTC 信息图制作 SOP

**给慧慧的执行版｜保存一个 Codex 会话，持续完成生图与修改**

**流程：打开生产文件夹 → 发提示词并保存会话 → 找内容、保存 MD → 同一会话生图 → 检查别的品牌信息 → Codex 自动整理并同步 Git**

## 01 · 在 Codex 打开生产文件夹

打开桌面的 `DTC信息图生产` 文件夹，让 Codex 按 [[AGENTS|AGENTS.md]] 工作，文件结构已经搭好

```text
DTC信息图生产/
├── AGENTS.md                 自动保存、整理与 Git 同步规则
├── README.md
├── SOP.md / SOP.html
├── prompts/infographic.md    制图提示词
├── 输入/<日期-主题>/          原始 MD 与相关附件
├── 输出/<日期-主题>/          成图、总结、使用提示词、任务记录
└── 示例/                     版式参考
```

每个任务的输入、输出由 Codex 自动保存到同名目录，不需要慧慧手动建文件夹或填写交接表

## 02 · 找到值得做成信息图的内容

在 Twitter 搜集过程中发现好文章、攻略或 post，先读内容，判断是否与 DTC agency、DTC 从业者、广告制作或 AI UGC 相关，有值得提炼的真实干货就可以使用

六张卡片来自当前提示词的“两列三行”版式，供 Codex 组织内容；选材按内容价值判断，原文可以包含任意数量的步骤

## 03 · 用 Obsidian Web Clipper 保存 MD

在源页面使用 **Obsidian Web Clipper** 把文章或 post 保存为 MD

插件设置入口：`chrome-extension://cnjifjpddelmedmihgijeibhnjfabmlf/settings.html?section=general`

将保存好的 MD 发到生产会话即可，Codex 按 AGENTS.md 自动保存到 `输入/<日期-主题>/`，不再手动整理到其他素材目录

## 04 · 先发提示词，保存并持续使用同一会话

### 第一次建立生产会话

1. 在已打开生产文件夹的 Codex 对话中，发送 [[prompts/infographic|完整制图提示词]]
2. 保存这个会话，后续所有生图与修改都在这里完成
3. Codex 根据 AGENTS.md 保存并整理相关输入、提示词和输出

### 后续每次生图

把源 MD 发到这个会话，并告诉 Codex 本张的 keywords

```text
请用这份 MD 生成信息图，keywords 是 <本张领取关键词>
按 AGENTS.md 保存和整理所有相关内容
图片生成后，输出一句话总结「这张图帮谁解决什么问题」
```

Codex 按当前提示词生成英文图片，将 keywords 填入图底部的 `Comment [XXX] to get the playbook`，并在图片生成后输出一句话总结

## 05 · 检查是否混入别的品牌信息

- [ ] 图片里有没有无关品牌的 Logo、水印、账号、网址、导航或原模板残留文字

发现后直接在同一会话指出，让 Codex 修改并保存新版本

```text
这张图的 <具体位置> 有别的品牌信息：<具体内容>
请去掉，并保存修改后的图片
```

内容本身需要提及的工具／模型名称，以及明确要求保留的来源署名，按实际内容保留

## 06 · Codex 自动保存、整理并同步 Git

根据 AGENTS.md，Codex 自动完成这些动作

1. 将原始 MD 与相关附件保存到 `输入/<日期-主题>/`
2. 将图片、生成后的一句话总结、实际使用提示词与任务记录保存到 `输出/<日期-主题>/`
3. 有修改时在同一任务中保留版本，更新当前成图
4. 提交本任务相关文件到 Git，推送后核对目标仓库结果
5. 在对话里返回图片、一句话总结、保存位置和 Git 同步结果

**不需要再手动保存成组素材或另做交接归档，悦己直接从同步后的 Git 获取文件**

当前桌面文件夹的公开 Git 远端为 `https://github.com/cheercheung/dtc-infographic-production`，默认分支为 `main`，后续按上述流程自动同步

## 07 · 版式示例

[[示例/ugc-team-4x5-en.png|Build a UGC Team · 4:5 英文成图]]

参考这张图的版式，新图的内容和 keywords 来自当次提供的 MD 与会话说明
