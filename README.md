# 教育对话、学生画像与长期记忆数据集整理

本仓库是**资源目录**，提供原始入口、数据说明、研究用途及开放状态。未打包、镜像或重新上传第三方原始数据；“入口已核实”指本次访问了官方数据卡、项目仓库或论文页，不代表已下载全部文件、复现论文或完整审计许可。

## 与研究方向的关系

研究目标：从学生与大模型的跨会话对话中，通过长期记忆构建和更新学生画像，并验证画像对意图/对话行为预测、下一轮问题排序等任务的帮助。

- StudyChat：已有实验的主数据，适合继续进行跨会话画像与行为分析。
- MathDial、Eedi、TSCC、CIMA：教育辅导对话补充资源；须检查用户标识、时间顺序及跨会话可连接性。
- TalkMoves、NCTE：课堂话语动作与互动模式参考；数据形态与一对一学生—大模型对话不同。
- LoCoMo、LongMemEval、MemoryAgentBench：检索、更新、冲突处理等记忆能力评测。
- PersonaMem、PrefEval、PGDataset：画像生成、偏好更新与偏好遵循的方法参考；教育任务仍需单独建立评价依据。

上述用途是整理者的适用性判断，不是原作者已证明的教育迁移结论。

## 文件

- `README.md`：中文分类目录。
- `datasets.csv`：可用Excel打开的完整目录。
- `datasets.json`：机器可读目录；每条含状态和核对日期。
- `USAGE.md`：下载、实验划分与引用注意事项。

## 教育对话

| 名称与原始入口 | 数据内容 | 对课题的用途 | 开放/核实状态 | 许可与边界 |
|---|---|---|---|---|
| [StudyChat](https://huggingface.co/datasets/wmcnicho/StudyChat) | 真实大学人工智能课程学生与ChatGPT对话；含层级对话行为标注 | 跨会话画像、提问意图预测、下一轮问题排序 | 公开数据入口已核实 | CC BY 4.0；用途说明另见数据卡 |
| [MathDial](https://huggingface.co/datasets/eth-nlped/mathdial) | 数学辅导对话，真人教师与模拟学生协作采集 | 教学动作、提示策略、教育场景方法验证 | 公开数据入口已核实 | 使用前核对数据卡及各组成数据条款 |
| [Eedi QATD-2k](https://huggingface.co/datasets/Eedi/Question-Anchored-Tutoring-Dialogues-2k) | 题目锚定的数学辅导对话及题目元数据 | 错因证据、辅导行为、画像适配 | 公开数据入口已核实 | CC BY-NC-SA 4.0；非商业研究用途 |
| [TSCC v2](https://www.ecp.ep.liu.se/index.php/sltc/article/view/575) | 英语教师与学习者的一对一聊天课；教学焦点、纠错等标注 | 语言学习画像与长期互动分析 | 研究使用；获取流程待复核 | 论文声明可免费用于研究；具体申请与再分发条款待核对 |
| [CIMA](https://github.com/kstats/CIMA) | 辅导对话、TutorActions和StudentActions；dataset.json | 对话行为预测与教育动作分类 | 公开数据入口已核实 | CC BY 2.5，见仓库README |
| [GrounDialog](https://aclanthology.org/2023.bea-1.26/) | 面向语言学习的口语任务对话；repair与grounding标注 | 理解障碍、澄清请求、互动意图 | 论文已核实；原始数据下载待核对 | 论文开放不代表语料可自由再分发；待核对数据许可 |

## 课堂与多模态

| 名称与原始入口 | 数据内容 | 对课题的用途 | 开放/核实状态 | 许可与边界 |
|---|---|---|---|---|
| [TalkMoves](https://github.com/SumnerLab/TalkMoves) | K-12数学课堂转录；教师与学生话语动作标注 | 教学互动与对话行为分类 | 公开数据入口已核实 | CC BY-NC-SA 4.0；主要是转录文本，不能直接称为音视频数据集 |
| [NCTE Transcripts](https://github.com/ddemszky/classroom-transcript-analysis) | 小学数学课堂转录及相关课堂观察研究资源 | 课堂语言、教学质量与话语模式分析 | 公开项目入口已核实 | 下载及关联文件条款以原仓库为准 |
| [Tutorbot Corpus](https://aclanthology.org/L14-1641/) | 多人面对面协作解题；音视频信号与导师行为标注 | 参与度、注意状态、多模态互动参考 | 论文已核实；原始数据下载待核对 | 不能把论文链接作为已开放数据下载证明 |
| [Ego4D](https://ego4d-data.org/docs/) | 通用第一人称日常活动视频及多种任务标注 | 多模态记忆方法参考；教育画像适配程度有限 | 官方入口已核实；按当前平台流程获取 | 访问已迁至Lab22；按官方当前协议获取 |

## 技能匹配与画像生成

| 名称与原始入口 | 数据内容 | 对课题的用途 | 开放/核实状态 | 许可与边界 |
|---|---|---|---|---|
| [UniSkill](https://huggingface.co/datasets/nurlanm/UniSkill_dataset) | 课程文本与技能匹配相关资源；此前实验使用过Excel | 文本技能匹配与BERT分类基线 | 公开资源入口已核实；需核对文件版本 | 数据卡标Apache-2.0；当前预览显示PDF，不能假定与旧Excel版本相同 |
| [PGDataset / PGTask](https://github.com/ruinunca/PGTask) | 对话话语与画像句子的配对资源 | 画像生成训练与评估方法参考 | 官方代码及下载说明已核实 | 按项目下载说明取数据；数据许可需单独核对 |

## 长期记忆与偏好评测

| 名称与原始入口 | 数据内容 | 对课题的用途 | 开放/核实状态 | 许可与边界 |
|---|---|---|---|---|
| [LoCoMo](https://github.com/snap-research/locomo) | 长跨度多会话对话、问答与事件摘要标注 | 长期检索、时间推理、多跳问答 | 公开数据入口已核实 | 按原仓库数据许可引用和使用 |
| [LongMemEval](https://github.com/xiaowu0162/LongMemEval) | 长历史会话与问答；S/M/oracle版本 | 跨会话检索、信息更新与记忆问答 | 公开数据及格式说明已核实 | 按官方数据包及许可使用 |
| [PersonaMem](https://github.com/bowen-upenn/PersonaMem) | 用户画像、偏好演化上下文与问答；不同上下文长度版本 | 动态画像及个性化回答评估 | 公开数据及格式说明已核实 | 官方仓库链接到Hugging Face数据；按所选版本许可使用 |
| [PrefEval](https://github.com/amazon-science/PrefEval) | 显式和隐式偏好、多会话偏好遵循任务 | 讲解偏好的记忆与使用评测思路 | 公开项目入口已核实 | 通用偏好不能直接当作教育讲解偏好金标准；按原项目条款使用 |
| [MemoryAgentBench](https://github.com/HUST-AI-HYZ/MemoryAgentBench) | 增量多轮交互下的检索、学习、长程理解、冲突解决任务 | 诊断记忆更新和冲突处理能力 | 公开项目入口已核实 | 各组成数据来源和许可分别遵循原项目 |

## 相关开源项目：需区分代码与数据

| 名称与原始入口 | 数据内容 | 对课题的用途 | 开放/核实状态 | 许可与边界 |
|---|---|---|---|---|
| [EduChat](https://github.com/ECNU-ICALK/EduChat) | 教育对话模型、训练及数据处理相关资源 | 教育回应适配和训练流程参考 | 开源项目；非单一已核实原始学生数据集 | 模型、代码、训练语料分别核对，不能合并推定为同一许可 |
| [Who Am I? / dialogue_student_sim](https://github.com/umass-ml4ed/dialogue_student_sim) | 基于历史画像的学生模拟、画像代理与评估代码 | 画像结构、提取和下游学生模拟方法参考 | 代码公开；原始数据仍声明待发布 | 当前README声明去标识化完成后发布数据；不可标记为已拿到原始数据 |
| [LLMsAsEducationalAnalysts](https://github.com/edavalosanaya/LLMsAsEducationalAnalysts) | 多模态阅读评估项目；预处理、评价标准和分析代码 | 多模态证据到教育评估报告的流程参考 | 公开项目入口已核实；原始学生数据开放范围待核对 | 仓库代码MIT标识不能自动覆盖全部原始眼动和学生数据 |

## 旧清单中尚未核实的名称

| 名称与原始入口 | 数据内容 | 对课题的用途 | 开放/核实状态 | 许可与边界 |
|---|---|---|---|---|
| Classroom-Act | 此前对话曾出现此名称，未定位可靠原始数据源 | 待确认准确名称后再评估 | 未核实 | 不列入已开放数据 |
| TALM Classroom Corpus | 此前对话曾出现此名称，未定位可靠原始数据源 | 待确认准确名称后再评估 | 未核实 | 不列入已开放数据 |
| Google Education Dialogue Dataset | 此前提及的泛称，未能确定唯一对应项目 | 需先定位原始论文和数据发布页 | 名称不充分，未核实 | 不据此构造下载链接或宣称已开源 |

## 已有实验记录的解释边界

StudyChat早前本地版本曾统计出16,851条记录、203个用户、2,214个会话；这些是旧实验记录，**未在本次重新下载验证**，不当作当前上游版本的固定规模。此前比较发现分学期文件与合并文件存在覆盖关系，后续下载后仍需按当前版本重新去重核对。

UniSkill此前Excel实验的样本数不能从当前Hugging Face页面PDF预览直接推出，应保留实际使用文件和版本。

## 不属于数据集的长期记忆系统

MemoryBank、MemGPT、MemTree、A-Mem、MemoryOS、LightMem等主要是论文方法或系统项目。它们可提供实现和示例数据，但不能将系统名称直接计为独立教育数据集。本目录仅在有明确数据发布入口时将其归入数据资源。

## 完整性与状态

本目录共23项：17项数据/语料/评测资源、3项相关项目、3项未核实旧名称。17项资源中仍有需要申请、仅核实论文或需要复核文件版本的条目，不能合称“23个已开源数据集”。未找回可核实的具体知识追踪数据集旧清单，因此未凭类别补写ASSISTments等新名称。

核对日期是入口检查日期，不保证之后链接与许可不变。正式实验请记录下载日期、文件SHA256、上游提交或数据版本，并引用各原始作者。
