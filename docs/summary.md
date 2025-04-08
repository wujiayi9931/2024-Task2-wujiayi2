## 所使用的 Git、Conda 命令并解释
# 创建一个名为test_env的虚拟环境（使用Python 3.9作为示例）
conda create -n test_env python=3.9

# 激活环境
conda activate test_env

# 安装指定的库
conda install numpy pandas matplotlib

conda create -n plot_env python=3.8

conda activate plot_env

# 导出环境依赖为 environment.yml 到本地仓库中
conda env export > environment.yml

# 切换回dev分支
git checkout dev

# 合并功能分支（保留合并记录）
git merge --no-ff feature-enhancement -m "merge: 合并参数功能到dev"

# 推送更新
git push origin dev

# 查看分支图谱
git log --graph --pretty=format:'%h -%d %s (%cr)' --abbrev-commit

## Anaconda 环境配置的优点与难点
-优点：隔离项目依赖，方便环境复现
-难点：环境导出需指定跨平台，SSL证书问题需`conda config --set ssl_verify false`

## Git 分支管理中的经验
# 创建并切换分支
   git checkout -b dev
# 强制推送（解决rejected错误）
   git push -f origin dev
# 合并分支（保留历史）
   git merge --no-ff feature-plot
# 需要返回主分支
   git checkout main

## 部署过程中遇到的问题及解决方案
子模块问题：重新搭建一个仓库，不使用子模块
