# ControlNet
参考网址：https://www.comfyuidoc.com/zh/Examples/controlnet/

## 准备工作
- 下载controlnet 插件
- 下载模型 [stablediffusionapi/anything-v5 at main](https://huggingface.co/stablediffusionapi/anything-v5/tree/main/safety_checker)
- 下载 controlnet 涂鸦模型
	-[control\_v11p\_sd15\_scribble.pth · lllyasviel/ControlNet-v1-1 at main](https://huggingface.co/lllyasviel/ControlNet-v1-1/blob/main/control_v11p_sd15_scribble.pth)
- vae：[vae-ft-mse-840000-ema-pruned.ckpt · stabilityai/sd-vae-ft-mse-original at main](https://huggingface.co/stabilityai/sd-vae-ft-mse-original/blob/main/vae-ft-mse-840000-ema-pruned.ckpt)
### 涂鸦 ControlNet
  - 加载工作流：
    - 下载图片
    - comfyui里加载图片
    - 复现成功
    - ![](https://s2.loli.net/2024/05/10/FT8PVNrhq7tnMGu.png)
- 使用 T 2 I-适配器
	- 将Load ControlNet Model 改为Load ControlNet Model (diff)
	- 左侧连接 checkpoint 的model
### 姿势 controlnet
下载模型：
下载 controlnet 模型：[control\_v11p\_sd15\_openpose.pth · lllyasviel/ControlNet-v1-1 at main](https://huggingface.co/lllyasviel/ControlNet-v1-1/blob/main/control_v11p_sd15_openpose.pth)
复现：![](https://s2.loli.net/2024/05/10/ZH4gXtAIGT6xSfn.png)
