# 环境搭建
pip install bitsandbytes>=0.39.0
## 安装xtuner
https://github.com/InternLM/xtuner.git
切换到0.2.3tag

cd xtuner
pip install -e '.[deepspeed]'

降级transformers到4.56版本

# 数据准备 转换数据，切分训练集测试集
python .\data_prepare\data_spilit.py

# 训练命令
nohup xtuner train ~/projects/xtuner_finetune/qwen1_5_1_8b_chat_qlora_alpaca_e3.py \
> ~/projects/xtuner_finetune/xtuner_train.log 2>&1 &
