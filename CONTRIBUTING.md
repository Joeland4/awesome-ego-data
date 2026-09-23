# Contributing

感谢贡献！请通过 PR 补充/修正数据集。

## 新增条目的要求

请在 `README.md` 对应分类下新增一行，并同步更新 `data/ego-datasets.csv`，字段包括：

| 字段 | 说明 |
|---|---|
| name | 数据集名称 |
| org | 发布机构/公司 |
| country | 国家/地区 |
| year | 发布年份 |
| scale | 规模（小时/轨迹/片段） |
| view | 视角：`mono` / `stereo` / `head+wrist` / `multi` |
| modalities | 模态（RGB/深度/手部/全身/触觉/IMU…） |
| access | `open` / `request` / `license` / `register` |
| link | **官方链接**（优先官网/GitHub/HuggingFace/ModelScope） |
| verified | 是否已核实官方来源（true/false） |

## 规则

1. **必须提供官方链接**，不接受仅新闻稿。
2. 优先收录 **Human Ego（第一人称人类）** 数据；纯机器人遥操数据请标注。
3. 未核实条目请在 `verified` 列标 `false`，并在 README 中标注 ⚠️。
4. 一个 PR 一个主题，描述中说明数据来源与核实方式。

## 本地检查

```bash
python -c "import csv;print(sum(1 for _ in open('data/ego-datasets.csv'))-1,'datasets')"
```
