# -Python-Web-
# 基于Python Web的太阳直射辐照和散射辐照智能预测系统设计

## 感谢xiayuwenshan提供的web搭建和mysql数据库，感谢whoiswennie提供的数据分析、gptAPI和语音模型。

## 使用教程（windows）

### 环境搭建
#### 经测试我们发现在python=3.10运行稳定
```python
conda create -n your_env_name python=3.10
```
```python
pip install -r requirement.txt
```
#### 后续若提示缺少某些库可以自行下载
### 下载预训练模型
#### 本项目预训练模型包括，太阳光照数据预测模型，bert-vits2中文语音合成模型，Bert模型
##### bert中文模型：https://huggingface.co/hfl/chinese-roberta-wwm-ext-large
###### 只需要下载最大的那三个模型文件，然后放在Bert-VITS2\bert\chinese-roberta-wwm-ext-large目录中
##### bert-vits2中文语音合成模型（可替换）：待传
###### 下载后将config.json放在Bert-VITS2\configs进行替换，另外两个pth文件放在Bert-VITS2\logs\huan内
##### 太阳光照数据预测模型：待传
###### 改文件放在项目根目录即可（与app.py同路径）

### 运行本项目
#### 打开两个Anaconda Powershell Prompt，运行
```python
conda activate your_env_name
```
#### （第一个Anaconda Powershell Prompt）cd至本项目目录后
```python
cd py/Bert-VITS2
python my_server.py
```
#### （第二个Anaconda Powershell Prompt）cd至本项目根目录
```python
python app.py
```
#### ctrl+点击app.py提供的本地端口地址即可
