---
name: experiment-protocol-writer
description: Create, research, rewrite, expand, and format Chinese experimental protocols in the user's fixed research protocol style. Use when Codex is asked to 整理实验 protocol, 输入简单实验步骤后查找资料并补充完善, 生成或润色实验方案, convert notes/manuals into a standardized protocol, or preserve the logic/style from 01.DNA提取.docx, including purpose, principle, parameter rationale, reagents/instruments, detailed steps with explanations, troubleshooting, notes, and actual-parameter records.
---

# Experiment Protocol Writer

## Core Workflow

1. Identify the experiment name, sample type, source notes/manuals, required output format, and any user-specific parameters.
2. If the user provides only simple steps or incomplete notes, treat them as the experimental backbone and research reliable sources before expanding.
3. Preserve user-provided factual parameters exactly. If a value is missing or uncertain, write `【待确认】` instead of inventing it.
4. Convert source material into the fixed protocol structure below.
5. Add rationale for parameters and steps, but keep the tone objective, concise, and suitable for a lab notebook/protocol document.
6. If the user asks for Word/DOCX styling or "my style", read `references/protocol-style-guide.md` and apply those layout rules.
7. Validate that all eight required modules are present before finishing.

## Research and Expansion Workflow

Use this when the user gives a short protocol, rough steps, reagent list, kit name, assay name, or a partially written protocol.

1. Extract the known facts:
   - experiment name and objective
   - sample type/species/tissue/cell line
   - kit, reagent, instrument, or platform names
   - volumes, temperatures, times, speeds, concentrations, storage conditions, and detection method
   - user-specific annotations or exceptions
2. Search for supporting information before completing missing sections. Prioritize sources in this order:
   - official kit handbooks, reagent manuals, instrument manuals, safety datasheets, and vendor protocols
   - peer-reviewed methods papers, review articles, or protocol repositories
   - reputable university/core facility protocols
   - general web pages only when better sources are unavailable
3. Use sources to supplement:
   - `实验目的`: what the experiment is meant to obtain, verify, quantify, or prepare for downstream use
   - `实验原理`: the biochemical/physical/molecular principle behind the method
   - `关键参数设定依据`: why each important value is used and how changing it affects yield, purity, specificity, sensitivity, or reproducibility
   - `试剂与仪器`: complete missing reagents, consumables, instruments, and per-reaction amounts
   - `具体操作步骤`: organize rough steps into stages and add `目的：` or `说明：` after each stage
   - `结果判断与原因分析`: define expected results, acceptable ranges, abnormal patterns, and troubleshooting
   - `注意事项`: add safety, contamination, reagent preparation, timing, storage, and measurement caveats
   - `本次实验实际参数记录`: choose record fields that best support later复盘 and parameter optimization
4. Keep user-provided steps as the primary protocol when they conflict with generic sources, but flag serious conflicts with official manuals, safety requirements, or biological plausibility.
5. Mark uncertain additions as `【待确认】`; do not fabricate exact values, catalog numbers, incubation times, or acceptance thresholds.
6. In the assistant response, briefly list the key sources used. In the protocol body, include citations only if the user asks for them or if source traceability is required.
7. If online access is unavailable, state that limitation and complete only from provided notes plus general knowledge, marking source-dependent values as `【待确认】`.

## Required Structure

Use this order and numbering:

1. `实验目的`
2. `实验原理`
   - Include the core method principle.
   - Include a table or subsection explaining key reagents/materials and their roles when relevant.
   - Include detection or quality-control principles when the experiment has measurable outputs.
3. `关键参数设定依据`
   - Explain why important sample amount, temperature, time, volume, speed, mixing, incubation, wash, elution, or detection parameters are chosen.
   - Tie each parameter to yield, purity, stability, sensitivity, specificity, or downstream compatibility.
4. `试剂与仪器`
   - Add `4.1 每个反应的主要试剂与用量` or a context-appropriate equivalent.
   - Add `4.2 主要仪器`.
5. `具体操作步骤`
   - Split steps into logical stages such as sample preparation, reaction setup, incubation, washing, detection, preservation, or cleanup.
   - Number action steps as `1）`, `2）`, `3）`.
   - After each stage, add one italic-style explanatory line beginning with `目的：` or `说明：`.
   - Explain what the step accomplishes and what can go wrong if it is not done well.
6. `结果判断与原因分析`
   - Include success criteria.
   - Include a common-problems table with `问题` and `可能原因及建议`.
   - Add protocol-specific interpretation notes when needed.
7. `注意事项`
   - Use short numbered notes, each beginning with `1）`, `2）`, etc.
   - Focus on safety, reagent preparation, timing, mixing, contamination control, storage, and measurement caveats.
8. `本次实验实际参数记录`
   - Add a fillable record table for the variables most likely to affect reproducibility.
   - Prefer paired columns: `项目 | 记录 | 项目 | 记录`.

Begin the document with:

- A centered title: `实验名称（方法/试剂盒/平台，可选）`
- A one-paragraph scope line beginning with `适用样本：` when sample context is known.

## Writing Rules

- Write in Chinese unless the user requests another language.
- Use direct protocol prose, not promotional or tutorial copy.
- Keep official kit/manual terminology intact, including buffer names and instrument names.
- Use consistent unit formatting: `56 ℃`, `180 μl`, `1 min`, `8000 rpm`, `pH 8.5`.
- Do not silently convert `rpm` to `× g` unless rotor information is available.
- Preserve user annotations such as bracketed exceptions or lab-specific notes, but place them where they affect the actual step.
- If the source protocol conflicts with a vendor manual or safety requirement, surface the conflict instead of resolving it silently.

## Output Checklist

Before finalizing, confirm:

- The document has the title, scope line, and all eight numbered modules.
- If the input was brief, reliable sources were checked or the inability to search was stated.
- Section 3 explains parameter choices rather than merely repeating parameters.
- Section 5 has staged steps plus `目的：` or `说明：` lines.
- Section 6 includes both interpretation criteria and troubleshooting.
- Section 8 captures actual-run parameters for later复盘.
- Missing values are marked `【待确认】`.
- Styled DOCX outputs follow `references/protocol-style-guide.md`.
