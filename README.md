<div align="center">

# 🎥 Awesome Human Egocentric (Ego) Data

**可下载 / 可申请的第一人称（Ego）人类数据集 —— 以真实数据仓库（HuggingFace / ModelScope）为准**
Open & requestable egocentric human datasets — verified against real data repositories

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: Apache-2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Updated](https://img.shields.io/badge/Updated-2026--09--23-blue.svg)](#)

</div>

---

## ⚠️ 核验标准（重要）

本清单**只认能真正拿到数据的地方**：HuggingFace / ModelScope / OpenDataLab 数据仓库，或官方 GitHub release。
**不再收录仅有营销官网首页的条目。**

- `open` = HF 仓库公开，`git clone` / `hf download` 可直接拿数据（已用 raw README 实测）
- `gated` = HF 仓库存在但需登录并同意条款后申请（`huggingface.co/datasets/...` 显示 Request access）
- `request` = 需官网注册 / 签署 DUA
- `✗` = 仅论文/仅模型，**未发现公开数据仓库**（已从主表移除，见文末）

**核验方法**：`curl hf-mirror.com/api/datasets/<id>` 判存在；`/raw/main/README.md` 判 open/gated；返回 "Access to dataset ... restricted" 即 gated。

---

## 📊 统计（截至 2026-09-23）

| 指标 | 数量 |
|---|---|
| 收录（有真实数据仓库/明确申请入口） | **70** |
| HuggingFace 公开可直接下载 (`open`) | **40** |
| HuggingFace 需申请 (`gated`) | **16** |
| 官网申请 / DUA (`request`) | **4** |
| 官方 GitHub / 数据门户（可下载） | **10** |
| 其中**双目 / 立体 / 头+腕** | **5** |
| 已剔除（无数据仓库 / 仅营销） | 见文末 |

---

## 1. 公司 / 机构 —— 公开可直接下载 (`open`，HuggingFace)

| 数据集 | 机构 | 年份 | 规模 | 视角 | 数据仓库（官方） | 许可 |
|---|---|---|---|---|---|---|
| **Gen-HumanEgo** | 简智机器人 GenRobot | 2026 | **1,800+ h**，6 摄 DAS-Ego | 多目(头+手) | https://huggingface.co/datasets/genrobot2025/Gen-HumanEgo | CC-BY-SA-4.0 |
| Gen-EgoData | 简智机器人 GenRobot | 2026 | 500 样本 / 4.23 h | 单目+SLAM | https://huggingface.co/datasets/genrobot2025/Gen-EgoData | CC-BY-SA-4.0 |
| Gen-EgoData | 京东 JoyAI | 2026 | 500 样本 / 4.23 h | 单目+SLAM | https://huggingface.co/datasets/jdopensource/Gen-EgoData | CC-BY-SA-4.0 |
| **SynData** | 灵初智能 PsiBot | 2026 | 开源 1,000 h | 手部/单目 | https://huggingface.co/datasets/PsiBotAI/SynData | CC-BY-4.0 |
| **WIYH** | 它石智航 TARS | 2025 | >10 万条操作视频 | 单目 | https://huggingface.co/datasets/tars-robotics/WIYH | CC-BY-NC-4.0 |
| **EgoViz-120** | humaidtech | 2026 | 120 h | **双目+双腕** | https://huggingface.co/datasets/humaidtech/EgoViz-120 | CC-BY-4.0 |
| **ego-stereo-cn-v1** | tatezhou | 2026 | <1K 段 | **双目 LeRobot** | https://huggingface.co/datasets/tatezhou/ego-stereo-cn-v1 | CC-BY-NC-4.0 |
| Open-AoE | Ant Group | 2026 | ~2,000 h | 单目 | https://huggingface.co/datasets/inclusionAI/OpenAoE-2000h | - |
| ACE-Data-0 | ACE Robotics | 2026 | 150 h / 75K 回合 | 单目/外视角 | https://huggingface.co/datasets/ACERobotics/ACE-Data-0 | - |
| EgoExoLearn | OpenGVLab (上海 AI Lab) | 2024 | 120 h | ego+exo | https://huggingface.co/datasets/hyf015/EgoExoLearn | - |
| HoloAssist | Microsoft | 2023 | 166 h | 单目+深度 | https://huggingface.co/datasets/hyf015/holoassist | - |
| EgoLife | EvolvingLMMs-Lab | 2025 | 266–300 h | 多目(Aria) | https://huggingface.co/datasets/lmms-lab/EgoLife | - |
| AEA | Meta (Project Aria) | 2024 | 143 seq | 多目 | https://huggingface.co/datasets/projectaria/aria-everyday-activities | - |
| ADT | Meta | 2023 | 200 seq | 多目 | https://huggingface.co/datasets/projectaria/aria-digital-twin | - |
| **HOT3D** | Meta | 2024 | 833 min / 3.7M 图 | 多目(Quest3 立体) | https://huggingface.co/datasets/projectaria/hot3d | - |
| **Nymeria** | Meta | 2024 | ~1,100 h / 264 人 | 多目(Aria+Quest3) | https://huggingface.co/datasets/projectaria/Nymeria | - |
| Assembly101 | cvml-nus | 2022 | 513 h 多视角 | 多目 | https://huggingface.co/datasets/cvml-nus/assembly101 | - |
| EgoTouch | - | 2026 | 1,891 回合 | 单目 | https://huggingface.co/datasets/zhenyuxie-zhzh/EgoTouch_hdf5 | - |
| EgoSPT | - | 2026 | 11,515 回合 | 单目 | https://huggingface.co/datasets/JackYFL233/EgoSPT | - |
| EgoMonth | - | 2026 | 301 h / 1,443 QA | 单目 | https://huggingface.co/datasets/anonymous-egomonth/egomonth-dataset | - |
| EgoMemReason | - | 2026 | 500 MCQ | 单目 | https://huggingface.co/datasets/Ted412/EgoMemReason | - |
| SuperMemory-VQA | OSU | 2026 | 52.9 h / 4,853 QA | 单目 | https://huggingface.co/datasets/OSU-AIoT-MLSys-Lab/SuperMemory-VQA | - |
| Causal-Plan-1M | THUSI-Lab | 2026 | 1M QA / 22.2K clips | 单目 | https://huggingface.co/datasets/anonymous-causal-plan/Causal_Plan | - |
| EgoServe | - | 2026 | 3K+ 实例 | 单目 | https://huggingface.co/datasets/SitongGong/EgoServe | - |
| EgoCoT-Bench | - | 2026 | 351 视频 / 3,172 QA | 单目 | https://huggingface.co/datasets/DStardust/EgoCoT-Bench | - |
| Ego2Web | - | 2026 | 500 对 | 单目 | https://huggingface.co/datasets/Shoubin/Ego2Web | - |
| GameplayQA | HATS-ICT | 2026 | ~2.4K QA | 合成 | https://huggingface.co/datasets/wangyz1999/GameplayQA | - |
| Ego-METAS | - | 2026 | 100 h / 5 模态 | 单目 | https://huggingface.co/datasets/Ego-METAS/Ego-METAS | - |
| EgoTactile | - | 2026 | 768 片段 | 单目 | https://huggingface.co/datasets/icml-2026-submission/EgoTactile | - |
| epic-contact | - | 2026 | 2.3K 片段 | 单目 | https://huggingface.co/datasets/Sid2697/epic-contact | - |
| sg-ego | - | 2026 | 3.8M 图 | 单目 | https://huggingface.co/datasets/francescapistilli/sg-ego | - |
| hrdexdb | - | 2026 | 1.4K 抓取 | 单目 | https://huggingface.co/datasets/hahahataeyun/hrdexdb | - |
| interpet4d | - | 2026 | 6.8M 帧 | 多目 | https://huggingface.co/datasets/ohicarip/interpet4d | - |
| OVO-S-Bench | - | 2026 | 348 视频 | 单目 | https://huggingface.co/datasets/kfkas/ovo-s-bench-ego4d-benchmark | - |

## 2. 需申请 (`gated` / `request`)

| 数据集 | 机构 | 年份 | 规模 | 视角 | 申请入口 | 类型 |
|---|---|---|---|---|---|---|
| 10Kh RealOmni-Open | 简智机器人 GenRobot | 2026 | >10,000 h | 单目 | https://huggingface.co/datasets/genrobot2025/10Kh-RealOmin-OpenData | gated |
| **Ego-OSCAR (stereo-550)** | fpvlabs | 2026 | ~550 h/相机 | **双目+IMU** | https://huggingface.co/datasets/fpvlabs/stereo-550 | gated |
| HA-Ego (ego500) | Human Archive | 2026 | 500+ | 头+腕 | https://huggingface.co/datasets/humanarchive/ego500 | gated |
| EgoSuite-Open100K | 光轮智能 Lightwheel | 2026 | 100,000 h | 头+腕 | https://egosuite100k.lightwheel.ai/ | request |
| EgoDemo / EgoPro / EgoStandard | 光轮智能 Lightwheel | 2026 | - | 头+腕 | https://huggingface.co/datasets/LightwheelAI/EgoDemo | gated |
| AgiBotWorld-Beta | 智元机器人 AgiBot | 2025 | 100 万轨迹 | 机器人(非人类) | https://huggingface.co/datasets/agibot-world/AgiBotWorld-Beta | gated |
| Egocentric-10K | Build AI | 2025 | 10,000 h / 10.8 亿帧 | 单目 | https://huggingface.co/datasets/builddotai/Egocentric-10K | gated |
| PRISM-100K | DreamVu | 2026 | 270K 样本 | 单目 | https://huggingface.co/datasets/DreamVu/PRISM-100K | gated |
| SABER-10K | DreamVu | 2026 | 100 h | 单目 | https://huggingface.co/datasets/DreamVu/SABER-10K | gated |
| EgoExo-Fitness | iSEE Lab | 2024 | 32 h | ego+exo | https://huggingface.co/datasets/Lymann/EgoExo-Fitness | gated |
| EgoCross | - | 2026 | 798 片段 | 单目 | https://huggingface.co/datasets/myuniverse/EgoCross | gated |
| Ropedia Xperience-10M | Ropedia | 2026 | 10M | 多目 | https://huggingface.co/datasets/ropedia-ai/xperience-10m | gated |
| EgoFun3D | SFU | 2026 | 271 视频 | 单目 | https://huggingface.co/datasets/3dlg-hcvc/EgoFun3D | gated |
| Ego-1K | Meta | 2026 | ~1K take | 多目 | https://huggingface.co/datasets/facebook/ego-1k | gated |
| EgoProactive / Pro²Bench | Meta | 2026 | 700 录制 | 单目 | https://huggingface.co/datasets/facebook/wearable-ai | gated |
| Ego4D | Meta AI | 2022 | 3,670 h | 单目 | https://ego4d-data.org | request/DUA |
| Ego-Exo4D | Meta AI | 2024 | 1,286 h | 多目+exo | https://ego-exo4d-data.org | request/DUA |

## 3. 双目 / 立体 / 头+腕（重点）

| 数据集 | 机构 | 立体类型 | 规模 | 访问 | 链接 |
|---|---|---|---|---|---|
| EgoViz-120 | humaidtech | 双目 + 双腕 | 120 h | open | https://huggingface.co/datasets/humaidtech/EgoViz-120 |
| ego-stereo-cn-v1 | tatezhou | 双目 LeRobot | <1K | open | https://huggingface.co/datasets/tatezhou/ego-stereo-cn-v1 |
| Ego-OSCAR (stereo-550) | fpvlabs | 全局快门立体+IMU | ~550 h | gated | https://huggingface.co/datasets/fpvlabs/stereo-550 |
| HOT3D | Meta | 多目(Quest3 立体) | 833 min | open | https://huggingface.co/datasets/projectaria/hot3d |
| Gen-HumanEgo | 简智 GenRobot | 6 摄(头+手) | 1,800 h | open | https://huggingface.co/datasets/genrobot2025/Gen-HumanEgo |

> 另：SANPO(Google 双目行车)、UnrealEgo(MPI 立体鱼眼)、EgoCap(ETH 双鱼眼) 见下节。

## 4. 官方 GitHub / 数据门户（无 HF 仓库，可直接下载或申请）

| 数据集 | 机构 | 年份 | 规模 | 视角 | 链接 |
|---|---|---|---|---|---|
| EPIC-KITCHENS-100 | Univ. Bristol | 2021 | 100 h | 单目 | https://epic-kitchens.github.io/ |
| HD-EPIC | Univ. Bristol | 2025 | 41 h | 单目(Aria) | https://hd-epic.github.io/ |
| Charades-Ego | AI2 / CMU | 2018 | ego/exo 配对 | 单目 | https://prior.allenai.org/projects/charades-ego |
| HOI4D | 清华等 | 2022 | 2.4M 帧 | 单目 RGB-D | https://hoi4d.github.io/ |
| EgoDex | Apple | 2025 | 829 h | 单目(Vision Pro) | https://github.com/apple/ml-egodex |
| Open X-Embodiment | Google DeepMind + 21 | 2023 | 100 万+ 轨迹 | 混合 | https://robotics-transformer-x.github.io |
| SANPO | Google | 2023 | 701 段 | **双目** | https://google-research-datasets.github.io/sanpo_dataset/ |
| UnrealEgo / UnrealEgo2 | MPI + Keio | 2022/24 | 合成+真实 | **双目鱼眼** | https://4dqv.mpi-inf.mpg.de/UnrealEgo/ |
| EgoCap | ETH Zurich | 2016 | - | **双鱼眼** | https://arxiv.org/abs/1609.07306 |
| EgoMimic | Georgia Tech + Stanford | 2024 | 小时级 | 头+腕 | https://egomimic.github.io/ |
| UMI / DexUMI | Stanford 等 | 2024/25 | 演示级 | 腕部单目 | https://umi-gripper.github.io/ · https://dex-umi.github.io/ |
| Open-TeleVision | UCSD/MIT | 2024 | 演示 | VR 双目 | https://robot-tv.github.io/ |

## 5. 已剔除 / 降级（无真实数据仓库或仅营销）

| 条目 | 原因 |
|---|---|
| 京东 EgoLive（独立） | 实际数据以 `jdopensource/Gen-EgoData` 发布；未找到独立 EgoLive HF 仓库 |
| 光轮 EgoSuite-Open100K | 官网可申请，HF/AtomGit 尚未检索到公开仓库 |
| Aligned DexWorld（跨维）、XRZero-G0（自变量）、ZODA（诺亦腾）、LARYBench（美团）、RoVid-X（字节） | 仅新闻稿，未找到公开数据仓库 |
| RoboMIND | 未核实到公开 HF/ModelScope 直链 |
| StereoEgo、EgoDepth | 无任何可信出处，**已删除** |
| facebook/ego-1k | raw README 404，状态待定（暂列 gated） |

---

## 贡献

见 [CONTRIBUTING.md](CONTRIBUTING.md)。要求：**必须提供可下载/可申请的数据仓库链接（HF/ModelScope/OpenDataLab/GitHub release）**，不接受纯官网首页。

## License

[Apache-2.0](LICENSE)。数据版权归各自发布方所有。
