# Protocol Style Guide

This guide captures the visual style extracted from `01.DNA提取.docx`. Use it when the user asks for a Word/DOCX protocol, the user's protocol style, or preservation of font/color/table formatting.

## Page

- Page size: Letter, 8.5 in × 11 in (`12240 × 15840` twips).
- Margins: top/right/left about 0.95 in, bottom about 0.87 in (`1361/1361/1361/1247` twips).
- Main East Asian font: `楷体`.
- Main Latin font: `Times New Roman`.
- Main text color: black unless specified.

## Paragraph Styles

Use direct formatting if no reusable Word styles are available.

| Element | Font | Size | Color | Weight/Style | Alignment | Spacing |
|---|---:|---:|---|---|---|---|
| Document title | Times New Roman / 楷体 | 16 pt | `#1E4F81` | bold | center | line 264 twips, auto |
| Scope line beginning `适用样本：` | Times New Roman / 楷体 | 12 pt | black | regular | left | after 160 twips, line 300 twips auto |
| Level 1 section heading, e.g. `1. 实验目的` | Times New Roman / 楷体 | 15 pt | `#1E4F81` | bold | left | before 80, after 120, line 264 twips auto |
| Level 2 heading, e.g. `2.1 ...` | Times New Roman / 楷体 | 14 pt | `#1E4F81` | bold | left | before 80, after 80, line 264 twips auto |
| Explanatory body paragraph | Times New Roman / 楷体 | 12 pt | black | regular | left | after 120, line 317 twips auto |
| Procedure action line | Times New Roman / 楷体 | 12 pt | black | regular | left | after 60, line 293 twips auto |
| Step rationale line beginning `目的：` or `说明：` | Times New Roman / 楷体 | 12 pt | `#646464` | italic | left | after 100, line 283 twips auto |
| Notes in `7. 注意事项` | Times New Roman / 楷体 | 11.5 pt | black | regular | left | after 40 twips |
| Text before the record table | Times New Roman / 楷体 | 12 pt | black | regular | left | after 80, line 288 twips auto |

## Tables

Use the same table treatment for reagent tables, troubleshooting tables, and actual-parameter record tables.

- Header row fill: `#5B87B8`.
- Header text: white `#FFFFFF`, bold, centered.
- Border: single line, about 0.75 pt, color `#B7C7D9`.
- Alternating body row fill: `#F5F8FC` on the first body row and every other body row after that; leave intervening rows unshaded.
- Table font: Times New Roman / 楷体.
- Reagent/principle/troubleshooting tables: 10.5 pt.
- Actual-parameter record table: 10 pt.
- Center short categorical columns such as `组分`, `主要作用`, `用量`, `问题`, and `项目`.
- Left-align longer explanatory columns such as `原理说明`, `备注`, `可能原因及建议`, and blank `记录` cells.

## Content Patterns

### Step Block

```text
5.x 阶段名称
1）具体操作。
2）具体操作。
说明：解释本阶段的作用、关键风险，以及参数不足或操作不充分时的影响。
```

Use `目的：` for sample-preparation or design-intent explanations; use `说明：` for mechanistic or operational explanations.

### Key Reagent Table

```text
组分 | 主要作用 | 原理说明
```

### Reagent-Amount Table

```text
组分 | 用量 | 备注
```

### Troubleshooting Table

```text
问题 | 可能原因及建议
```

### Actual-Parameter Record Table

Use paired fields:

```text
项目 | 记录 | 项目 | 记录
样本类型 |  | 样本数量 |
样本保存条件 |  | 关键前处理 |
关键温度 |  | 关键时间 |
是否成功 |  | 后续用途 |
异常情况 |  | 处理措施 |
```

Customize the field names to the experiment, but keep the paired `项目/记录` structure.
