<div align="center">

# 🎥 Awesome Human Egocentric (Ego) Data

**可下载 / 可申请的第一人称（Ego）人类数据集 —— 以真实数据仓库（HuggingFace / ModelScope）为准**
Verified open & requestable egocentric human datasets, with precise release dates

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: Apache-2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Updated](https://img.shields.io/badge/Updated-2026--09--23-blue.svg)](#)

</div>

---

## ⚠️ 核验标准

**只认能真正拿到数据的地方**：HuggingFace / ModelScope / 官方 GitHub release。仅有营销官网首页的条目不收录。

- `open` = HF 仓库公开，可直接 `hf download`
- `gated` = HF 仓库存在，需登录并同意条款后申请（`gated=auto` 自动通过 / `manual` 人工审核）
- `request` = 官网注册 / 签 DUA
- **日期** = HF 仓库创建日（`createdAt`，即数据上线日）或官方发布日期；精确到日
- **下载量** = HF 累计下载（2026-09-23 实测）

**核验**：`curl hf-mirror.com/api/datasets/<id>` 取 `createdAt/gated/downloads`；`/raw/main/README.md` 判 open/gated。

---

## 📊 总览（截至 2026-09-23）

| 指标 | 数量 |
|---|---|
| 收录（有真实数据仓库/明确申请入口） | **64** |
| └ HuggingFace 公开可直接下载 (`open`) | **35** |
| └ HuggingFace 需申请 (`gated`) | **14** |
| └ 官方 GitHub / 数据门户 | **12** |
| └ 官网申请 / DUA (`request`) | **3** |
| 其中**双目 / 立体 / 头+腕** | **5** |
| 已剔除（无数据仓库 / 仅营销） | 见文末 |

### 规模与质量速览

- **已解析小时数合计 ≈ 134,353 h（≈15.3 年）**，是下界（Gen-HumanEgo 1,800h 等未计入）。
- **规模被操作数据垄断**：manipulation/HOI 占 86% 时长；双目+VQA+世界模型合计 <1%。
- **质量**：按「规模/模态/标注/视角/开放度/采用度」6 维评分（0–100），最高仅 63.9（光轮 EgoSuite），说明**没有全能数据集**。
- 详见 **[docs/analysis.md](docs/analysis.md)**（含小时数、质量榜、综述分析、生态位）与 `data/quality-ranking.csv`。

---

## 📈 趋势与分类统计

### 1) 年度分布（按数据上线日）

```
2018  ▏ 1
2021  ▏ 1
2022  ▏ 2
2023  ▏ 3
2024  ▏ 9
2025  ▏ 9
2026  ███████████████████████████████████████ 39   ← 爆发年
```

### 2) 年度 × 访问类型

| 年份 | open | gated | request | 合计 |
|---|---|---|---|---|
| 2018 | 1 | 0 | 0 | 1 |
| 2021 | 1 | 0 | 0 | 1 |
| 2022 | 1 | 0 | 1 | 2 |
| 2023 | 3 | 0 | 0 | 3 |
| 2024 | 8 | 0 | 1 | 9 |
| 2025 | 5 | 4 | 0 | 9 |
| **2026** | **28** | **10** | **1** | **39** |

> 趋势：2026 年占总量 61%；且 **gated 从 2025 年才开始出现**（大厂开始收紧许可），2026 年 10 个 gated。

### 3) 分类分布

| 分类 | 数量 | 说明 |
|---|---|---|
| manipulation / HOI | 22 | 手-物交互、灵巧操作（最多） |
| VQA / 推理 | 7 | 视频问答 |
| general（通用语料） | 6 | Ego4D/Nymeria 等 |
| procedural（程序性） | 5 | 装配/烹饪/纠错 |
| 3D / scene | 5 | 场景图、3D 感知 |
| world-model | 4 | 世界模型预训练 |
| **stereo（双目）** | 4 | 立体采集 |
| memory / long-form | 4 | 长时记忆 |
| action（动作识别） | 4 | - |
| robot（非人类） | 2 | 机器人遥操 |
| detection | 1 | 目标检测 |

### 4) 国家 / 地区分布

| 国家 | 数量 |
|---|---|
| 未标注 | 24 |
| 美国 US | 22 |
| 中国 CN | 16 |
| 英国 UK | 2 |

> 中国 16 个中有 **12 个集中在 2026 年**，是增长最快的来源。

### 5) 下载量 Top 10（HF 实测）

| 数据集 | 机构 | 下载量 |
|---|---|---|
| Open-AoE | Ant Group | 498,169 |
| Ego-OSCAR (stereo-550) | fpvlabs | 234,370 |
| EgoDemo | 光轮智能 | 148,293 |
| EgoLife | EvolvingLMMs-Lab | 108,742 |
| AgiBotWorld-Beta | 智元机器人 | 102,134 |
| Ropedia Xperience-10M | Ropedia | 96,685 |
| Egocentric-10K | Build AI | 69,927 |
| Assembly101 | cvml-nus | 69,350 |
| Ego-1K | Meta | 52,679 |
| EgoPro | 光轮智能 | 38,710 |

---

## 1. HuggingFace 公开可直接下载 (`open`)

| 数据集 | 机构 | 日期 | 规模 | 视角 | 下载 | 仓库 | 许可 |
|---|---|---|---|---|---|---|---|
| **Gen-HumanEgo** | 简智机器人 GenRobot | **2026-09-12** | **1,800+ h** | 多目(6 摄头+手) | - | https://huggingface.co/datasets/genrobot2025/Gen-HumanEgo | CC-BY-SA-4.0 |
| Gen-EgoData | 简智机器人 GenRobot | 2026-03-14 | 500 / 4.23 h | 单目+SLAM | 545 | https://huggingface.co/datasets/genrobot2025/Gen-EgoData | CC-BY-SA-4.0 |
| Gen-EgoData | 京东 JoyAI | 2026-08-10 | 500 / 4.23 h | 单目+SLAM | 114 | https://huggingface.co/datasets/jdopensource/Gen-EgoData | CC-BY-SA-4.0 |
| **SynData** | 灵初智能 PsiBot | 2026-04-21 | 开源 1,000 h | 手部 | 13,557 | https://huggingface.co/datasets/PsiBotAI/SynData | CC-BY-4.0 |
| **WIYH** | 它石智航 TARS | 2026-03-25 | >10 万条 | 单目 | 12,066 | https://huggingface.co/datasets/tars-robotics/WIYH | CC-BY-NC-4.0 |
| **EgoViz-120** | humaidtech | 2026-08-28 | 120 h | **双目+双腕** | 174 | https://huggingface.co/datasets/humaidtech/EgoViz-120 | CC-BY-4.0 |
| **ego-stereo-cn-v1** | tatezhou | 2026-08-22 | <1K | **双目** | 338 | https://huggingface.co/datasets/tatezhou/ego-stereo-cn-v1 | CC-BY-NC-4.0 |
| ACE-Data-0 | ACE Robotics | 2026-09-08 | 150 h / 75K | 单目/外视角 | - | https://huggingface.co/datasets/ACERobotics/ACE-Data-0 | - |
| Open-AoE | Ant Group | 2026-07-07 | ~2,000 h | 单目 | 498,169 | https://huggingface.co/datasets/inclusionAI/OpenAoE-2000h | - |
| EgoExoLearn | OpenGVLab | 2024-08-07 | 120 h | ego+exo | 3,216 | https://huggingface.co/datasets/hyf015/EgoExoLearn | - |
| HoloAssist | Microsoft | 2025-06-25 | 166 h | 单目+深度 | 12,715 | https://huggingface.co/datasets/hyf015/holoassist | - |
| EgoLife | EvolvingLMMs-Lab | 2025-02-26 | 266–300 h | 多目 | 108,742 | https://huggingface.co/datasets/lmms-lab/EgoLife | - |
| AEA | Meta | 2024-09-13 | 143 seq | 多目 | 81 | https://huggingface.co/datasets/projectaria/aria-everyday-activities | - |
| ADT | Meta | 2024-08-27 | 200 seq | 多目 | 171 | https://huggingface.co/datasets/projectaria/aria-digital-twin | - |
| **HOT3D** | Meta | 2024-09-17 | 833 min | 多目(Quest3 立体) | 168 | https://huggingface.co/datasets/projectaria/hot3d | - |
| **Nymeria** | Meta | 2024-09-19 | ~1,100 h | 多目 | 282 | https://huggingface.co/datasets/projectaria/Nymeria | - |
| Assembly101 | cvml-nus | 2026-05-13 | 513 h | 多目 | 69,350 | https://huggingface.co/datasets/cvml-nus/assembly101 | - |
| EgoTouch | - | 2026-05-24 | 1,891 回合 | 单目 | 6,710 | https://huggingface.co/datasets/zhenyuxie-zhzh/EgoTouch_hdf5 | - |
| EgoSPT | - | 2026-05-14 | 11,515 回合 | 单目 | 36 | https://huggingface.co/datasets/JackYFL233/EgoSPT | - |
| EgoMonth | - | 2026-05-03 | 301 h | 单目 | 261 | https://huggingface.co/datasets/anonymous-egomonth/egomonth-dataset | - |
| EgoMemReason | - | 2026-05-11 | 500 MCQ | 单目 | 118 | https://huggingface.co/datasets/Ted412/EgoMemReason | - |
| SuperMemory-VQA | OSU | 2026-04-24 | 52.9 h | 单目 | 3,378 | https://huggingface.co/datasets/OSU-AIoT-MLSys-Lab/SuperMemory-VQA | - |
| Causal-Plan-1M | THUSI-Lab | 2026-05-04 | 1M QA | 单目 | 747 | https://huggingface.co/datasets/anonymous-causal-plan/Causal_Plan | - |
| EgoServe | - | 2026-06-27 | 3K+ | 单目 | 181 | https://huggingface.co/datasets/SitongGong/EgoServe | - |
| EgoCoT-Bench | - | 2026-06-02 | 351 视频 | 单目 | 89 | https://huggingface.co/datasets/DStardust/EgoCoT-Bench | - |
| Ego2Web | - | 2026-03-22 | 500 对 | 单目 | 56 | https://huggingface.co/datasets/Shoubin/Ego2Web | - |
| GameplayQA | HATS-ICT | 2026-03-24 | ~2.4K QA | 合成 | 1,000 | https://huggingface.co/datasets/wangyz1999/GameplayQA | - |
| Ego-METAS | - | 2026-05-02 | 100 h | 单目 | 506 | https://huggingface.co/datasets/Ego-METAS/Ego-METAS | - |
| EgoTactile | - | 2026-01-25 | 768 片段 | 单目 | 719 | https://huggingface.co/datasets/HustleHard/EgoTactile | - |
| epic-contact | - | 2026-06-27 | 2.3K 片段 | 单目 | 6,035 | https://huggingface.co/datasets/Sid2697/epic-contact | - |
| sg-ego | - | 2026-06-29 | 3.8M 图 | 单目 | 173 | https://huggingface.co/datasets/francescapistilli/sg-ego | - |
| hrdexdb | - | 2026-04-03 | 1.4K | 单目 | 104 | https://huggingface.co/datasets/hahahataeyun/hrdexdb | - |
| interpet4d | - | 2026-06-27 | 6.8M 帧 | 多目 | 2,025 | https://huggingface.co/datasets/ohicarip/interpet4d | - |
| OVO-S-Bench | - | 2026-08-15 | 348 视频 | 单目 | 27 | https://huggingface.co/datasets/kfkas/ovo-s-bench-ego4d-benchmark | - |
| EgoFun3D | SFU | 2026-03-31 | 271 视频 | 单目 | 185 | https://huggingface.co/datasets/3dlg-hcvc/EgoFun3D | - |

## 2. 需申请 (`gated` / `request`)

| 数据集 | 机构 | 日期 | 规模 | 视角 | 下载 | 入口 | 类型 |
|---|---|---|---|---|---|---|---|
| 10Kh RealOmni-Open | 简智机器人 GenRobot | 2026-01-06 | >10,000 h | 单目 | - | https://huggingface.co/datasets/genrobot2025/10Kh-RealOmin-OpenData | gated |
| EgoSuite-Open100K | 光轮智能 Lightwheel | 2026-08-20 | 100,000 h | 头+腕 | - | https://egosuite100k.lightwheel.ai/ | request |
| EgoDemo | 光轮智能 Lightwheel | 2026-08-07 | - | 头+腕 | 148,293 | https://huggingface.co/datasets/LightwheelAI/EgoDemo | gated(manual) |
| EgoPro | 光轮智能 Lightwheel | 2026-08-07 | - | 头+腕 | 38,710 | https://huggingface.co/datasets/LightwheelAI/EgoPro | gated(manual) |
| **Ego-OSCAR (stereo-550)** | fpvlabs | 2026-07-30 | ~550 h/相机 | **双目+IMU** | 234,370 | https://huggingface.co/datasets/fpvlabs/stereo-550 | gated(auto) |
| AgiBotWorld-Beta | 智元机器人 AgiBot | 2025-02-11 | 100 万轨迹 | 机器人 | 102,134 | https://huggingface.co/datasets/agibot-world/AgiBotWorld-Beta | gated(auto) |
| Ego-1K | Meta | 2026-01-29 | ~1K take | 多目 | 52,679 | https://huggingface.co/datasets/facebook/ego-1k | gated |
| EgoProactive / Pro²Bench | Meta | 2026-05-15 | 700 录制 | 单目 | 2,894 | https://huggingface.co/datasets/facebook/wearable-ai | gated(auto) |
| HA-Ego (ego500) | Human Archive | 2026-08-07 | 500+ | 头+腕 | 26 | https://huggingface.co/datasets/humanarchive/ego500 | gated(manual) |
| Egocentric-10K | Build AI | 2025-11-09 | 10,000 h | 单目 | 69,927 | https://huggingface.co/datasets/builddotai/Egocentric-10K | gated(auto) |
| PRISM-100K | DreamVu | 2026-03-22 | 270K | 单目 | 310 | https://huggingface.co/datasets/DreamVu/PRISM-100K | gated(auto) |
| SABER-10K | DreamVu | 2026-04-02 | 100 h | 单目 | 20 | https://huggingface.co/datasets/DreamVu/SABER-10K | gated(auto) |
| EgoExo-Fitness | iSEE Lab | 2025-02-11 | 32 h | ego+exo | 247 | https://huggingface.co/datasets/Lymann/EgoExo-Fitness | gated(auto) |
| EgoCross | - | 2025-10-16 | 798 片段 | 单目 | 32 | https://huggingface.co/datasets/myuniverse/EgoCross | gated(auto) |
| Ropedia Xperience-10M | Ropedia | 2026-03-11 | 10M | 多目 | 96,685 | https://huggingface.co/datasets/ropedia-ai/xperience-10m | gated(manual) |
| Ego4D | Meta AI | 2022-06-01 | 3,670 h | 单目 | - | https://ego4d-data.org | request/DUA |
| Ego-Exo4D | Meta AI | 2024-06-01 | 1,286 h | 多目+exo | - | https://ego-exo4d-data.org | request/DUA |

## 3. 官方 GitHub / 数据门户（可直接下载）

| 数据集 | 机构 | 日期 | 规模 | 视角 | 链接 |
|---|---|---|---|---|---|
| EPIC-KITCHENS-100 | Univ. Bristol | 2021-01-01 | 100 h | 单目 | https://epic-kitchens.github.io/ |
| HD-EPIC | Univ. Bristol | 2025-02-06 | 41 h | 单目(Aria) | https://hd-epic.github.io/ |
| Charades-Ego | AI2 / CMU | 2018-04-25 | ego/exo 配对 | 单目 | https://prior.allenai.org/projects/charades-ego |
| HOI4D | 清华等 | 2022-06-01 | 2.4M 帧 | 单目 RGB-D | https://hoi4d.github.io/ |
| EgoObjects | Meta | 2023-06-01 | 9.2K+ 视频 | 单目 | https://github.com/facebookresearch/EgoObjects |
| EgoDex | Apple | 2025-05-16 | 829 h | 单目(Vision Pro) | https://github.com/apple/ml-egodex |
| Open X-Embodiment | Google DeepMind + 21 | 2023-10-13 | 100 万+ 轨迹 | 混合 | https://robotics-transformer-x.github.io |
| SANPO | Google | 2023-09-22 | 701 段 | **双目** | https://google-research-datasets.github.io/sanpo_dataset/ |
| EgoMimic | Georgia Tech + Stanford | 2024-10-30 | 小时级 | 头+腕 | https://egomimic.github.io/ |
| UMI | Stanford 等 | 2024-02-06 | 演示级 | 腕部单目 | https://umi-gripper.github.io/ |
| DexUMI | Stanford/Columbia/NVIDIA | 2025-05-27 | 演示级 | 腕部单目 | https://dex-umi.github.io/ |
| Open-TeleVision | UCSD/MIT | 2024-07-01 | 演示 | VR 双目 | https://robot-tv.github.io/ |

## 4. 双目 / 立体 / 头+腕（重点）

| 数据集 | 机构 | 日期 | 立体类型 | 访问 | 链接 |
|---|---|---|---|---|---|
| EgoViz-120 | humaidtech | 2026-08-28 | 双目+双腕 | open | https://huggingface.co/datasets/humaidtech/EgoViz-120 |
| ego-stereo-cn-v1 | tatezhou | 2026-08-22 | 双目 LeRobot | open | https://huggingface.co/datasets/tatezhou/ego-stereo-cn-v1 |
| Ego-OSCAR (stereo-550) | fpvlabs | 2026-07-30 | 全局快门立体+IMU | gated | https://huggingface.co/datasets/fpvlabs/stereo-550 |
| HOT3D | Meta | 2024-09-17 | 多目(Quest3 立体) | open | https://huggingface.co/datasets/projectaria/hot3d |
| Gen-HumanEgo | 简智 GenRobot | 2026-09-12 | 6 摄(头+手) | open | https://huggingface.co/datasets/genrobot2025/Gen-HumanEgo |
| SANPO | Google | 2023-09-22 | 双目行车 | open | https://google-research-datasets.github.io/sanpo_dataset/ |
| UnrealEgo | MPI + Keio | 2022-06 | 双目鱼眼 | open | https://4dqv.mpi-inf.mpg.de/UnrealEgo/ |
| EgoCap | ETH Zurich | 2016-09 | 双鱼眼 | open | https://arxiv.org/abs/1609.07306 |

## 5. 已剔除 / 降级（无真实数据仓库或仅营销）

| 条目 | 原因 |
|---|---|
| 京东独立 EgoLive | 实际数据以 `jdopensource/Gen-EgoData` 发布 |
| Aligned DexWorld（跨维）、XRZero-G0（自变量）、ZODA（诺亦腾）、LARYBench（美团）、RoVid-X（字节） | 仅新闻稿，无数据仓库 |
| RoboMIND | 未核实到公开 HF/ModelScope 直链 |
| StereoEgo、EgoDepth | 无任何可信出处，**已删除** |

---

## 贡献

见 [CONTRIBUTING.md](CONTRIBUTING.md)。**必须提供可下载/可申请的数据仓库链接（HF/ModelScope/GitHub release）**，不接受纯官网首页。

## License

[Apache-2.0](LICENSE)。数据版权归各自发布方所有。
