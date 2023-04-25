# Lora模型

英文全称Low-Rank Adaptation of Large Language Models（大语言模型的低阶适应）

LoRA的做法是，冻结预训练好的模型权重参数，然后在每个Transformer（Transforme就是GPT的那个T）块里注入可训练的层，由于不需要对模型的权重参数重新计算梯度，所以，大大减少了需要训练的计算量。目前最新的stable-diffusion已经原生支持Lora了，直接move模型进行就好了。

这个特性意味着大家也可以fine-tune训练微调，降低参数门槛了！

> 怎么知道模型是base模型还是Lora 模型呢?
>
> 根据Type和文件大小就可以区分，文件很大基本都是base model
>


## 训练案例

- [如何使用8G以下显卡训练Stable diffusion可用的Lora模型](https://zhuanlan.zhihu.com/p/609632788)
  
- [stable diffusion 换装 换模特 想怎么组装都可以](https://www.youtube.com/watch?v=TK31N_vHVJY)

- [我用AI重构了张颂文的狂飙人生，看Lora怎么样训练模型，AI真是把他的样子学到骨子里了！](https://www.youtube.com/watch?v=RA0wUfEOb2A)

- [Stable Diffusion lora训练AI绘画高级自定义定制服饰教程](https://www.youtube.com/watch?v=9xhDWU8Vb6E)