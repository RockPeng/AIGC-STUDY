# Models 模型

- 真人模型chilloutmix

- 经典的二次元模型Anything V3
  
## 基础模型

### checkpoint

完整模型的常见格式，模型体积较大，一般单个模型的大小在3~7G 左右，通常称之为基础模型（基模 base model）。常见的模型chilloutmix_NiPrunedFp32Fix 就是4G。

- [chilloutmix_NiPrunedFp32Fix](https://huggingface.co/naonovn/chilloutmix_NiPrunedFp32Fix/tree/main)
  
- [Realistic Vision V2.0](https://civitai.com/models/4201/realistic-vision-v12)
### VAE

负责将潜空间的数据转换为正常图像，就是改变滤镜和色彩。有一些checkpoint merge会自带VAE


## Lora模型

- [koreanDollLikeness_v15](https://huggingface.co/amornlnw7/koreanDollLikeness_v15/blob/main/koreanDollLikeness_v15.safetensors)
  
## ControlNet模型
  
特别提到一下，ControlNet的作者是中国人！！！张吕敏大佬（致敬）

> [ControlNet项目链接](https://github.com/lllyasviel/ControlNet)
>
> [Stable Diffusion webui扩展github项目链接](https://github.com/Mikubill/sd-webui-controlnet)
>

ControlNet模块是用于img2img 的精准控制的（后面实战会根据其中的open pose模块进行实验），以插件的形式存在于stable-diffusion中

ControlNet 把每一种不同类别的输入分别训练了模型，目前公开的有下面8个。分别是：canny，depth，hed，mlsd，normal，openpose，scribble，seg。  

- canny：边缘检测，属于比较通用的模型

- hed：HED边缘提取，跟canny类似

- scribble：手稿模型，随手涂鸦然后生成一个精美的画面

- openpose：姿势控制专用模型，用于人物动作

- normal：模型识别，适用于建模

- depth：深度检测，提取深度图

- seg：语义分割识别

- mlsd：线段检测，一般用于建筑、物体的检测，常用于室内装潢，建筑设计

### 辅助工具

- [OneFormer: One Transformer to Rule Universal Image Segmentation](https://huggingface.co/spaces/shi-labs/OneFormer)

### 教程

- [NEW ControlNet for Stable diffusion RELEASED! THIS IS MIND BLOWING!](https://www.youtube.com/watch?v=vFZgPyCJflE)

- [NEXT-GEN NEW IMG2IMG In Stable Diffusion! This Is TRULY INCREDIBLE!](https://www.youtube.com/watch?v=OxFcIv8Gq8o)

- [Transform Your Sketches into Masterpieces with Stable Diffusion ControlNet AI - How To Use Tutorial](https://www.youtube.com/watch?v=YJebdQ30UZQ)

- [A1111 WebUI用 ControlNetの導入方法備忘録](https://miro.com/app/board/uXjVPnNbqTA=/)

