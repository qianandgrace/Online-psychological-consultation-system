# 环境搭建
## 安装torch 速度过慢可以先下载到本地
pip install torch==2.6.0 torchvision==0.21.0 torchaudio==2.6.0 --index-url https://download.pytorch.org/whl/cu126
## 安装xtuner
https://github.com/InternLM/xtuner.git
切换到0.2.3tag

#数据准备 转换数据，切分训练集测试集
python .\data_prepare\data_spilit.py
