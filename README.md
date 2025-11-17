# 基于Google Earth Engine的单景SAR影像洪水提取

本仓库包含论文 **"[这里填写您的论文标题]"** 的官方源代码。该分析在Jupyter Notebook环境中，利用Python和Google Earth Engine (GEE)平台实现。

## 核心算法

代码的核心逻辑在 `单图像分割.ipynb` 文件中，主要实现了两种分割策略：

1.  **自适应提取**: 结合在自动检测的候选框内使用局部阈值和在框外使用全局平均阈值的策略。
2.  **混合格网分块分割**: 将研究区划分为规则与不规则相结合的网格，并为每个网格单元分配最优阈值进行分割。


## 运行环境要求

### 1. Google Earth Engine 账户
您必须拥有一个Google Earth Engine账户，并在您的本地机器上完成认证。

### 2. GEE资产 (Asset)
本分析需要访问一个存储在GEE上的研究区矢量边界。请确保您有权限访问以下资产：
`projects/geemap-441216/assets/roi_sci_valencia_small`

### 3. Python 依赖库
所有必需的Python库都记录在 `requirements.txt` 文件中。请使用以下命令进行安装：
```sh
pip install -r requirements.txt
```

## 如何运行

1.  克隆本仓库到您的本地计算机。
2.  使用 `pip` 安装 `requirements.txt` 中列出的所有依赖项。
3.  确保您的GEE账户已在本地认证。
4.  打开 `单图像分割.ipynb` 文件，并按顺序执行所有代码单元格。

## 仓库结构

- `单图像分割.ipynb`: 包含所有分析和可视化代码的核心Jupyter 函数。
- `requirements.txt`: 项目所需的Python依赖库列表。
- `README.md`: 本说明文档。