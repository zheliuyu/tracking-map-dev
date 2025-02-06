## introduction
tracking-map用于跟踪Ascend NPU适配一些热门生态工具的进展

这里可以查看全量PR细节https://github.com/pt-ecosystem/tracking-map/issues/1

**非常感谢这些优秀的生态工具能接受我们的PR**


## 项目清单

#### torchtune原生支持NPU

- NPU单卡功能相关: https://github.com/pytorch/torchtune/pull/2234
- 分布式roadmap: https://github.com/pytorch/torchtune/issues/2288

#### IntrernLMv3发布后0 day支持NPU

- 首先令xtuner支持NPU: https://github.com/InternLM/xtuner/pull/983
- NPU中使用InternLMv3快速上手指导: https://github.com/InternLM/InternLM/pull/816
    - 组织PR并贡献了基于huggingface-transformers直接推理的脚本
    - 在-1 day让xtuner在Ascend NPU原生支持，并在InternLMv3发布当天即完成在xtuner的LoRA微调验证
    - 贡献了基于llama-factory的微调脚本，并在发布当天完成InternLMv3精度和性能的验证

#### RL工具探索

- OpenRLHF原生支持NPU: https://github.com/OpenRLHF/OpenRLHF/pull/605
- veRL原生支持NPU: https://github.com/volcengine/verl/compare/main...as12138:verl:main
