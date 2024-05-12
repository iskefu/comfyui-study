_发现一个问题_

我原封不动复制 c 站的参数下来在我的电脑上使用，出来的图片和作者不一样。

为此，我又在网上开启一个云 gpu 来再次生成这个参数的图片，

但是结果并不是和作者的一样而是和我的一样，所以, 我认为，这可能是由于作者的配置问题引起的，

比如能够影响图片的生成的 embedding ，lora, vae 等等没有给出的模型，
# 日漫赛博御姐
- this civitai pic:
![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/149d378e-ce16-4cab-b666-2b0afdaa71c1/original=true/00059-2425464473.jpeg)

- my generated pic:![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/8a42467f-a6d6-4c2f-8011-68940b810eb8/original=true/ComfyUI_00001_.jpeg)
- my generated pic with the cloud gpu :![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/b2581572-86b9-4414-8b50-9fccafdd506b/original=true/d55bbca18dbeda21aa44ef44fc32ebd9c163b1cc799d682d5057eb0243929b20.jpeg)
- 由此可见，我的本地和云端gpu好歹姿势是一样的，虽然生成的风格差别有点大，但是我生成的两个和C站作者差别也太大了。
- 经过浏览，作者的这个穿搭应该是启用了网站的一个lora,我忘记名字了
- 我用C站生成的图和作者的差不多，然后看到我C站使用的vae是kl-f8-anime2 vae ，而我使用的是vae-ft-mse-840000-ema-pruned 所以，这个问题解决了，包括一开始就找不到原因的案例一也差不多可以肯定就是这个原因了。
  
# 写实 风格 复刻
![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/a768b16f-41b0-4eb7-89f0-5f6dbdfb0687/original=true/00010-2503085764.jpeg)
我生成的:![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/0783e6f1-0353-417a-96d5-c1f72756289d/original=true/ef647bf8ac5d64bd67b7db82179b43aa127be085cd99f73250c5ca74349101be.jpeg)
自动瑟瑟，对比度过于浓了，

# lora 的组合使用
模仿源：[Image posted by Mazz\_W](https://civitai.com/images/718471)
![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/4c0ccb9b-8426-4e33-b4fe-bbca293efc32/original=true/Mazz_Earth_1440.jpeg)
这看起来难度有点大啊
不管
按流程：找模型，找 lora 模型，写 prompt，出图
- 模型：[SDVN7-NijiStyleXL - v1 | Stable Diffusion Checkpoint | Civitai](https://civitai.com/models/123307/sdvn7-nijistylexl?modelVersionId=155870) 看起来一点也不相关
- lora：[extremely detailed (no trigger) - sliders.ntcai.xyz - v1.0 | Stable Diffusion LoRA | Civitai](https://civitai.com/models/229213/extremely-detailed-no-trigger-slidersntcaixyz?modelVersionId=258687)
- prompt：一个女孩，站在龙头上，沙尘漫天，在空中，
- 出图：![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/d443f2a0-737a-4da5-a1c5-bb70c488fe89/original=true/2b61b7ef7e40855508fc99f980860268077172e7c47136db4b4d8aec11fa43e1.jpeg)
- 评价：差远了，
- 出图：![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/713a4675-1df1-4f80-b62d-0a5911764719/original=true/ed4e640ced8e6c45d7b221b35258b2c55f33f23006bf934996ed5b1dd7094433.jpeg)
- 评价：同上，
- 出：![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/8c5b88f5-170f-4212-9bbe-7da8db30d7b1/original=true/252864069edad0d7d0751c27ff82cd60a4acf91fc62032430afdcd10330e398f.jpeg)
- ps: face is oh my god 
- ![](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/68c04364-5ee1-4d24-afa7-792689a68810/original=true/28c74d6e4848cf28ba2df29e679a09c460574b953dacb977d3ceb65384b75845.jpeg)
- ps: just so so, 不过细节还可，

- 不管怎么改 prompt, 女人就是不骑在龙头上，而且龙占了 主体，而女人是却成了点缀，
- 所以，这个复刻应该算是 失败的，要好好 学一下怎么写 prompt,
- 还有，好好研究怎么让细节更加惊叹，
- 和原图还是有很大的差别的，烟雾和沙尘的细节，光影的艺术，等等，人物的刻画也是，那个主角太有生命力了
- 


