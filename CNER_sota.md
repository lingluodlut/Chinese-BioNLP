# CNER SOTA #

中文电子病历实体识别任务的数据集以及相应数据集上系统模型性能表现。目前现存公开的中文电子病历标注数据十分稀缺，为了推动CNER系统在中文临床文本上的表现，中国知识图谱与语义计算大会(China Conference on Knowledge Graph and Semantic Computing, CCKS)在近几年都组织了面向中文电子病历的命名实体识别评测任务，下面我们主要关注CCKS评测上的结果。
 
- [CCKS 2017](#17)
- [CCKS 2018](#18)
- [CCKS 2019](#19)
- [CCKS 2020](#20)


## CCKS 2017  ##
<a name="17"></a>
CCKS17数据集：原始数据集分为训练集和测试集，其中训练集包括300个医疗记录，人工标注了五类实体(包括症状和体征、检查和检验、疾病和诊断、治疗、身体部位)。测试集包含100个医疗记录。 

**语料数据统计**
|  | 症状体征|检查检验|疾病诊断|治疗|身体部位|总体| 
| ----------- | ---- | ---- | ---- | ---- | ---- | ---- |
| 训练集 | 7,831	| 9,546	| 722 | 1,048 | 10,719 | 29,866 |
| 测试集 | 2,311	| 3,143 | 553 | 465 | 3,021 | 9,493 |


**现存方法性能比较 (%F值)**



| 方法 | 症状体征|检查检验|疾病诊断|治疗|身体部位|总体|论文|
| ----------- | ----| ---- | ---- | ---- | ---- | ---- | ---- |
| HIT-CNER (Hu et al., 2017) Top1 | 96.00 |	94.43 |	78.97 |	81.47 |	87.48 | 91.14 | [HITSZ_CNER: a hybrid system for entity recognition from Chinese clinical text](http://ceur-ws.org/Vol-1976/paper05.pdf) |
| BiLSTM-CRF-DIC (Wang et al., 2019) | - |	- |	- |	- |	- | 91.24 | [Incorporating dictionaries into deep neural networks for the chinese clinical named entity recognition](https://doi.org/10.1016/j.jbi.2019.103133) |
| RD-CNN-CRF (Qiu et al., 2019) | - |	- |	- |	- |	- | 91.32 | [Chinese Clinical Named Entity Recognition Using Residual Dilated Convolutional Neural Network with Conditional Random Field](https://doi.org/10.1109/TNB.2019.2908678) |
| BiLSTM-CRF-SP+ELMo (Luo et al., 2020) | 95.37 |	94.94 |	81.13 |	83.32 |	88.74 | 91.75 | [基于笔画ELMo和多任务学习的中文电子病历命名实体识别研究](https://nxgp.cnki.net/kcms/detail?v=3uoqIhG8C46NmWw7YpEsKMypi3qVj28LGACqMpRVR0Cx7F0z4nrArOkieaNEVV6aCvPFCLMxyD4Jd9UPWqorowq7bp%25mmd2BEnUre&uniplatform=NZKPT) |

注：Top表示当时评测的前三名系统方法。




