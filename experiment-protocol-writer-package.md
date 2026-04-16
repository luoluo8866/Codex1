# Experiment Protocol Writer Skill

This repository includes a packaged Codex skill for expanding brief experimental steps into a complete Chinese experimental protocol.

## What It Does

- Researches reliable sources when the input protocol is brief or incomplete.
- Completes the fixed protocol structure:
  1. 实验目的
  2. 实验原理
  3. 关键参数设定依据
  4. 试剂与仪器
  5. 具体操作步骤，包括说明
  6. 结果判断与原因分析
  7. 注意事项
  8. 本次实验实际参数记录
- Preserves the Word style extracted from `01.DNA提取.docx`, including fonts, heading colors, table colors, and spacing guidance.

## Install

Copy the `experiment-protocol-writer` folder into your Codex skills directory:

```text
C:\Users\12398\.codex\skills\experiment-protocol-writer
```

## Use

Invoke it in Codex with:

```text
使用 $experiment-protocol-writer，把下面的简单实验步骤查资料补全，并整理成我的 protocol 样式。
```

Then provide the experiment name, sample type, known steps, reagents, and expected output format.
