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

1. **必须提供可下载/可申请的数据仓库链接**：HuggingFace / ModelScope / OpenDataLab / 官方 GitHub release。
   **不接受纯营销官网首页**，除非该数据集确实只有官网申请入口。
2. 明确标注访问类型：`open`（HF 公开可 clone）/ `gated`（HF 需申请）/ `request`（官网/DUA）。
3. 优先收录 **Human Ego（第一人称人类）** 数据；纯机器人遥操数据请标注。
4. 未核实条目请标 `⚠️` 并在描述中说明；无法找到数据仓库的条目请勿提交。
5. 一个 PR 一个主题，描述中附核验方式（例如 `curl hf-mirror.com/api/datasets/<id>`）。

## 本地检查

```bash
python -c "import csv;print(sum(1 for _ in open('data/ego-datasets.csv'))-1,'datasets')"
```
