# mingyue_jupyterhub

## 1. 激活conda
登入linux，在~目录下
```
source .bashrc
```

## 2. conda环境

### 查看已有环境及目录
```
conda env list
```
### 配置环境（例:python3.7）

公共：
```
conda create -n envName python=3.7
```
私人（创建 ~/envs）：
```
conda create -p ~/envs/envName python=3.7
```
### 切换环境

公共：
```
conda activate envName
```
私人：
conda activate ~/envs/envName

### 切换环境后，在已有环境里安装package

查看当前环境下packages
```
conda list
```
然后安装package（例:tensorflow-gpu 2.4）
```
conda install tensorflow-gpu==2.4
```
### 在新环境中安装kernel
```
conda install ipykernel
```
## 3. 将conda环境写入jupyter的kernel中

```
python -m ipykernel install --user  --name kernelName
```

