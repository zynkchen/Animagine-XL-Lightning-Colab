# Animagine-XL-Lightning-Colab 极致加速的二次元 AI 绘画工作流。
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zynk/Animagine-XL-Lightning-Colab/blob/main/cartoon.ipynb)
Animagine XL + SDXL-Lightning Colab 工作流 🚀

这是一个专为 Google Colab 优化的 Stable Diffusion XL (SDXL) 快速图像生成项目。基于 Animagine XL 3.1 基底模型与 SDXL-Lightning 加速技术，实现 4-8 步内生成高质量二次元图像。
✨ 项目核心优势

    极速生成：集成 ByteDance SDXL-Lightning 技术，生成速度较原生 SDXL 提升 5-10 倍。

    智能存储策略：独创“大文件进 Drive，小文件留本地”方案。通过符号链接 (Symlink) 将 GB 级权重保存在 Google Drive，而将碎片化库文件保留在 Colab 高速空间，兼顾启动速度与存储空间。

    显存压力优化：深度集成 xformers、VAE Tiling 与 Attention Slicing，在 Colab T4 环境下亦可稳定输出 1216px 以上超清大图。

    实时预览画廊：基于 HTML/Base64 开发的动态网格系统，无需等待任务结束，即可实时查看生成进度。

    高质量 Prompt 预设：内置针对 Animagine XL 3.1 优化的质量标签体系，支持 NSFW 内容的高清渲染。

🛠️ 环境要求

    一个 Google 账号

    Google Drive 空间（建议剩余 15GB 以上）

    Colab 建议运行环境：Python 3.10+ / GPU T4

🚀 快速上手指南
1. 挂载与环境准备

运行 单元 1，根据提示授权挂载 Google Drive。

    脚本会自动检查 /content/drive/MyDrive/AI_Models_Cache 文件夹，并建立软链接，确保之后无需重复下载模型。

2. 模型引擎加载

运行 单元 2。系统将自动下载 Animagine XL 3.1 和 SDXL-Lightning 权重。

    注意：首次运行因写入云盘较慢，需等待 5-10 分钟；后续启动将实现“秒开”。

3. 开始创作

在 单元 3 的 UI 界面中输入你的 Prompt。

    推荐前缀：score_9, score_8_up, score_7_up, source_anime, masterpiece, ...

    推荐设置：Steps: 8 | CFG: 1.5 | Size: 832x1216

🎨 效果预览
少女/光影	场景/宏大


⚠️ 免责声明

    本工具仅供科研与学习交流使用，请勿用于非法用途。

    生成的图像版权归使用者所有，请遵守 Animagine XL 3.1 的开源许可协议。

    Google Colab 对 NSFW 内容有监测风险，请适度使用并遵守相关服务条款。

🤝 鸣谢

    模型基底：CagliostroLab

    加速补丁：ByteDance/SDXL-Lightning

    框架支持：Hugging Face Diffusers

如何贡献？

如果你有更好的显存优化方案或 ControlNet 集成经验，欢迎提交 Pull Request 或开 Issue 交流！
