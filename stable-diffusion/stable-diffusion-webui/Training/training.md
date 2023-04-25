# 模型训练

几种stable-diffusion的fine-tune技术，主要用于让模型通过少量样本的学习，掌握训练数据未出现的一些新概念，比如人脸、宠物和画风等。

![训练方法](https://pic3.zhimg.com/80/v2-66b8506e19ccc32cfc2c73acf99df882_1440w.webp)

- Lora：冻结预训练好的模型权重参数，然后在每个Transformer（Transforme就是GPT的那个T）块里注入可训练的层，由于不需要对模型的权重参数重新计算梯度，所以，大大减少了需要训练的计算量（目前最focus的地方）显存8GB以上

- Hypernetwork：额外辅助神经网络预测原网络的新权重。一般为.pt后缀格式，大小一般在几十兆左右。显存6GB以上

- Textual Inversion：创建另外的Text2embedding，捕捉新prompt 概念。显存12GB以上

- Dreambooth：微调扩散至模型。显存12GB以上

## 训练教程

1. [訓練AI來製作頭像，偷偷為你女友做個頭像來給她驚喜吧~](https://www.youtube.com/watch?v=SDNB07J3fFE)

2. [stable diffusion 换装 换模特 想怎么组装都可以](https://www.youtube.com/watch?v=TK31N_vHVJY)

3. [[AI繪圖速成懶人包] (粵語繁中)新版LoRA教學 | 8張圖就能成功? | 手把手超詳細 |](https://www.youtube.com/watch?v=is7TNhPVJEo)