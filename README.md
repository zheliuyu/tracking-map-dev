# 一、简介
tracking-map用于跟踪pt-ecosystem小组在Ascend NPU适配一些热门生态工具的进展。

****非常感谢这些优秀的生态工具能接受我们的PR**



# 二、项目清单
## 24年Q4
### 1、基于transformers、llama-factory、openMind做的一系列微调指导
- [以huggingface-transformers为例，创建一个可供使用昇腾原生支持三方套件的环境](https://modelers.cn/models/PNP/Start-Create-Env-Transformers)
- [以llama-factory为例，快速使用Qwen2.5-7B-Instruct模型完成一个微调任务](https://modelers.cn/models/PNP/Llama-Factory-Quick-Start)
- [使用昇腾原生支持生态库llama-factory做法律垂域模型微调](https://modelers.cn/models/PNP/Enhance-Llama-Factory-SFT-Law)

### 2、后来，这系列文章被整合，并发到了官网公众号宣传
 - 文章标题：[基于应用使能套件的行业模型微调实践](https://mp.weixin.qq.com/s/7ocVjwX1k4xF6AaUkj-6vg)


## 25年Q1
### 1、IntrernLMv3发布后0 day支持xtuner npu

- 在-1 day令xtuner原生支持Ascend NPU: https://github.com/InternLM/xtuner/pull/983
- NPU中使用InternLMv3快速上手指导: https://github.com/InternLM/InternLM/pull/816
    - 贡献基于huggingface-transformers直接推理的脚本
    - 基于已适配的xtuner，在InternLMv3发布当天即完成在xtuner的LoRA微调验证
    - 贡献基于llama-factory的微调脚本，并在发布当天完成InternLMv3精度和性能的验证

### 2、torchtune原生支持

- NPU单卡功能相关: https://github.com/pytorch/torchtune/pull/2234
- NPU多卡分布式相关：https://github.com/pytorch/torchtune/pull/2646
- 分布式roadmap: https://github.com/pytorch/torchtune/issues/2288

### 3、OpenRLHF原生支持
- OpenRLHF原生支持NPU: https://github.com/OpenRLHF/OpenRLHF/pull/605
- Q2 RoadMap：https://github.com/OpenRLHF/OpenRLHF/issues/914
- 因OpenRLHF没有支持第三方device计划，后续转为此项目维护：[pt-ecosystem/OpenRLHF-NPU](https://github.com/pt-ecosystem/OpenRLHF-NPU)

### 4、尝试在transformers中原生支持npu亲和加速kernels
- 尝试在transformers中开启SDPA：[PR1](https://github.com/huggingface/transformers/pull/35165)、[PR2](https://github.com/huggingface/transformers/pull/36383)
- transformers原生支持npu的flash attention：[PR1](https://github.com/huggingface/transformers/pull/36696)、[PR2](https://github.com/huggingface/transformers/pull/37698)
、[PR3](https://github.com/huggingface/transformers/pull/38278)
- 除FA外其他加速kernels的加入：[ISSUE](https://github.com/huggingface/transformers/issues/39105)、[PR](https://github.com/huggingface/transformers/pull/39238)

### 5、在RL场景中vllm-ascend需要一些独特的修改
- vllm-ascend支持sleep mode功能：https://github.com/vllm-project/vllm-ascend/issues/320
- 修复RL场景拉起vllm的功能问题：https://github.com/vllm-project/vllm-ascend/pull/884
- 为vllm_ascend_C增加lazy init：https://github.com/vllm-project/vllm-ascend/pull/1234

## 25年Q2
### 1、在RL场景中vllm-ascend需要一些独特的修改（持续）
- 配套torch_npu升级：https://github.com/vllm-project/vllm-ascend/issues/1390
- DFX-澄清报错信息：https://github.com/vllm-project/vllm-ascend/issues/1706
- 修复Qwen2.5-VL场景功能缺失：https://github.com/vllm-project/vllm-ascend/pull/1705

### 2、veRL原生支持NPU
 - 原生支持PR：https://github.com/volcengine/verl/pull/332
 - verl Q3 Roadmap：https://github.com/volcengine/verl/discussions/2171



# 三、pt-ecosystem小组成员
24年10月-至今，参与pt-ecosystem适配工作的成员包含:
- [@zheliuyu](https://github.com/zheliuyu)
- [@FightingZhen](https://github.com/FightingZhen)
- [@zhuo97](https://github.com/zhuo97)
- [@Nicorgi](https://github.com/Nicorgi)
- [@as12138](https://github.com/as12138)
- [@tongtong0613](https://github.com/tongtong0613)
- [@Tonyztj](https://github.com/Tonyztj)
- [@Keilo001](https://github.com/Keilo001)
- [Leo-imperial](https://github.com/Leo-imperial)