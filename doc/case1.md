# I want milk 
_逛C站的时候看到的一张图片，不错,  决定复刻_
![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/76f34435-346c-405b-b54e-3315fe33cd9a/original=true/00000-2576117923.jpeg)

_果然性是人类第一动力_

- 图片url：[Image posted by xiaoxiaohuiji](https://civitai.com/images/10880329)

- 所包含模型url：
	- type：checkpoint：[CyberRealistic - v4.2 | Stable Diffusion Checkpoint | Civitai](https://civitai.com/models/15003/cyberrealistic)
	- tpye：lora：[Add More Details - Detail Enhancer / Tweaker (细节调整) LoRA - v1.0 | Stable Diffusion LoRA | Civitai](https://civitai.com/models/82098/add-more-details-detail-enhancer-tweaker-lora?modelVersionId=87153)
	- type：lora ：[長乳locon / hanging breasts locon - v1 | Stable Diffusion LyCORIS | Civitai](https://civitai.com/models/16202/locon-hanging-breasts-locon?modelVersionId=19135)
	- type：emmbedded：[epiCPhoto - epiCPhoto | Stable Diffusion Embedding | Civitai](https://civitai.com/models/195911/epicphoto?modelVersionId=220262)
- 下载模型，放在对应位置
- 启动comfyui 
- 打开本地UI http://127.0.0.1:8188/
- 把参数复制过来
- 开始炼丹
- 参数：工作流： [comfyui-study/data/case1.json at main · iskefu/comfyui-study · GitHub](https://github.com/iskefu/comfyui-study/blob/main/data/case1.json)
	- _没有 下载他 prompt 里的 lora，只是加载了他给出的 lora 连接_
- 生成效果：![](https://s2.loli.net/2024/05/09/qjWIfMpGV9JunXe.png)
- 分析结果：
	- 眼睛不自然，（他的 prompt 里包含很多 lora 我只下载他给出的两个 lora ，初步猜测可能是这个引起的 ）
	- 清晰度不够，（没有使用 upscale 放大图片，可能是这个原因）
	- 没有大白腿，（可能是没有使用 lora）
	- 奶子下坠太厉害了，（可能是没有使用 lora）
- 改：
	- 清晰度问题就是没有使用 upscale ，
		- 加载 upscale，下载模型 : 放在 `model/upscale_models`, vaedecode 节点后面插入：图像--放大---图像通过模型放大。图像通过模型放大节点的放大模型连接到：加载器--放大模型加载器。
	- 多张图片都不理想，可以考虑为采样算法带a,不完全复现图片。

	
- 

- 
- 
- 换个模型：![](https://s2.loli.net/2024/05/09/RAe3QOk1wmBngNX.png)
- 得下面效果：![](https://s2.loli.net/2024/05/09/EyR4Dfq95NLpOTG.png)
- 再换个模型：![](https://s2.loli.net/2024/05/09/GWBk4XlUosvQhb9.png)
- 对比起来，模型的重要性不容忽视。
- 除此之外，手部有点古怪，图片不够清晰，
## 总结
- 模型的选择是图片输出的主要来源，也是影响输出效果的关键因素。
