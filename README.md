# 2024-Task2 数据可视化项目

##  项目简介
通过Anaconda环境管理依赖，使用Git进行版本控制。主要功能：
- 生成自定义学号相关的相位折线图
- 自动保存可视化结果
- 支持命令行参数配置

## 文件说明
2024-Task2-wujiayi2/
├── src/                 # 源代码目录
│   ├── plot.py          # 主程序脚本
├── images/              # 输出图像目录
├── docs/                
│   └── summary.md       # 项目总结
├── environment.yml      # Conda环境配置
├── README.md            # 本项目说明
└── .gitignore           # Git忽略规则

## 部署步骤
### 环境配置
```bash
# 创建Conda环境
conda env create -f environment.yml

# 激活环境
conda activate plot_env

# 安装Python依赖
pip install -r requirements.txt

# 基本运行
python plot.py

git checkout -b feature-功能
