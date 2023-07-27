# StarGLM

## 项目描述

我们整合了司天工程相关的语料数据与知识库资料，训练得到了天文大语言模型StarGLM(ChatGLM for Variable Star)。

以期缓解大语言模型在部分天文通用知识和前沿变星领域的幻觉现象，为接下来可处理天文多模态任务、部署于望远镜阵列的观测Agent——司天大脑（数据智能处理）打下基础。

## 功能展示

![监督微调](example/example1.png)

<br>

![链接知识库](example/example2.png)

<br>

![链接SD](example/example3.png)

<br>

![多模态探索](example/example4.png)

<br>

![未来计划](example/example5.png)
## 安装指南
 
1.基础模型安装：Releases-Checkpoint.7z存有监督微调后的Lora权重，可根据配置条件(建议在搭载GPU的环境运行)，参考ChatGLM2-6B官方教程加载,或直接使用Wenda(闻达)。

  模型文件组成：

  Checkpoint 

    ├── adapter_config.json
    
    └── adapter_model.bin

2.链接知识库/StableDiffusion:建议使用Wenda(闻达)实现，基于StarGLM，能够进行多种天文相关的文本处理、知识库回答、AI绘画等任务。

(注：考虑到版权因素，暂不直接提供知识库文件，经典书籍可参考example/books，感谢沈长安（一只张秀）同学提供。变星领域相关知识，将在司天-变星知识图谱完善后一同发布。StableDiffusion使用的基模型与Lora权重见“使用/推荐的相关项目”)
## 司天项目介绍

当今天文学已经从刻画静态宇宙发展到认识动态宇宙。对宇宙空间中任何时间变化加以研究的时域天文学，将揭示各类天体的变化、发现和探索新天体、新现象并开拓新的理论空间，已成为天文和天体物理界最活跃和最具突破性的前沿领域之一。高效搜寻和监测天体动态事件需要大视场、多波段和高频次的时域巡天，高性能观测设备与能充分发挥设备观测能力的优质天文台址缺一不可。司天工程是我国天文学家面向时域天文学所提出的“十五五”天文重大基础设施，一期计划在国内多个优选观测台址布置54台（18组）口径1米级的大视场望远镜，组成多波段同时监测网络，每30分钟完成1万平方度天区的高精度三色“凝视”巡天。司天的采样频率比全球其它巡天项目高近两个量级，将突破目前探测时标的限制，在新的空域和时域下发现大批新天体、新现象，在宇宙极端高能爆发源、引力波电磁对应体、系外行星和太阳系天体等理论和观测研究中形成新的突破，在“两暗一黑三起源”等重大科学问题研究以及地球文明灾难预警等国家空间安全问题方面发挥重要作用。

![sitian](example/Sitian.png)

其中司天"大脑"作为数据智能处理中枢，需要适配于天文的AI工具。StarGLM作为其备选方案，在使用大模型整合天文知识的同时，探索多模态解决具体天文问题的可能性。
## 许可证信息

项目源码遵从Alpaca 2.0，ChatGLM2-6B的模型权重使用需遵从相应许可。

## 使用/推荐的相关项目

- THUDM/ChatGLM2-6B: ChatGLM2-6B: An Open Bilingual Chat LLM | 开源双语对话语言模型 (github.com) 
- wenda-LLM/wenda: 闻达：一个LLM调用平台。目标为针对特定环境的高效内容生成，同时考虑个人和中小企业的计算资源局限性，以及知识安全和私密性问题 (github.com) 
- THUDM/VisualGLM-6B: Chinese and English multimodal conversational language model | 多模态中英双语对话语言模型 (github.com) 
- hiyouga/ChatGLM-Efficient-Tuning: Fine-tuning ChatGLM-6B with PEFT | 基于 PEFT 的高效 ChatGLM 微调 (github.com) 
- BelleGroup (BELLE Group // Be Everyone's Large Language model Engine) (huggingface.co)
- PlexPt/chatgpt-corpus: ChatGPT 中文语料库 对话语料 小说语料 客服语料 用于训练大模型 (github.com)
- YeungNLP/firefly-train-1.1M · Datasets at Hugging Face
- XueFuzhao/InstructionWild (github.com)
- Instruction-Tuning-with-GPT-4/GPT-4-LLM: Instruction Tuning with GPT-4 (github.com)
- rexwang8/stellar-diffusion · Hugging Face
- 光芒-极光｜LiblibAI
## To do list

### 大语言模型（科普方式）

- [ ]  在相关材料上进行二次预训练，扩充天文知识。
- [ ]  调整监督微调中，通用数据和专业数据的比例，缓解灾难性遗忘问题。
- [ ]  通过人工反馈的强化学习，进一步提升模型性能。
- [ ]  通过特定数据集微调，提升模型总结能力，进一步适配知识库。
- [ ]  完成司天-变星知识图谱，与模型链接，进一步降低变星领域的幻觉现象。

### 专业多模态（科研工具）

- [ ]  开源在变星光变曲线上训练的VisualGLM微调权重
- [ ]  继续训练输入/输出视觉编码器/解码器，提升在天文专业领域的多模态能力。

### 观测Agent（司天大脑）

- [ ]  结合CodeGeeX2-6B工作，提升模型在天文领域的编程能力。
- [ ]  考虑通过工具学习，链接相关天文专业工具。
- [ ]  尝试Agent相关工作，验证作为司天大脑备选方案的可行性。

## 引用
如果这篇工作对你有帮助，请引用：

@Misc{chatglm-for-variable-star,

  title = {StarGLM},
  
  author = {YuYang Li, CunShi Wang, MengWei Qu, JiFeng Liu, Yu Bai, Roberto Soria},
  
  howpublished = {\url{https://github.com/Yu-Yang-Li/StarGLM}},
  
  year = {2023}
  
}
