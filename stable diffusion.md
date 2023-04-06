# why study

我想找生成ai方面的工作，找了一堆的招聘信息里面提到了gan，vae，diffusion，stable diffusion，nerf这些内容

问谷歌，b站，知乎，chatGPT（实时）好友，

后来慢慢来了解了这些内容中stable diffusion最强.而且很多已经落地了。所以你要学他。

# what 

先查询他是什么 chatGPt，github，谷歌，b站，知乎

22年发布的StabilityAI的Stable Diffusion是一个开源模型，是一个文生图底层大模型。[**CompVis**](https://github.com/CompVis)、 📘[**Stability AI**](https://stability.ai/)和 📘[**LAION**](https://laion.ai/)开源

和他同层次的还有

[**Midjourney**](https://www.midjourney.com/home/) 由同名研究实验室开发（不开源）

[**DALL·E2**](https://openai.com/dall-e-2/)由 📘[**OpenAI**](https://openai.com/)开发（不开源）2021年1月，OpenAI发布了两个连接文本与图像的神经网络：DALL・E和 CLIP。DALL・E可以基于文本直接生成图像，CLIP能够完成图像与文本类别的匹配。DALL・E是基于GPT-3的120亿参数版本实现的。

由于开源关系你就应该知道学那一个了

# how study

然后想一下，公司人家需要什么，

## 应用

1首先，知道怎么用代码最简单的调用他实现文生图，即能简单的应用

首先你应该先使用，去github 或者hugging face hub上看一下应该会有直接能用的。

github

从[CompVis](https://github.com/CompVis)/**[stable-diffusion](https://github.com/CompVis/stable-diffusion)** 上看到Stable Diffusion was made  by [Stability AI](https://stability.ai/) and [Runway](https://runwayml.com/) 。并且看到一篇论文。

然后看到他们对模型版本一些说明。可以看出这个是最早的模型，然后提供了简单调用案例，其他说明。所以你就可以实现第一步了

hugging face hub

上面有许多模型版本，你不知道那一个合适。

## 理论

看懂一下数学理论和结构

YouTube看有没有把。

或者google 上找 用 from scrath。下面的就是朋友通过这种方式找到的

https://scholar.harvard.edu/binxuw/classes/machine-learning-scratch/materials/stable-diffusion-scratch。好友发的

内容如下

扩散模型的原理。
用UNet模型建立图像的得分函数模型 
通过上下文的词语嵌入来理解提示 
让文字通过交叉注意影响图像 
通过增加一个自动编码器来提高效率 
大规模的训练。

终于找到了stable diffusion的组成结构。可以根据课件开始学习了。



## 源码

看懂源码，有自己的想法能改进能力，根据已有的论文或者自己能力改进某个方向，然后应用部署

查stable diffusion的github，

1从[CompVis](https://github.com/CompVis)/**[stable-diffusion](https://github.com/CompVis/stable-diffusion)** 上看到Stable Diffusion was made  by [Stability AI](https://stability.ai/) and [Runway](https://runwayml.com/) 。并且看到一篇论文。

然后看到他们对模型版本一些说明。明显这个里就不适合学习，因为没讲理论和结构



然后点击进去查看这两个公司链接

2 [Stability AI](https://stability.ai/) 你看完封面你就会看到一个指向stable diffusion的github， https://github.com/Stability-AI/stablediffusion 

提供多个版本的stable diffusion v2 这些是进一步优化的。也说了最初的模型是上面那一个。然后说明一些stable diffusion v2 的优化和本地使用，网络使用。



3Runway 就会看到两个相关链接在最下面，第一个进去https://research.runwayml.com/publications/high-resolution-image-synthesis-with-latent-diffusion-models 提供论文和代码。

第二个直接是一些相关研究



## 追新

3追最新的应用和论文，

从youtube，谷歌，chatGPt，b站上找，从知乎上找，从csdn上找



# stable diffusion

## what 

一个文生图的模型

## 应用

案例应用

直接在kaggle 上跑一下，看是否能生成你想要的图片。直接看kaggle上的stable diffusion。





构造他需要什么 前面的他需要构造的，后面是要用的模型。构造一个好的生成模型需要这么多

生成新的图片使用         正向/反向扩散（Forward/Reverse Diffusion）

 Way to link text and images                Text-image representation model文本-图像表示模型（GAN-INT-CLS）

Way to compress images                Autoencoder

Way to add in good inductive biases（添加良好的归纳偏差的）             U-net architecture + ‘attention’

组合在一起就是这样	

![截屏2023-04-02 下午9.11.37](../../../../../计算机学习/应用层/unity/unity-VR/picoVR/picoVR-picture/截屏2023-04-02 下午9.11.37.png)

潜空间（Latent Space）语义地图（Semantic Map）

去噪步骤（Denoising Step）交叉注意力（Cross-Attention）跳跃连接（Skip Connection）Concat（连接

