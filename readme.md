# 安装

```
# 创建环境
conda create -n geotransformer python==3.8
conda activate geotransformer

# 安装mamba
conda install mamba -c conda-forge

# 安装pytorch、torchvision、cudatoolkit
mamba install pytorch=1.7.1 torchvision cudatoolkit=11.0.221 -c pytorch

# 安装pytorch3d
wget https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch3d/linux-64/pytorch3d-0.6.1-py38_cu110_pyt171.tar.bz2
conda install -c local pytorch3d-0.6.1-py38_cu110_pyt171.tar.bz2

# 安装程序包和其他依赖
pip install -r  requirements.txt -i https://pypi.doubanio.com/simple/
python setup.py build develop
```

# 训练

使用下面命令训练

```
python experiments/geotransformer.modelnet.rpmnet.stage4.gse.k3.max.oacl.stage2.sinkhorn/trainval.py
```

开始训练

![20230523105550](https://raw.githubusercontent.com/skykone1/images/main/20230523105550.png)

# 测试
使用下面命令测试

```
python experiments/geotransformer.modelnet.rpmnet.stage4.gse.k3.max.oacl.stage2.sinkhorn/eval_bop.py
```

开始测试
![20230523122734](https://raw.githubusercontent.com/skykone1/images/main/20230523122734.png)
