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

## 软件展示

![image](https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/a310c688-14af-4064-94f1-90e0deba830c)
### 启动程序
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/5b93383f-7876-476c-ac7e-f8154812e29a">

### 未存在数据库的用户无法通过登录验证
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/249698e7-ed14-4b32-ad07-b1e64d4d3c45">

### 注册页面
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/6bdf38b9-e836-4006-8722-a8c8889279b4">

### 已注册用户无法再次注册
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/4a5404c1-d018-4966-98fc-486a3a42b001">

### 新用户注册成功
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/f2100036-f500-4ad2-a23c-30b80bafeff4">
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/6fb0b270-2e10-44e3-baeb-083fcfacdc46">

### 新用户登录成功
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/41ecccb4-f182-4ebd-95a3-b8d1ef8a466c">

### 输入数据使用预测功能
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/d401dd84-ddc4-4ddc-b219-4053bbccedcc">

### 预测成功：真实值为（0，0）预测值为（0.06，0.16）
<img width="440" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/ddc0bc5c-8940-40a5-ad93-0c3b8164c942">
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/0c940ca2-0d5c-4f69-8d3b-00af7ed76ce1">

### 进入数据分析页面开始数据分析
<img width="440" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/56421a66-3e86-40cd-8626-50a87ad27beb">

### 分析完成开始语音播报
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/5a464a2f-adb6-4ff2-a28e-28ea6ea70d26">

### 语音播报完成，展示播报的文本，同时可以通过左边的音频进行重新播放和进度条跳转。
<img width="440" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/00df7014-76da-4fbc-aae3-9831961cab8e">

### 可以进入数据分析图页面查看本次预测数据在全年的太阳光照数据分布中的具体位置。
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/3680b1ef-7e26-4432-81b5-accd181d2904">

### 聊天框可以使用聊天模型
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/4e247408-8d88-44f2-bc6e-06dc7ec3fedc">
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/da57ed99-ad43-4faa-b3c8-afe03e10caff">

### 聊天模型会使用语音和文本进行回复
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/90cd8b12-c0af-4647-8dcc-fea6304b4b73">

### 开启语音对话功能
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/9a432593-69d3-41e3-8133-536d34b9b30a">

### 用户通过语音识别同聊天进行进行交流
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/4884490e-b345-42e0-8aab-b783110a5a39">
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/a89f6ed9-9eea-49ad-81e7-930360289ea7">

### 本项目还提供了我们开源的仓库地址
<img width="441" alt="image" src="https://github.com/xiayuwenshan/-Python-Web-/assets/104626642/6afb9e01-860e-4eef-ad6e-8e9ee2f4435a">


















