# Ego 数据深度分析（截至 2026-09-23）

> 本文配套 [README](../README.md)，数据源为 `data/ego-datasets.csv` 与 `data/quality-ranking.csv`。

---

## 一、规模统计（小时数）

**已解析小时数的 27 个数据集合计 ≈ 134,353 小时（≈15.3 年连续视频）。** 这是**下界**，多数新数据集（Gen-HumanEgo 1,800h 未计入、WIYH 以“条”计、Demo 类无时长）未纳入。

### Top 10（按小时）

| 排名 | 数据集 | 机构 | 小时 |
|---|---|---|---|
| 1 | EgoSuite-Open100K | 光轮智能 | 100,000 |
| 2 | Egocentric-10K | Build AI | 10,000 |
| 2 | 10Kh RealOmni-Open | 简智机器人 | 10,000 |
| 4 | Ego4D | Meta | 3,670 |
| 5 | Open-AoE | Ant Group | 2,000 |
| 6 | Gen-HumanEgo | 简智机器人 | 1,800 |
| 7 | Ego-Exo4D | Meta | 1,286 |
| 8 | Nymeria | Meta | 1,100 |
| 9 | SynData | 灵初智能 | 1,000 |
| 10 | EgoDex | Apple | 829 |

### 小时数 × 分类

| 分类 | 小时 | 占比 |
|---|---|---|
| manipulation / HOI | 115,893 | 86% |
| general（通用语料） | 16,056 | 12% |
| procedural | 799 | 0.6% |
| stereo（双目） | 670 | 0.5% |
| memory / long-form | 654 | 0.5% |
| action | 232 | 0.2% |
| VQA | 41 | 0.03% |
| world-model | 8 | ~0 |

**结论**：**规模被「机器人操作」数据垄断**（86%），而双目、VQA、世界模型的总时长加起来不足 1%。数量上 VQA/记忆类很多，但**单集短、总量小**。

---

## 二、质量维度与评分

数据质量在 Ego 领域没有统一标准。本清单提出 6 个可操作维度，加权成 0–100 分（脚本见 commit）：

| 维度 | 权重 | 说明 |
|---|---|---|
| 规模 Scale | 28% | log10(小时)，10 万 h 封顶 |
| 模态丰富度 Modality | 18% | RGB/深度/手/全身/IMU/触觉/语音/3D 的种类数 |
| 标注密度 Annotation | 18% | 手部/3D/语义/SLAM/触觉/深度/视线/接触 |
| 视角 View | 14% | 多目 > 双目/头+腕 > 单目 |
| 开放度 Access | 10% | open > gated > request |
| 采用度 Adoption | 12% | log10(HF 下载量) |

### 质量 Top 12

| 排名 | 数据集 | 机构 | 分 | 小时 |
|---|---|---|---|---|
| 1 | EgoSuite-Open100K | 光轮智能 | 63.9 | 100,000 |
| 2 | Ego-OSCAR (stereo-550) | fpvlabs | 61.5 | 550 |
| 3 | EgoViz-120 | humaidtech | 60.8 | 120 |
| 4 | HoloAssist | Microsoft | 59.9 | 166 |
| 5 | Gen-HumanEgo | 简智机器人 | 58.5 | 1,800 |
| 6 | 10Kh RealOmni-Open | 简智机器人 | 54.7 | 10,000 |
| 7 | Ego4D | Meta | 54.2 | 3,670 |
| 8 | Nymeria | Meta | 53.9 | 1,100 |
| 9 | EgoLife | EvolvingLMMs-Lab | 53.6 | 300 |
| 10 | SynData | 灵初智能 | 53.2 | 1,000 |
| 11 | Ropedia Xperience-10M | Ropedia | 51.2 | - |
| 12 | ACE-Data-0 | ACE Robotics | 51.1 | 150 |

**观察**：最高分也只有 63.9/100 —— 说明**没有任何一个数据集在“规模+模态+标注+视角+开放+采用”上全面领先**；质量与规模严重脱钩（EgoViz-120 仅 120h 却排第 3，EgoSuite 靠规模第一）。

> ⚠️ 该评分是启发式，仅用于横向对比，不代表下游任务性能。

---

## 三、Ego 数据综述清单（截至 2026-09-23）

| 年份 | arXiv | 标题 | 侧重 |
|---|---|---|---|
| 2026 | 2609.19793 | AI Smart Glasses for Wearable Intelligence | 智能眼镜/可穿戴 |
| 2026 | 2608.24877 | From Seeing to Acting: Smart Glasses as First-Person Intelligence Platforms | 眼镜=第一人称智能平台 |
| 2026 | 2608.18671 | **Vision-Language Models for Egocentric Video: From HOI to Embodied AI** | Ego-VLM |
| 2026 | 2607.28394 | Hand-Object Interaction in the Age of Large Foundation Models | HOI |
| 2026 | 2607.24744 | **Data Pyramid for Embodied Manipulation: A Survey** | 具身数据生态 |
| 2026 | 2606.00054 | **From Human Videos to Robot Manipulation: A Survey on Scalable VLA with Human-Centric Data** | 人类视频→VLA |
| 2026 | 2605.12090 | World Action Models: The Next Frontier in Embodied AI | 世界动作模型 |
| 2026 | 2604.27621 | **Robot Learning from Human Videos: A Survey** | 人类视频→机器人 |
| 2025 | 2511.13261 | Building Egocentric Procedural AI Assistant | 程序性助手 |
| 2025 | 2506.06253 | Bridging Perspectives: Cross-view Collaborative Intelligence (Ego-Exo) | 跨视角 |
| 2025 | 2503.15275 | **Challenges and Trends in Egocentric Vision: A Survey** | 全景综述 |
| 2024 | 2410.20621 | Egocentric and Exocentric Methods: A Short Survey | 短综述 |
| 2024 | 2403.17893 | A Survey on 3D Egocentric Human Pose Estimation | 3D 姿态 |
| 2024 | 2308.07123 | An Outlook into the Future of Egocentric Vision (IJCV) | 未来展望 |
| 2021 | 2107.13411 | Predicting the Future from First Person Vision: A Survey | 未来预测 |
| 2019 | 1912.10867 | Analysis of the Hands in Egocentric Vision: A Survey | 手部 |
| 2015 | 1501.02825 | A Survey on Recent Advances of CV Algorithms for Egocentric Video | 传统方法 |
| 2014 | 1409.1484 | The Evolution of First Person Vision Methods: A Survey | 早期奠基 |

---

## 四、这些综述都分析了什么

1. **任务分类**：2503.15275 把 Ego 任务分为「主体/客体/环境/混合」四类；2608.18671 围绕「识别→多模态基础模型→具身系统」演进；2403.17893 专攻 3D 人体姿态。
2. **数据集罗列**：几乎每篇都附数据集表（规模、模态、任务），但多为**静态快照**。
3. **人类视频→机器人**：2604.27621 / 2606.00054 系统梳理「潜动作、世界模型、3D 表征、轨迹重定向」四类迁移路线，并提出「数据基础」是核心瓶颈。
4. **数据生态分层**：2607.24744 首次把具身数据组织成「真机 / UMI / ego-exo / 仿真 / 通用视觉语言」五层金字塔，并给出质量-多样性-可复用性-物理保真度四维。
5. **可穿戴系统闭环**：2608.24877 强调「感知-状态-交互-行动」完整闭环，而非单点模型。
6. **世界模型**：2605.12090 定义 World Action Models（联合建模未来状态与动作）。
7. **HOI 基础模型先验**：2607.28394 梳理基础模型在 HOI 重建/生成中的六类任务。

---

## 五、重要但普遍缺失的分析（我的判断）

| 缺失点 | 为什么重要 | 现状 |
|---|---|---|
| **1. 小时数的真实核验** | 新闻宣称的“10 万小时”常是**采集总量**而非**已开放量**（光轮 Open100K 首批仅部分上线） | 综述只抄宣称值，无实测 |
| **2. 质量/可用性标准化** | 没有统一质量指标，用户无法选型 | 本文首次给启发式评分，但行业无共识 |
| **3. 许可与可申请性** | “开源”≠可商用；gated/DUA 差异巨大 | 综述几乎不区分 open/gated/DUA |
| **4. 双目/立体被忽视** | 立体对深度/尺度/机器人迁移关键，但综述极少单列 | 仅 BinoGen(2609.19881)、Ego-OSCAR 等零星 |
| **5. 数据去重与血缘** | 大量数据集基于 Ego4D/EPIC 二次标注，存在**同源重复** | 无血缘图谱 |
| **6. 采集设备与标定** | 相机内参/时间同步/SLAM 精度决定可用性 | 极少系统比较 |
| **7. 隐私与合规** | Ego 数据含人脸/语音/身份，跨域合规差异大 | 多篇提及，无量化 |
| **8. 长尾/多样性度量** | 场景、人群、任务分布极不均衡 | 无多样性指标 |
| **9. 失败样本 / 负面数据** | 机器人学习最缺“纠错/失败”数据 | 仅 EgoRecovery 等零星 |
| **10. 评测协议不统一** | 同一任务（如 EgoSchema）被不同数据集各自评测 | 无统一 leaderboard |
| **11. 触觉/力觉模态** | 仅少数（EgoTouch、H-Tac、EgoTactile） | 综述覆盖不足 |
| **12. 成本与采集效率** | 每小时的采集/标注成本几乎无人披露 | 商业公司核心机密 |

---

## 六、Ego 数据的生态位（Niche）

Ego 数据处在 **「人类行为」与「机器人行动」之间的转换层**，其独特生态位可概括为：

```
        人类互联网视频          真机遥操作数据
              \                    /
               \                  /
         [ Ego 数据 = 转换层/桥梁 ]
              /                  \
   人类先验/尺度/操作语义    低成本、可规模化
```

**四个不可替代的生态位：**

1. **规模-成本优势**：真机数据每小时的采集成本比 Ego 高 1–2 个数量级；Ego 用「无本体采集」换取规模化（光轮 10 万 h、简智 1 万 h、京东规划千万 h）。
2. **人手→机械手的语义桥梁**：手-物交互（HOI）是唯一能直接映射到抓取/操作策略的人类信号，占数据量 86%。
3. **世界模型的动作条件来源**：世界模型需要「动作-后果」配对，Ego 视频天然提供（2605.12090、EgoViz）。
4. **可穿戴/助手的唯一视角**：智能眼镜、记忆助手、主动服务只能从第一人称做（2608.24877、EgoLife）。

**竞争与替代关系：**
- 与**仿真数据**：Ego 提供真实性与长尾，仿真提供物理精确与标注完美 → 互补而非替代（2607.24744 金字塔）。
- 与**真机数据**：Ego 负责预训练，真机负责对齐/精调（2606.00054、Ego2Robot、HumanNet）。
- 与**通用互联网视频**：Ego 的视角/手部/动作信息密度远高，但规模仍小 3–4 个数量级。

**生态位的风险：**
- **许可收紧**：2025 起 gated 占比上升，大厂开始圈地；
- **质量参差**：宣称规模 >> 实际可用；
- **同质化**：大量数据集做同样的 HOI，重复投入。

---

## 七、给数据使用者的建议

1. **优先看 HF/ModelScope 仓库与 `gated` 状态**，别信官网宣称的规模。
2. **按任务选生态位**：预训练看规模（光轮/简智/Open-AoE）；灵巧操作看标注（Gen-HumanEgo/EgoDex/Open-AoE）；立体/深度看双目（EgoViz-120/Ego-OSCAR/HOT3D）；记忆/助手看长时（EgoLife/EgoMonth）。
3. **关注血缘**：EgoSchema/EgoTaskQA 等基于 Ego4D，混用会重复计数。
4. **合规前置**：商用前确认许可（CC-BY-SA 有传染性，CC-BY-NC 禁商用，DUA 需单独谈）。
