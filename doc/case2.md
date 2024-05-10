# 琉璃效果复现

## 详情：
[IMAGE TO 💎JADE STYLE | ComfyUI Workflow](https://openart.ai/workflows/xiongmu/image-to-jade-style/BRuUXjQhMaLu0dPOvZHD)
## 准备
### checkpoint 模型：
[Juggernaut XL - Jugg\_X\_RunDiffusion\_Hyper | Stable Diffusion Checkpoint | Civitai](https://civitai.com/models/133005/juggernaut-xl)

### lora模型：

- glazed girl

https://civitai.com/models/140681/xlglazed-girl-jade-glass-ceramic-and-other-textures

- sdxl_glass

https://civitai.com/models/11203/glass-sculptures

- jade

https://civitai.com/models/148809/sdxl-or-jadeite-cabbage-or-chinese-treasure
### 放大模型
[4x-Ultrasharp - 4x-UltraSharp v1.0 | Stable Diffusion Upscaler | Civitai](https://civitai.com/models/116225/4x-ultrasharp)
## 开始
###  打开工作流
#### - 安装缺失的节点
```sh
cd  custom_nodes 
#  ComfyUI's ControlNet Auxiliary Preprocessors

git clone https://github.com/Fannovel16/comfyui_controlnet_aux/
cd comfyui_controlnet_aux
pip install -r requirements.txt

# was-node-suite-comfyui 
cd ..
git clone https://github.com/WASasquatch/was-node-suite-comfyui/
cd was-node-suite-comfyui
pip install -r requirements.txt

git clone https://github.com/EllangoK/ComfyUI-post-processing-nodes/
git clone https://github.com/Suzie1/ComfyUI_Comfyroll_CustomNodes.git
git clone https://github.com/cubiq/ComfyUI_IPAdapter_plus.git
git clone https://github.com/sipherxyz/comfyui-art-venture.git
git clone https://github.com/Kosinkadink/ComfyUI-Advanced-ControlNet.git
git clone https://github.com/rgthree/rgthree-comfy.git
git clone  https://github.com/shadowcz007/comfyui-mixlab-nodes.git
```
