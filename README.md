# Crop-Recommendation-System-Using-Machine-Learning 项目复现

## 1. 项目基本信息
- 对应课程作业登记 Issue: https://github.com/D2RS-2026spring/projects/issues/30
- 项目名称: Crop-Recommendation-System-Using-Machine-Learning 项目的可复现性评估与复现

## 2. 小组成员
- 韩杰 @JieHan369
- 傅垣毓 @FYY0130
- 周蕴熙 @SuperXi-9
- 王子恒 @WZH-303110125

## 3. 原始项目
- 原始项目地址: https://github.com/KRUTHIKTR/Crop-Recommendation-System-Using-Machine-Learning

## 4. 研究目标
本项目围绕原始作物推荐系统开展可复现性评估与复现，检查该项目是否能够在不同环境中完成数据读取、模型训练、结果输出和预测流程，并对结果进行解释。

## 5. 数据来源与预处理
本项目使用原仓库提供的数据集，主要特征包括 N、P、K、temperature、humidity、ph、rainfall，目标变量为 crop label。

预处理工作主要包括：
- 读取原始数据
- 检查数据字段是否完整
- 检查缺失值与异常值情况
- 划分训练集与测试集
- 为后续模型训练准备输入数据

## 6. 数据分析与可视化
本项目对数据进行了基础探索性分析与可视化，包括：
- 各变量的分布情况：核心特征氮（N）的分布呈现明显的双峰形态，样本主要集中在 0-100 区间，高氮含量样本占比极低，整体分布符合农业生产中不同作物的氮需求规律，特征区分度高，为模型训练提供了有效支撑。
- 特征之间的关系：氮元素分布无大量异常值，仅存在少量高值极端样本，未对整体数据分布造成影响，数据集质量稳定，无需复杂预处理即可用于建模。
- 不同模型的效果比较
- 模型支撑层面：特征的双峰分布验证了数据的分类价值，是 Gaussian Naive Bayes 等模型能取得高准确率的重要原因，支撑了原项目的核心结论。
- 结果图表展示：<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/d91867ea-1eb1-4ef2-ac8d-e140bc348409" />


## 7. 模型训练与结果
本项目尝试了多种机器学习模型进行作物推荐预测，包括：
- Logistic Regression
- Gaussian Naive Bayes
- Random Forest
- Support Vector Machine
- AdaBoost

复现结果显示，Gaussian Naive Bayes 模型表现较好，验证集准确率约为 92.53%。

## 8. 结果解读
实验结果表明，原项目在当前数据集和环境下具有较好的可复现性。模型训练流程完整，主要结果能够稳定复现。不同模型在该数据集上的表现存在差异，其中 Gaussian Naive Bayes 和 SVM 表现较优，而部分集成模型效果一般。

## 9. 仓库结构

```text
Crop-Recommendation-System-Using-Machine-Learning/
├── Datasets/
├── Notebook/
├── README.md
├── Requirements.txt
├── Contributing.md
└── crop recommendation model
```

## 10. 复现步骤

1. 下载或克隆本仓库
2. 创建 Python 虚拟环境
3. 安装依赖
4. 打开 Notebook 并按顺序运行
5. 生成结果图表与模型输出
6. 根据 Notebook 中的说明查看分析结论

示例命令：

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
pip install -r Requirements.txt
jupyter notebook
```

## 11. 小组分工

- 韩杰：项目选题、仓库整理、README 编写
- 傅垣毓：数据预处理与结果检查
- 周蕴熙：可视化整理与结果分析
- 王子恒：复现测试与流程记录

## 12. 结论

该项目基本满足结果复现和流程复现要求，但为了更符合课程作业规范，后续仍需继续补充更完整的研究报告说明、成员协作记录以及更加清晰的复现指导。


