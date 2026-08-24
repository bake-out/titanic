# titanic
泰坦尼克号生存预测-机器学习项目
# Titanic Survival Prediction
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-orange)](https://scikit-learn.org/)

## 🚢 项目简介
这是一个基于Kaggle经典竞赛“Titanic: Machine Learning from Disaster”的机器学习项目。项目目标是通过乘客信息（如性别、年龄、舱位等级等），预测其在泰坦尼克号沉没事故中是否幸存。

本项目通过特征工程实验，最终发现删除缺失值较多的`Age`特征后，模型性能得到最佳提升。

## ✨ 项目亮点
*   **严谨的实验设计**：通过控制变量法，逐一验证不同特征对模型性能的影响。
*   **明确的结论**：揭示了在特定数据集下，“特征质量 > 特征数量”的核心原则。
*   **完整的流程**：覆盖了从数据清洗、特征工程、模型训练到结果提交的全过程。

## 📊 实验结果
| 实验 | 核心改动 | 分数 | 结论 |
| :--- | :--- | :--- | :--- |
| 基准 | 7特征 + 随机森林 | 0.75598 | 初始基线 |
| **最佳方案** | **删除 `Age` 特征** | **0.77033** | **删除低质量特征，模型准确率提升** |
| 实验六 | 仅使用 `Sex` + `Pclass` | 0.76555 | 两个最强特征已能提供足够信息 |

**最佳模型**：随机森林 (`RandomForestClassifier`)，特征为 `Pclass`, `Sex`, `SibSp`, `Parch`, `Fare`, `Embarked`。

## 🚀 快速开始
### 环境准备
确保你已安装Python 3.8+，然后安装依赖：
```bash
pip install -r requirements.txt
