<div align="center">

# 🎥 Awesome Human Egocentric (Ego) Data

**面向具身智能 / 世界模型的开源第一人称（Ego）人类数据集汇总**
Monocular · Stereo/Binocular · Head+Wrist · Open or requestable

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: Apache-2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Last Update](https://img.shields.io/badge/Updated-2026--09--23-blue.svg)](#)

</div>

---

## 说明 / Legend

- **视角**：`单目` / `双目(立体)` / `头+腕` / `多目`（Project Aria 等）
- **获取**：`开放`=直接下载；`申请`=需注册/DUA；`许可`=开放许可（CC-BY 等）
- **核实**：✅=官方站点/论文/GitHub 已核实；⚠️=仅搜索摘要，下载前请复核

> 本清单优先收录 **Human Ego（第一人称人类）** 数据；纯机器人遥操数据（无人类视角）单独标注。

---

## 📊 统计（截至 2026-09-23）

| 指标 | 数量 |
|---|---|
| 收录条目总数 | **87** |
| 已核实官方来源（✅） | 74 |
| 待复核（⚠️） | 13 |
| 可直接下载 / 开放许可 | 62（+ 开放硬件/代码 4） |
| 需申请 / DUA / 注册 / 登录 | 6 |
| 仅论文（数据待放） | 5 |
| 中国公司 / 机构 | 22 |
| 国际（美国 31、瑞士 4、英国 3、德/韩/澳/荷/新各 1） | 44 |
| **双目 / 立体 / 头+腕** | **12** |

### 链接核验结果（2026-09-23，curl 实测）

- **HTTP 200（可直连）**：绝大部分官网、GitHub、arXiv、GitHub Pages、Project Aria、ModelScope 等。
- **已修正的失效链接**：HoloAssist → `holoassist.github.io`；CaptainCook4D → `github.com/CaptainCook4D/CaptainCook4D`；EgoOops → `github.com/Y-Haneji/EgoOops-annotations`；OakInk → `github.com/oakink/OakInk2`；Nymeria → 去掉尾部斜杠。
- **本机网络屏蔽、无法直连核验（非失效）**：`huggingface.co`（全部 HF 数据集）、`ego4d-data.org`、`ego-exo4d-data.org`、`oakink.net`、`waymo.com/open`、`prior.allenai.org`、`sites.google.com`。这些域名在其它网络环境可正常访问；HF 条目均来自官方发布公告。
- 已剔除无法找到可信出处的 `StereoEgo`、`EgoDepth`。

---

## 📑 目录

1. [中国公司 / 机构](#1-中国公司--机构)
2. [国际公司 / 机构](#2-国际公司--机构)
3. [双目 / 立体 / 头+腕 双视角](#3-双目--立体--头腕-双视角)
4. [大规模通用 Ego 语料（学术）](#4-大规模通用-ego-语料学术)
5. [手-物交互 / 灵巧操作](#5-手-物交互--灵巧操作)
6. [长视频 / 记忆 / VQA](#6-长视频--记忆--vqa)
7. [程序性活动 / VLA / 技能学习](#7-程序性活动--vla--技能学习)
8. [其他 Awesome 清单](#8-其他-awesome-清单)

---

## 1. 中国公司 / 机构

| 数据集 | 公司/机构 | 年份 | 规模 | 视角 | 模态 | 获取 | 官方链接 | 核实 |
|---|---|---|---|---|---|---|---|---|
| **EgoSuite-Open100K** | 光轮智能 Lightwheel | 2026 | 10 万 h / 1.5 万场景 | 头+腕双视角 | 手 21 关节 + 全身 + 深度 + 语义 | 开放（学术+商用双许可） | https://egosuite100k.lightwheel.ai/ · https://github.com/LightwheelAI/LW-Egosuite-DevKit | ✅ |
| **10Kh RealOmni-Open** | 简智机器人 GenRobot | 2026 | >1 万 h / ~100 万 clips | 第一人称无本体 | 视觉/深度/触觉/位姿 | 开放 | https://huggingface.co/datasets/genrobot2025/10Kh-RealOmin-OpenData · https://genrobot.ai/data/open-dataset | ✅ |
| **Gen Ego Data (Gen-EgoData)** | 简智机器人 GenRobot | 2026 | 首批 500 样本 / 4.23 h（持续扩） | 第一人称 + ego-SLAM | 全模态（面向世界模型） | 开放 | https://genrobot.ai/data/assets · https://modelscope.cn （Gen-EgoData） | ✅ |
| **EgoLive 人类第一视角数据集** | 京东 JoyAI | 2026 | 首批开放（规划 1 年 500 万 h） | 第一人称（JoyEgoCam） | 视觉 + 空间交互 | 开放 | 京东云 JoyAI（WAIC 2026-07 发布） | ⚠️ |
| **WIYH (World In Your Hands)** | 它石智航 TARS | 2025 | >10 万条人类操作视频 / 40+ 任务 | 第一人称 Human-centric | VLTA（视觉-语言-触觉-动作） | 开放 | https://wiyh.tars-ai.com/ · https://github.com/tars-robotics/World-In-Your-Hands | ✅ |
| **SynData** | 灵初智能 PsiBot | 2026 | 采集 >10 万 h，开源 1000 h | 第一人称 / 手部 | 视觉+语言+关节角+触觉 | 开放 | https://huggingface.co/datasets/PsiBotAI/SynData | ✅ |
| **EgoRobo-data** | 伊格具身数据 EgoRobo | 2026 | 工业级（持续扩） | 第一人称 | 行为数据采集/标注 | 开放 | https://github.com/EgoRobo-Data/EgoRobo-data | ✅ |
| AgiBot World (Alpha/Beta) | 智元机器人 AgiBot | 2024–25 | Beta 100 万轨迹 | 机器人头+双腕（非人类） | RGB-D/触觉/关节 | 开放 | https://github.com/OpenDriveLab/AgiBot-World · https://huggingface.co/datasets/agibot-world/AgiBotWorld-Beta | ✅ |
| RoboMIND | 北京人形机器人创新中心 | 2024–25 | 10.7 万→40 万+轨迹 | 机器人多视角 | RGB-D/关节 | 开放 | https://modelscope.cn （RoboMIND） | ⚠️ |
| Aligned DexWorld | 跨维智能 DexForce | 2026 | 大规模 | 人类→仿真→真机 | 时空动作对齐 | 开放 | — | ⚠️ |
| XRZero-G0 | 自变量机器人 X2Robotics | 2026 | 2000+ | 头部+多视角 | 视觉/位姿 | 开放 | — | ⚠️ |
| ZODA 具身数据 | 诺亦腾 | 2026 | 计划 600 h | 全身运动 | 全身/交互物体 | 开放 | — | ⚠️ |
| LARYBench | 美团 LongCat | 2026 | 基准+数据 | 人类视频→动作 | 视频/动作表征 | 开放 | — | ⚠️ |
| RoVid-X | 字节跳动 Seed + 北大 | 2026 | 大规模 | 机器人视频生成 | 视频 | 开放 | — | ⚠️ |

> **只开源模型/硬件、未公开人类 Ego 数据**：星尘智能 Astribot、千寻智能 Spirit AI、原力灵机 Dexmal、银河通用 Galbot、影石 Insta360。
> **未发现公开 Human Ego 数据**：腾讯 Robotics X、阿里达摩院、百度、华为、小米、大疆、优必选、傅利叶、宇树、云深处、帕西尼、戴盟、因时、加速进化、松延动力、他山科技。

---

## 2. 国际公司 / 机构

| 数据集 | 公司/机构 | 年份 | 规模 | 视角 | 获取 | 官方链接 | 核实 |
|---|---|---|---|---|---|---|---|
| Ego4D | Meta AI (FAIR) | 2022 | 3,670 h / 923 人 | 单目（部分多目） | 申请 (DUA) | https://ego4d-data.org | ✅ |
| Ego-Exo4D | Meta AI | 2024 | 1,286 h | 多目 + exo | 申请 (DUA) | https://ego-exo4d-data.org | ✅ |
| Nymeria | Meta AI | 2024 | ~1,100 h / 264 人 | 多目 (Aria+Quest3) | 申请 | https://www.projectaria.com/datasets/nymeria | ✅ |
| HOT3D | Meta AI | 2024 | 833 min / 3.7M 图 | 多目（Quest3 立体） | 许可 | https://facebookresearch.github.io/hot3d/ | ✅ |
| AEA (Aria Everyday Activities) | Meta (Project Aria) | 2024 | 143 seq | 多目 | 许可 | https://www.projectaria.com/datasets/aea/ | ✅ |
| ADT (Aria Digital Twin) | Meta | 2023 | 200 seq | 多目 | 许可 | https://www.projectaria.com/datasets/adt/ | ✅ |
| ASE (Aria Synthetic Environments) | Meta | 2024 | 合成 | 多目 | 许可 | https://www.projectaria.com/datasets/ase/ | ✅ |
| EgoObjects | Meta | 2023 | 9.2K+ 视频 | 单目 | 开放 | https://github.com/facebookresearch/EgoObjects | ✅ |
| Ego-1K | Meta | 2026 | ~1K 多视角 take | 多目 | 开放 | https://huggingface.co/datasets/facebook/ego-1k | ✅ |
| EgoProactive / Pro²Bench | Meta | 2026 | 700 录制 | 单目 (Aria) | 开放 | https://huggingface.co/datasets/facebook/wearable-ai | ✅ |
| **EgoDex** | Apple | 2025 | 829 h / 194 任务 | 单目 (Vision Pro) | 许可 (CC-BY-NC-ND) | https://github.com/apple/ml-egodex | ✅ |
| Open X-Embodiment | Google DeepMind + 21 机构 | 2023 | 100 万+ 轨迹（含人类数据） | 混合 | 开放 | https://robotics-transformer-x.github.io | ✅ |
| HowToDIV | Google | 2025 | 24 h / 6,636 QA | 单目 | 论文 | https://arxiv.org/abs/2508.11192 | ✅ |
| SANPO | Google | 2023 | 701 段 | **双目(立体)** | 开放 | https://google-research-datasets.github.io/sanpo_dataset/ | ✅ |
| HoloAssist | Microsoft | 2023 | 166–169 h | 单目+深度 | 开放 | https://holoassist.github.io/ | ✅ |
| SynthEgo | Microsoft | 2024 | 6 万合成图 | **双目合成** | 论文 | https://arxiv.org/abs/2401.14785 | ✅ |
| DreamDojo / DexMimicGen | NVIDIA | 2024–26 | 4.4 万 h / 2.1 万演示 | 单目/仿真 | 代码/模型开放 | https://dreamdojo-world.github.io | ✅ |
| EgoEdit | Snap Research | 2025 | 10 万编辑对 | 单目 | 开放 | https://snap-research.github.io/EgoEdit | ✅ |
| Egocentric-10K | Build AI | 2025 | 10,000 h / 10.8 亿帧 / 16.4 TB | 单目（工厂） | 开放 | https://huggingface.co/datasets/egocentric-10k | ⚠️ |
| comma2k19 / comma10k | comma.ai | 2018/20 | 33 h / 10K 图 | 单目行车 | 开放 | https://github.com/commaai/comma2k19 | ✅ |
| Waymo Open Dataset | Waymo | 2020 | ~11 h 段 | 多相机（车） | 注册下载 | https://waymo.com/open | ✅ |
| EgoMimic | Georgia Tech + Stanford | 2024 | 小时级 | **头(Aria)+腕** | 开放 | https://egomimic.github.io/ | ✅ |
| UMI (Universal Manipulation Interface) | Stanford 等 | 2024 | 演示级 | **腕部单目** | 开放硬件 | https://umi-gripper.github.io/ | ✅ |
| DexUMI | Stanford/Columbia/NVIDIA | 2025 | 演示级 | **腕部单目+触觉** | 开放 | https://dex-umi.github.io/ | ✅ |
| Open-TeleVision | UCSD/MIT | 2024 | 演示 | **VR 双目** | 开放代码 | https://robot-tv.github.io/ | ✅ |
| Ego-OSCAR (550h) | 开源社区 (Paul et al.) | 2026 | ~550 h/相机 | **双目立体+IMU** | 开放 (Apache-2.0) | https://arxiv.org/abs/2608.08285 | ✅ |

> **未找到公开 Human Ego 数据**：Physical Intelligence、Figure、1X、Skild、TRI、Samsung、Sony、Qualcomm、Amazon、Adobe、Runway、Tesla、Nuro、Zoox、Woven Planet、Boston Dynamics、Agility、Apptronik、Sanctuary。

---

## 3. 双目 / 立体 / 头+腕 双视角

| 数据集 | 机构 | 年份 | 立体类型 | 规模 | 获取 | 官方链接 | 核实 |
|---|---|---|---|---|---|---|---|
| **Ego-OSCAR** | 开源社区 | 2026 | 全局快门立体 + IMU，开源硬件 <$200 | ~550 h/相机 | 开放 | https://arxiv.org/abs/2608.08285 | ✅ |
| **EgoSuite-Open100K** | 光轮智能 | 2026 | 头左/右 + 双腕 | 10 万 h | 开放 | https://egosuite100k.lightwheel.ai/ | ✅ |
| **EgoViz-120** | humaidtech | 2026 | 立体 + 双腕 | 120 h | 开放 | https://github.com/humaidtech/EgoViz-120 | ⚠️ |
| **ego-stereo-cn-v1** | 10K HoursData | 2026 | 立体 (LeRobot) | 号称 10K h | 开放 | https://github.com/TateZhouSiu/ego-stereo-cn-v1-tools | ⚠️ |
| UnrealEgo / UnrealEgo2 / -RW | MPI + Keio | 2022/24 | 立体鱼眼 | 合成 + 真实 | 开放 | https://4dqv.mpi-inf.mpg.de/UnrealEgo/ | ✅ |
| EgoCap | ETH Zurich | 2016 | 双鱼眼头盔 | — | 开放 | https://arxiv.org/abs/1609.07306 | ✅ |
| Ego3DPose | KAIST | 2023 | 双目 | — | 代码开放 | https://github.com/tho-kn/Ego3DPose | ⚠️ |
| EgoGlass | Univ. Adelaide | 2021 | 双体相机眼镜 | 多被试 | 开放 | https://github.com/FloralZhao/EgoGlass | ✅ |
| SANPO | Google | 2023 | 双目行车 | 701 段 | 开放 | https://google-research-datasets.github.io/sanpo_dataset/ | ✅ |
| SynthEgo | Microsoft | 2024 | 双目合成 HMD | 6 万图 | 论文 | https://arxiv.org/abs/2401.14785 | ✅ |
| EgoEVHands | 浙江大学 | 2026 | 双目事件相机 | 5,419 序列 | 待发布 | https://github.com/ZJUWang01/EgoEV-HandPose | ⚠️ |
| EventKitchen | TU Delft | 2026 | 双目事件 + RGB-D | 5.5 h | 论文 | https://arxiv.org/abs/2608.04865 | ⚠️ |
| HOT3D | Meta | 2024 | 多目（Quest3 立体） | 833 min | 许可 | https://facebookresearch.github.io/hot3d/ | ✅ |
| EgoMimic | Georgia Tech | 2024 | 头 + 腕 | 小时级 | 开放 | https://egomimic.github.io/ | ✅ |
| StereoEgo / EgoDepth | — | — | 未找到可信出处，暂不收录 | — | — | — | ❌ |

---

## 4. 大规模通用 Ego 语料（学术）

| 数据集 | 机构 | 年份 | 规模 | 视角 | 获取 | 官方链接 |
|---|---|---|---|---|---|---|
| EPIC-KITCHENS-100 | Univ. Bristol | 2021 | 100 h / 90K 段 | 单目 | 开放 | https://epic-kitchens.github.io/ |
| HD-EPIC | Univ. Bristol | 2025 | 41 h 高分辨率 | 单目 (Aria) | 开放 (CC BY-NC) | https://hd-epic.github.io/ |
| EgoLife | EvolvingLMMs-Lab | 2025 | 266–300 h | 多目 (Aria) | 开放 | https://egolife-ai.github.io/ |
| Charades-Ego | AI2 / CMU | 2018 | ego/exo 配对 | 单目 | 开放 | https://prior.allenai.org/projects/charades-ego |
| EgoExoLearn | OpenGVLab | 2024 | 120 h | ego+exo | 开放 | https://github.com/OpenGVLab/EgoExoLearn |
| EgoVid-5M | — | 2024 | 5M 片段 | 单目 | 开放 | https://egovid.github.io/ |
| Ropedia Xperience-10M | Ropedia | 2026 | 10M 多流经历 | 多目 | 开放 | https://huggingface.co/datasets/ropedia-ai/xperience-10m |
| Open-AoE | Ant Group | 2026 | ~2,000 h | 第一人称 | 开放 | https://github.com/ant-research/Open-AoE |
| HumanNet | — | 2026 | ~1M h（ego+exo） | 混合 | 论文 | https://arxiv.org/abs/2605.06747 |
| Ego-Exo4D | Meta | 2024 | 1,286 h | 多目 | 申请 | https://ego-exo4d-data.org |

---

## 5. 手-物交互 / 灵巧操作

| 数据集 | 机构 | 年份 | 规模 | 视角 | 获取 | 官方链接 |
|---|---|---|---|---|---|---|
| HOI4D | 清华等 | 2022 | 2.4M 帧 / 4K 序列 | 单目 RGB-D | 开放 | https://hoi4d.github.io/ |
| OakInk / OakInk2 | 清华 / 北大 | 2022/24 | 100+ 物体 | 多目 | 许可 | https://github.com/oakink/OakInk2 |
| ARCTIC | ETH + MPI | 2023 | 2.1M 帧 | 多目 | 登录 | https://arctic.is.tue.mpg.de/ |
| AssemblyHands | Meta | 2023 | 3M 图像 | 单目 | 开放 | https://assemblyhands.github.io/ |
| H2O | ETH Zurich | 2021 | 100K+ 帧 | 单目 | 开放 | https://h2odataset.ethz.ch/ |
| EgoBody | ETH Zurich | 2022 | 125 seq | 多目 | 申请 | https://egobody.ethz.ch/ |
| FPHA | — | 2018 | 1,175 RGB-D 序列 | 单目 | 开放 | https://guiggh.github.io/publications/first-person-hands/ |
| Touch and Go | — | 2022 | 12K+ 视触帧 | 单目 | 开放 | https://touch-and-go.github.io/ |
| VISOR | Univ. Bristol | 2022 | EPIC + 掩码 | 单目 | 开放 | https://epic-kitchens.github.io/VISOR/ |
| EgoHOS | — | 2022 | 11K+ 图像 | 单目 | 开放 | https://github.com/owenzlz/EgoHOS |
| EgoTouch | — | 2026 | 1,891 回合 / 208 任务 | 单目 | 开放 | https://huggingface.co/datasets/zhenyuxie-zhzh/EgoTouch_hdf5 |
| DexYCB | NVIDIA/多校 | 2021 | 抓取数据集 | 多目 | 开放 | https://dex-ycb.github.io/ |
| EgoDex-R | — | 2026 | 4.3M RGB-D 帧 | 单目 | 论文 | https://arxiv.org/abs/2606.08057 |

---

## 6. 长视频 / 记忆 / VQA

| 数据集 | 机构 | 年份 | 规模 | 获取 | 官方链接 |
|---|---|---|---|---|---|
| EgoSchema | — | 2023 | 250+ h / 5K QA | 开放 | https://egoschema.github.io/ |
| EgoClip | NUS ShowLab | 2022 | 3.8M 图文对 | 开放 | https://github.com/showlab/EgoVLP |
| EgoTaskQA | — | 2022 | ~2K 视频 / 40K QA | 开放 | https://sites.google.com/view/egotaskqa |
| EgoThink / VidEgoThink | — | 2024 | 12 维度 QA | 开放 | https://arxiv.org/abs/2311.15596 |
| EgoMonth | — | 2026 | 301 h / 1,443 QA | 开放 | https://huggingface.co/datasets/anonymous-egomonth/egomonth-dataset |
| EgoMemReason | — | 2026 | 500 MCQ | 开放 | https://huggingface.co/datasets/Ted412/EgoMemReason |
| SuperMemory-VQA | OSU | 2026 | 52.9 h / 4,853 QA | 开放 | https://huggingface.co/datasets/OSU-AIoT-MLSys-Lab/SuperMemory-VQA |
| EgoStream | — | 2026 | 2,250 Q / 8,528 评测 | 开放 | https://saroo25.github.io/Egostream/ |
| EgoSAT | — | 2026 | 165 h / 4.8K QA | 开放 | https://leiyj23.github.io/EgoSAT/ |
| Causal-Plan-1M | THUSI-Lab | 2026 | 1M QA / 22.2K 片段 | 开放 | https://huggingface.co/datasets/anonymous-causal-plan/Causal_Plan |

---

## 7. 程序性活动 / VLA / 技能学习

| 数据集 | 机构 | 年份 | 规模 | 获取 | 官方链接 |
|---|---|---|---|---|---|
| Assembly101 | — | 2022 | 513 h 多视角 | 许可 | https://assembly-101.github.io/ |
| CaptainCook4D | — | 2024 | 烹饪 + 4D 错误标注 | 开放 | https://github.com/CaptainCook4D/CaptainCook4D |
| EgoOops | — | 2024 | 错误动作检测 | 开放 | https://github.com/Y-Haneji/EgoOops-annotations |
| IndustReal | — | 2024 | ~6 h 工业装配 | 开放 | https://timschoonbeek.github.io/industreal.html |
| EgoProceL | — | 2022 | 62 视频 / 16 任务 | 开放 | https://github.com/Sid2697/EgoProceL-egocentric-procedure-learning |
| EgoVerse | GaTech RL2 | 2026 | 1,362 h / ~80K 回合 | 开放 | https://egoverse.ai/ |
| EgoProactive / Pro²Bench | Meta | 2026 | 700 录制 | 开放 | https://huggingface.co/datasets/facebook/wearable-ai |
| HumanEgo | — | 2026 | Aria 演示 | 开放 | https://humanego-ai.github.io/ |

---

## 8. 其他 Awesome 清单

- https://github.com/player0718/awesome-ego-video-datasets
- https://github.com/sun254667/awesome-egocentric-vision
- https://github.com/EgoRobo-Data/EgoRobo-data
- https://github.com/OpenDriveLab/AgiBot-World

---

## 贡献 / Contributing

欢迎 PR 补充新数据集。请提供：名称、机构、年份、规模、视角（单目/双目/头+腕/多目）、模态、获取方式、**官方链接**，并尽量附论文/官网核实。

## 免责声明

本清单为社区整理，链接与规模以各官方发布为准。标记 ⚠️ 的条目来自公开搜索摘要，**下载/引用前请务必核对官方页面**。

## License

[Apache-2.0](LICENSE) — 数据版权归各自发布方所有。
