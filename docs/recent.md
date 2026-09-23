# 最近文章（滚动更新）— 检索至 2026-09-23

> 按 arXiv 提交日期倒序。用于综述的「最新进展」章节与趋势判断。
> 检索方式：arXiv 高级检索，`sortBy=submittedDate&sortOrder=descending`。

## A. 最新综述 / 评论（Review）

> ⚠️ 分类提示：`2609.19793` 与 `2608.24877` 是**系统/硬件综述（智能眼镜）**，**不是 Ego 数据综述**；真正的 Ego 数据综述是 `2607.24744`、`2606.00054`、`2604.27621`、`2503.15275`、`2608.18671`。

| 日期 | arXiv | 标题 | 类型 |
|---|---|---|---|
| 2026-09-17 | 2609.19793 | AI Smart Glasses for Wearable Intelligence | 系统/硬件综述（非数据） |
| 2026-08-25 | 2608.24877 | From Seeing to Acting: Smart Glasses as First-Person Intelligence Platforms | 系统/硬件综述（非数据） |
| 2026-08-19 | 2608.18671 | Vision-Language Models for Egocentric Video: From HOI to Embodied AI | Ego-VLM 综述（含数据） |
| 2026-08-08 | 2607.24744 | Data Pyramid for Embodied Manipulation: A Survey | **具身数据中心综述** |
| 2026-05-12 | 2605.12090 | World Action Models: The Next Frontier in Embodied AI | 模型综述 |
| 2026-04-08 | 2604.27621 | Robot Learning from Human Videos: A Survey | 人类视频→机器人综述 |
| 2026-03-xx | 2606.00054 | From Human Videos to Robot Manipulation: Scalable VLA with Human-Centric Data | 人类数据→VLA 综述 |

> **观察**：2026 下半年综述主题明显转向「智能眼镜 / 第一人称平台」和「具身数据配方」——数据问题被正式当作研究主题。

## B. 最新数据集 / 基准（Dataset / Benchmark）

| 日期 | arXiv | 名称 | 要点 |
|---|---|---|---|
| 2026-09-17 | 2609.19881 | **BinoGen** | **大规模 ego 双目合成数据**（embodiment-aware；环境+观察者建模） |
| 2026-09-17 | 2609.19876 | SlugTrails | ego 楼层定位基准 |
| 2026-09-15 | 2609.17189 | EventEgoHands++ | 事件相机 ego 3D 手部网格（真实数据） |
| 2026-09-15 | 2609.16610 | EgoPathBench | VLM 零样本 ego 路径决策 |
| 2026-09-08 | 2609.09023 | **DYAD** | 共处人类协助的多模态数据集 |
| 2026-09-xx | 2609.17688 | CapMem | ego 视频字幕式情景记忆基准 |
| 2026-09-21 | 2609.24778 | **H2RBench** | 人→机器人迁移的 real-to-sim 基准 |

## C. 最新方法（使用 Ego 数据做训练/增益证据）

| 日期 | arXiv | 名称 | 与数据的关系 |
|---|---|---|---|
| 2026-09-22 | 2609.24411 | **Zeva-Ego** | ego 视频 mid-training + 因果学习做机器人操作（增益证据） |
| 2026-09-21 | 2609.21461 | **AtomEgo** | ego-robot 融合预训练（如何用 ego 数据进具身基座） |
| 2026-09-21 | 2609.25627 | MachEmbodied-U0 | 统一理解+生成 |
| 2026-09-20 | 2609.23755 | EgoWild2Dex | 从野外人类经验学灵巧操作 |
| 2026-09-08 | 2609.04958 | MINT | 世界空间相机+手部运动估计（ego pipeline） |
| 2026-09-08 | 2609.08636 | From Where to How | 连续 4D 交互预测 |
| 2026-09-17 | 2609.20414 | TouchSight | ego 视频触觉预测 |

## D. 对综述的意义

1. **数据问题已上升为主题**：2607.24744（Data Pyramid）、2608.24877（第一人称平台）把数据/系统当核心——但**仍无逐数据集审计**，我们的定位更清晰。
2. **双目/立体重新升温**：BinoGen（2609.19881）专门做 ego 双目——印证我们「双目被忽视但重要」的判断。
3. **增益证据开始出现**：Zeva-Ego、AtomEgo、EgoWild2Dex 都在报「ego 数据→机器人增益」，可作为 RQ4 的素材。
4. **趋势**：2026-09 几乎每周都有 ego 数据/方法论文——**living review 是刚需**。

## 检索覆盖说明

- 已按提交日期倒序检索关键词：`egocentric`、`egocentric dataset`、`egocentric survey`、`human data embodied`、`egocentric world model` 等。
- 最新覆盖到 **2026-09-22**（2609.25627 / 2609.24411）。
- 局限：arXiv 为主；CVPR/ICCV 等会议论文集、公司技术博客需另行补充。
