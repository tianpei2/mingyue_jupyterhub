# mingyue_jupyterhub

## 1. 激活conda
登入linux，在~目录下
```
source .bashrc
```

## 2. conda环境

### 1. 查看已有环境及目录
```
conda env list
```
### 2. 配置环境(例:python3.7)

公共：
```
conda create -n envName python=3.7
```
私人(新建环境文件夹envs)：
```
conda create -p ~/envs -n envName python=3.7
```
### 3. 切换环境
```
conda activate envName
```
### 4. 在已有环境里安装package

切换到想安装的环境
```
conda activate envName
```
然后安装package(例:tensorflow-gpu 2.4)
```
conda install tensorflow-gpu==2.4
```
### 5.在新环境中安装kernel
```
conda install ipykernel
```
## 3. 将conda环境写入jupyter的kernel中

```
python -m ipykernel install --user  --name envName --display-name "kernelName"
```

