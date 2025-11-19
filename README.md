🏠 Kaggle Housing Price — Advanced Regression Techniques
Kaggle 排名：TOP 2,601 / 5,000+ 参赛者

本仓库包含我在 Kaggle “House Prices: Advanced Regression Techniques” 比赛中的完整解决方案，包括数据预处理、复杂特征工程、多模型集成（Voting Regressor）与最终预测提交。

📌 1. 项目背景（Project Background）
本项目的任务是预测 Ames, Iowa 地区的房屋销售价格（SalePrice），这是一个经典的回归问题。 项目主要考察：

对高维、多类型数据的理解与处理（包含近80个特征）。

复杂特征工程，尤其针对类别特征和时间特征。

多策略的缺失值处理和异常值处理。

使用**集成（Ensembling）**技术以优化预测精度。

核心评估指标：均方根对数误差 (RMSLE)。

📌 2. 我的解决方案（My Approach）
以下流程完全基于本项目 Notebook 的真实步骤：

① 数据加载与EDA
使用 train.csv 和 test.csv 作为输入数据。

合并数据集进行统一的特征工程与预处理。

初步探索性数据分析 (EDA) 识别关键特征和异常值。

② 数据预处理与特征工程（Data Preprocessing & FE）
你在 Notebook 中做了：

针对不同特征（如 LotFrontage, Garage 相关列, MasVnrType 等）采用多策略进行缺失值填充。

对目标变量 SalePrice 进行对数变换以使其更接近正态分布，优化回归模型表现。

创建新的组合特征，例如总面积、总浴室数量等。

处理离群值（Outliers）。

③ 特征编码与缩放（Encoding & Scaling）
独热编码 (One-Hot Encoding)：对所有类别特征进行独热编码。

特征缩放 (Standard Scaling)：使用 StandardScaler 对数值特征进行标准化处理，以消除量纲影响，利于基于距离和梯度的模型。

④ 模型训练与比较（Modeling）
训练并比较了以下回归模型：

Linear Regression

Support Vector Regressor (SVR)

RandomForestRegressor

GradientBoostingRegressor

XGBoost Regressor

通过交叉验证选出各模型的最佳超参数。

⑤ 最终模型（Final Model: Voting Regressor 集成）
选择了多个表现优秀的基模型，并使用投票回归器 (Voting Regressor) 进行模型集成（Ensembling），充分结合不同模型的预测优势。

使用该集成模型生成最终提交文件 submission.csv。

📌 3. 文件结构（Repository Structure）
├── README.md ├── Housing Price.ipynb (我的解决方案 Notebook) ├── train.csv / test.csv ├── submission.csv └── kaggle_score.png

📌 4. 环境要求（Environment Requirements）
python 3.8+ pandas numpy matplotlib seaborn scikit-learn xgboost

📌 5. 如何运行（How to Run）
下载本仓库。

打开 Notebook：Housing Price.ipynb。

运行所有单元格。

会自动生成 submission.csv。

上传到 Kaggle 查看分数。

📌 6. 项目亮点（Key Highlights）
全流程机器学习回归项目。

涵盖了复杂的特征工程与多策略缺失值处理。

使用了独热编码和标准化缩放等关键预处理步骤。

最终采用强大的多模型集成（Voting Regressor）策略，显著提高预测精度。

Notebook 结构清晰，易于复现。
