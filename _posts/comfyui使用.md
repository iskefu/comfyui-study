---
created: 2024-04-03T00:00:00.000Z
---
# install

## download comfyui
```sh
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI
conda create -n comfyui  --noconfirm
conda activate comfyui
conda install python

```
## install requirements

```sh
pip install -r requirements.txt

# or

pip install -r requirements.txt -i http://mirrors.aliyun.com/pypi/simple/ --trusted-host mirrors.aliyun.com

# wait for a installation to complete
```
## download model

[Hugging Face – The AI community building the future.](https://huggingface.co)

[Civitai: The Home of Open-Source Generative AI](https://civitai.com)
### model directory

| 模型类型             | 放置路径示例                       | 描述                                |
| ---------------- | ---------------------------- | --------------------------------- |
| 大模型（Checkpoints） | `ComfyUI\models\checkpoints` | Stable Diffusion的主要模型文件，通常较大。     |
| VAE模型            | `ComfyUI\models\vae`         | VAE（Variational Autoencoder）模型文件。 |
| Lora模型           | `ComfyUI\models\loras`       | Lora微调技术相关模型文件。                   |
| plugins          | `ComfyUI\custom_nodes\`      | 插件目录，用于存放自定义节点。                   |
|                  |                              |                                   |
|                  |                              |                                   |
|                  |                              |                                   |
#### checkpoints
```sh
# wget -P models/checkpoints url
```
#### vae
```sh
# wget -P models/vae url
```
#### lora
```sh
# wget -P models/loras url
```
#### plugins
```sh
# git clone <repository-url> custom_nodes
git clone https://github.com/ltdrdata/ComfyUI-Manager.git custom_nodes/

# AIGODLIKE-ComfyUI-Translation

# ControlNet  
```
## run
```sh
python main.py
```
# TIPs

## 如何显示高质量预览

使用 --preview-method auto 启用预览。  
默认安装包含一种低分辨率的快速潜伏预览方法。要使用 TAESD 启用更高质量的预览，  
请下载  
Taesd_decoder. Pth（用于 SD 1. X 和 SD 2. X）  
和 taesdxl_decoder. Pth（用于 SDXL）模型，  
并将它们放到 models/vae_approx 文件夹中。

安装完成后，重启 ComfyUI 以启用高质量预览。

# USAGE
## basic

- Load Checkpoint 
	- 加载模型 ![LoadCheckpointWithConfig-BN6zB4MN.svg](https://www.comfyuidoc.com/assets/LoadCheckpointWithConfig-BN6zB4MN.svg)
	- 模型存放位置：`ComfyUI\models\checkpoints`
-  CLIP Text Encode(Prompt) 
	- ![CLIPTextEncodePrompt-hZy3NNU2.svg](https://www.comfyuidoc.com/assets/CLIPTextEncodePrompt-hZy3NNU2.svg)
	- 正向提示词
	- 反向提示词
-  Empty Latent Image
	- 设置图像大小
- KSmapler
	- seed
		- 种子
	- CONTROL after generated
		- 生存后种子变化
	- steps
		- 步数
	- cfg
	- sampler_name
		- 采用算法
	- scheduler
		- 调度算法
	- denoise
		- 初始噪声值
- Vae 
	- 变分自编码器
	- 图像处理
-  Save Image
### prompt tips
- 词的位置与其权重正相关
- 符号分割
- 基本结构
	- subject
	- environment
	- medium
	- style
		- when
		- who
		- what
		- where
## 辅助增强
- embedding
	-  转化 prompt 为机器理解的内部语言特征
	- usage
		- 在 prompt 中
		- `embedding:xxx`
- loRA![LoadLoRA-Bng2EN8f.svg](https://www.comfyuidoc.com/assets/LoadLoRA-Bng2EN8f.svg)
	- 微调，滤镜的意思
	- 连接、
		- 左：checkpoint
		- 右：clip, ksampler
	- 
## 额外功能
- iamge 2 image![](https://www.comfyuidoc.com/assets/img2imgExample-Xo6WpEPU.png)
	- add load image node
		- right click
		- all node 
		- image
	- add clip vision encode
		- ![CLIPVisionEncode-CftDdXV-.svg](https://www.comfyuidoc.com/assets/CLIPVisionEncode-CftDdXV-.svg)
		- encode image
		- right click
		- all node 
		- conditioning
	- add unclipconditioning node![unCLIPConditioning-DLHXFnff.svg](https://www.comfyuidoc.com/assets/unCLIPConditioning-DLHXFnff.svg)
		- 融合 text encode 和 image encode
		- right click
		- all node
		- conditioning
	- 
- upscale![LoadUpscaleModel-C74PIl6V.svg](https://www.comfyuidoc.com/assets/LoadUpscaleModel-C74PIl6V.svg)
	- 
