# 中文电子病历实体识别现存方法性能 #

中文电子病历实体识别任务的数据集以及相应数据集上系统模型性能表现。目前现存公开的中文电子病历标注数据十分稀缺，为了推动CNER系统在中文临床文本上的表现，中国知识图谱与语义计算大会(China Conference on Knowledge Graph and Semantic Computing, CCKS)在近几年都组织了面向中文电子病历的命名实体识别评测任务，下面我们主要关注CCKS CNER数据集上的结果。
 
- [CCKS 2017](#17)
- [CCKS 2018](#18)
- [CCKS 2019](#19)
- [CCKS 2020](#20)


## [CCKS 2017](https://www.biendata.xyz/competition/CCKS2017_2/)  ##
<a name="17"></a>
CCKS17数据集：原始数据集分为训练集和测试集，其中训练集包括300个医疗记录，人工标注了五类实体(包括症状和体征、检查和检验、疾病和诊断、治疗、身体部位)。测试集包含100个医疗记录。 

**语料数据统计**
|  | 症状体征|检查检验|疾病诊断|治疗|身体部位|总数| 
| :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| 训练集 | 7,831	| 9,546	| 722 | 1,048 | 10,719 | 29,866 |
| 测试集 | 2,311	| 3,143 | 553 | 465 | 3,021 | 9,493 |


**现存方法性能比较 (%F值)**



| 方法 | 症状体征|检查检验|疾病诊断|治疗|身体部位|总体|论文|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| HIT-CNER (Hu et al., 2017) Top1 | 96.00 |	94.43 |	78.97 |	81.47 |	87.48 | 91.14 | [HITSZ_CNER: a hybrid system for entity recognition from Chinese clinical text](http://ceur-ws.org/Vol-1976/paper05.pdf) |
| BiLSTM-CRF-DIC (Wang et al., 2019) | - |	- |	- |	- |	- | 91.24 | [Incorporating dictionaries into deep neural networks for the chinese clinical named entity recognition](https://doi.org/10.1016/j.jbi.2019.103133) |
| RD-CNN-CRF (Qiu et al., 2019) | - |	- |	- |	- |	- | 91.32 | [Chinese Clinical Named Entity Recognition Using Residual Dilated Convolutional Neural Network with Conditional Random Field](https://doi.org/10.1109/TNB.2019.2908678) |
| Tang et al. (2019) | - |	- |	- |	- |	- | 91.34 | [融入语言模型和注意力机制的临床电子病历命名实体 识别](https://kns.cnki.net/kcms/detail/detail.aspx?dbcode=CJFD&dbname=CJFDLAST2020&filename=JSJA202003034&v=Ntl86ICshXNN1esogTLhJ2IVb0OpIvyIjXQtWpJ%25mmd2BHFriZZVaOS1OAvlni6EQ3gJB) |
| PDET Feature in Model-II (Lu et al., 2019) | - |	- |	- |	- |	- | 92.68 | [Chinese Clinical Named Entity Recognition with Word-Level Information Incorporating Dictionaries](https://doi.org/10.1109/IJCNN.2019.8852113) |
| BiLSTM-CRF-SP+ELMo (Luo et al., 2020) | 95.37 |	94.94 |	81.13 |	83.32 |	88.74 | 91.75 | [基于笔画ELMo和多任务学习的中文电子病历命名实体识别研究](https://nxgp.cnki.net/kcms/detail?v=3uoqIhG8C46NmWw7YpEsKMypi3qVj28LGACqMpRVR0Cx7F0z4nrArOkieaNEVV6aCvPFCLMxyD4Jd9UPWqorowq7bp%25mmd2BEnUre&uniplatform=NZKPT) |
| FT-BERT + BiLSTM + CRF+Fea (Li et al., 2020) | 96.57 |	94.09 |	81.26 |	82.62 |	88.37 | 91.60 | [Chinese clinical named entity recognition with variant neural structures based on BERT methods](https://doi.org/10.1016/j.jbi.2020.103422) |

注：Top表示当时评测的前三名系统方法。



## [CCKS 2018](https://www.biendata.xyz/competition/CCKS2018_1/)  ##
<a name="18"></a>
CCKS18数据集：原始数据集包括训练集和测试集．其中训练集包括600个医疗记录，人工标注了五 类实体（包括解剖部位、症状描述、独立症状、药物、 手术）。测试集包含400个医疗记录原始数据。 


**语料数据统计**
|  | 解剖部位|症状描述|独立症状|药物|手术|总数| 
| :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| 训练集 | 9,472	| 2,484	| 3,712 | 1,221 | 1,329 | 18,218 |
| 测试集 | 6,339	| 918 | 1,327 | 813 | 735 | 10,132 |


**现存方法性能比较 (%F值)**



| 方法 | 解剖部位|症状描述|独立症状|药物|手术|总体|论文|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| Alihealth Lab (Yang and Huang) (2018) Top1 | 87.97 |	90.59 |	92.45 |	94.49 |	85.43 | 89.13 | [A Conditional Random Fields Approach to Clinical Name Entity Recognition](http://ceur-ws.org/Vol-2242/paper01.pdf) |
| DUTIR (Luo et al., 2018) Top3 | 87.59 |	90.77 |	91.72 |	91.53 |	86.41 | 88.63 | [DUTIR at the CCKS-2018 Task1: A Neural Network Ensemble Approach for Chinese Clinical Named Entity Recognition](http://ceur-ws.org/Vol-2242/paper02.pdf) |
| BiLSTM-CRF (Ji et al., 2018) | 86.65 | 89.13 | 90.69 |	91.15 |	85.61 | 87.68 | [A BiLSTM-CRF Method to Chinese Electronic Medical Record Named Entity Recognition](https://doi.org/10.1145/3302425.3302465) |
| Lattice-LSTM (潘璀然等人, 2019) | - |	- |	- |	- |	- | 89.75 | [基于句子级 Lattice- 长短记忆神经网络的中文电子病历命名实体识别](https://doi.org/10.16781/j.0258-879x.2019.05.0497) |
| Attention-BiLSTM-CRF + all (Ji et al, 2019) | - |	- |	- |	- |	- | 90.82 | [A hybrid approach for named entity recognition in Chinese electronic medical record](https://doi.org/10.1186/s12911-019-0767-2) |
| MSD_DT_NER (Wang et al., 2020) | 88.01 |	92.57 |	90.71 |	94.58 |	85.62 | 89.88 | [Chinese medical named entity recognition based on multi-granularity semantic dictionary and multimodal tree](https://doi.org/10.1016/j.jbi.2020.103583) |
| BiLSTM-CRF-SP+ELMo (Luo et al., 2020) | 89.69 |	91.83 |	92.01 |	91.30 |	86.22 | 90.05 | [基于笔画ELMo和多任务学习的中文电子病历命名实体识别研究](https://nxgp.cnki.net/kcms/detail?v=3uoqIhG8C46NmWw7YpEsKMypi3qVj28LGACqMpRVR0Cx7F0z4nrArOkieaNEVV6aCvPFCLMxyD4Jd9UPWqorowq7bp%25mmd2BEnUre&uniplatform=NZKPT) |
| FT-BERT + BiLSTM + CRF+Fea (Li et al., 2020) | 89.12 |	90.66 |	92.94 |	87.99 |	87.59 | 89.56 | [Chinese clinical named entity recognition with variant neural structures based on BERT methods](https://doi.org/10.1016/j.jbi.2020.103422) |

注：Top表示当时评测的前三名系统方法。


## [CCKS 2019](https://www.biendata.xyz/competition/ccks_2019_1/)  ##
<a name="19"></a>
CCKS19数据集：原始数据集包括训练集和测试集．其中训练集包括1000个医疗记录，人工标注了六类实体（包括疾病和诊断、检查、检验、手术、药物、解剖部位）。测试集包含379个医疗记录原始数据。 


**语料数据统计（唯一实体个数）**
|  | 疾病和诊断|检查|检验|手术|药物|解剖部位| 总数|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: |:----: |
| 训练集 | 2,116	| 222	| 318 | 765 | 456 | 1486 | 5,363|
| 测试集 | 682	| 91 | 193 | 140 | 263 | 447 | 1,816 |



**现存方法性能比较 (%F值)**



| 方法 | 疾病和诊断|检查|检验|手术|药物|解剖部位|总体|论文|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |:----: |
| Alihealth (乔锐等人, 2019) Top1 | 84.29 | 86.29 | 76.94 | 83.33 |	96.02 | 86.18 | 85.62 |[基于BERT与模型融合的医疗命名实体识别](https://conference.bj.bcebos.com/ccks2019/eval/webpage/pdfs/eval_paper_1_1_1.pdf) |
| MSIIP (Liu et al., 2019) Top2 | - | - |	- |	- |	- | - | 85.59|[Team MSIIP at CCKS 2019 Task 1](https://conference.bj.bcebos.com/ccks2019/eval/webpage/pdfs/eval_paper_1_1_2.pdf) |
| DUTIR (Li et al., 2019) Top3 | 82.81 | 88.01 | 75.65 |	86.79 |	94.49 | 85.99 | 85.16| [DUTIR at the CCKS-2019 Task 1: Improving Chinese clinical named entity recognition using stroke ELMo and transfer learning](https://www.researchgate.net/profile/Ling_Luo11/publication/335824610_DUTIR_at_the_CCKS-2019_Task1_Improving_Chinese_Clinical_Named_Entity_Recognition_using_Stroke_ELMo_and_Transfer_Learning/links/5d7d836992851c87c389caf8/DUTIR-at-the-CCKS-2019-Task1-Improving-Chinese-Clinical-Named-Entity-Recognition-using-Stroke-ELMo-and-Transfer-Learning.pdf) |

注：Top表示当时评测的前三名系统方法。

## [CCKS 2020](https://www.biendata.xyz/competition/ccks_2020_2_1/)  ##
<a name="20"></a>
CCKS20数据集：原始数据集包括训练集和测试集．其中训练集包括1050个医疗记录，人工标注了六类实体（包括疾病和诊断、检查、检验、手术、药物、解剖部位）。测试集未公开。 


**语料数据统计**
|  | 疾病和诊断|检查|检验|手术|药物|解剖部位| 总数|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: |:----: |
| 训练集 | 4,345	| 1002	| 1297 | 923 | 1935 | 8811 | 18313|




**现存方法性能比较 (%F值)**



| 方法 | 疾病和诊断|检查|检验|手术|药物|解剖部位|总体|论文|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |:----: |
| CASIA_Unisound (Li et al.,2020) Top1 | 90.93 | 89.96 | 85.94 | 94.85 |	93.56 | 91.62 | 91.56 |[Noisy Label Learning for Chinese Medical Named Entity Recognition Based on Uncertainty Strategy](https://bj.bcebos.com/v1/conference/ccks2020/eval_paper/ccks2020_eval_paper_3_1_1.pdf) |
| TMAIL (晏阳天等人, 2020) Top2 | 90.53 | 88.47 |	83.50 |	96.21 |	93.75 | 92.00 | 91.54|[基于BERT与字形字音特征的医疗命名实体识别](https://bj.bcebos.com/v1/conference/ccks2020/eval_paper/ccks2020_eval_paper_3_1_2.pdf) |
| ChiEHRBert (杨文明等人, 2020) Top3 | 91.10 | 88.62 | 85.71 |	95.52 |	92.93 | 91.16 | 91.24| [基于 ChiEHRBert 与多模型融合的医疗命名实体识别](https://bj.bcebos.com/v1/conference/ccks2020/eval_paper/ccks2020_eval_paper_3_1_3.pdf) |

注：Top表示当时评测的前三名系统方法。