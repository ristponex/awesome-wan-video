<!-- markdownlint-disable MD033 MD041 -->

<div align="center">

# 🌊 Awesome Wan 视频生成

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Stars](https://img.shields.io/github/stars/your-org/awesome-wan-video?style=social)](https://github.com/your-org/awesome-wan-video)
[![VBench #1](https://img.shields.io/badge/VBench-No.1%20(86.22%25)-gold?style=flat-square&logo=data:image/svg+xml;base64,PHN2Zy8+)](https://vbench.org)
[![Downloads](https://img.shields.io/badge/下载量-2.2M+-blue?style=flat-square&logo=huggingface)](https://huggingface.co/Wan-AI)
[![Wan 2.6](https://img.shields.io/badge/最新版-Wan%202.6-ff6b35?style=flat-square)](https://github.com/Wan-Video/Wan2.6)

**阿里巴巴 Wan 视频生成模型完全资源汇总**

*领先的 AI 视频生成模型系列 — 开源模型 (2.1/2.2) 与前沿商业 API (2.5/2.6)。精选工具、提示词、教程和资源。*

[English](./README.md) | [简体中文](./README_zh-CN.md) | [日本語](./README_ja.md) | [한국어](./README_ko.md)

---

🚀 **通过 API 生成 Wan 视频 — $0.03/秒起** 🚀

[![在 Atlas Cloud 上试用](https://img.shields.io/badge/立即试用-Atlas%20Cloud-blue?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video)

*首次充值额外赠送 25%（最高 $100）• 支持无审查 Wan Spicy • Wan 2.7 即将上线！*

---

</div>

> 🔒 **企业级安全保障** — Atlas Cloud 已通过 **SOC I & II 认证** | **HIPAA 合规** | 美国公司，提供 99.9% 正常运行时间 SLA。

> 💳 **支付便捷** — 支持微信支付、支付宝直接付款，无需国际信用卡。

> 🎨 **NSFW 白名单更新** — 除 Seedance 和 Kling 外，**Vidu 系列**（Q3-Pro、Q3-Turbo）现已加入 Atlas Cloud 无审查内容生成白名单。

## 📑 目录

- [关于 Wan 模型](#-关于-wan-模型)
- [模型对比](#-模型对比)
- [快速开始](#-快速开始)
- [提示词集合](#-提示词集合)
- [本地部署指南](#-本地部署指南)
- [提示词工程](#-提示词工程)
- [API 价格对比](#-api-价格对比)
- [官方资源](#-官方资源)
- [社区与生态](#-社区与生态)
- [常见问题](#-常见问题)
- [Star 历史](#-star-历史)
- [贡献指南](#-贡献指南)
- [许可证](#-许可证)

---

## 🌊 关于 Wan 模型

**Wan** 是阿里巴巴推出的视频生成模型系列。其中 Wan 2.1 和 2.2 是**完全开源的**（Apache 2.0 许可），权重可在 Hugging Face 下载并自部署；而 Wan 2.5 和 2.6 是**闭源商业 API** 模型，提供更先进的功能。从首次亮相到登顶 **VBench 排行榜第一名**，Wan 持续突破视频 AI 的边界。

### 为什么选择 Wan？

- **🏆 VBench 冠军** — Wan 2.1 在 VBench 上取得 **86.22%** 的得分，超越 Sora (84.28%)、Luma (83.61%) 等所有模型
- **🔓 开源 (2.1/2.2)** — 与 Sora、可灵、Runway 不同，Wan 2.1/2.2 完全开源（Apache 2.0），权重可在 Hugging Face 下载，支持自部署
- **💻 消费级 GPU 友好** — 1.3B 版本仅需 **8.19GB 显存**，单卡 RTX 3060 即可运行
- **📊 海量训练数据** — 基于 **15 亿视频** + **100 亿图片** 训练
- **🔥 220 万+ 下载量** — 全球 AI 社区在 Hugging Face 和 ModelScope 上验证
- **🎬 无审查选项** — Wan 2.2 Spicy 实现无限制创意自由

### 模型发展路线

```
Wan 1.0 (2024 Q3)
  └── Wan 2.1 (2024 Q4) — VBench 第一名，14B 与 1.3B 双版本 [开源, Apache 2.0]
       └── Wan 2.2 (2025 Q1) — 质量提升，Spicy 变体 🌶️ [开源, Apache 2.0]
            ├── Wan 2.2 Spicy — NSFW/无审查生成 [闭源, Atlas Cloud LoRA 微调]
            └── Wan 2.5 (2025 Q2) — 音频同步，1080p，10秒 [闭源, 仅API]
                 └── Wan 2.6 (2025 Q3) — 多镜头，15秒，角色稳定性 [闭源, 仅API]
                      └── Wan 2.7 (即将推出！) — 🔜 首发于 Atlas Cloud
```

### 与闭源模型的关键差异

| 特性 | Wan 2.1/2.2 | Wan 2.5/2.6 | Sora | 可灵 | Runway Gen-3 |
|------|-------------|-------------|------|------|---------------|
| 开源 | ✅ Apache 2.0 | ❌ 仅 API | ❌ | ❌ | ❌ |
| 本地部署 | ✅ | ❌ | ❌ | ❌ | ❌ |
| 最高分辨率 | 720p | 1920×1080 | 1920×1080 | 1920×1080 | 1920×1080 |
| 最长时长 | 5秒 | 15秒 | 20秒 | 10秒 | 10秒 |
| 原生音频 | ❌ | ✅ | ✅ | ❌ | ❌ |
| 多镜头 | ❌ | ✅ | ❌ | ❌ | ❌ |
| NSFW 支持 | ✅ (Spicy) | ❌ | ❌ | ❌ | ❌ |
| 每视频价格 | 自部署 | 低至 $0.03 | $0.50+ | $0.30+ | $0.50+ |
| 消费级 GPU | ✅ (1.3B) | 不适用 | 不适用 | 不适用 | 不适用 |
| 微调支持 | ✅ LoRA | ❌ | ❌ | ❌ | ❌ |

---

## 📊 模型对比

| 版本 | 参数量 | 分辨率 | 时长 | 音频 | 多镜头 | 开源 | NSFW | API 价格 |
|------|--------|--------|------|------|--------|------|------|----------|
| **Wan 2.6** | 14B | 1080p | 最长 15秒 | ✅ | ✅ | ❌ (仅API) | ❌ | $0.07 |
| **Wan 2.5** | 14B | 1080p | 最长 10秒 | ✅ | ❌ | ❌ (仅API) | ❌ | 更低 |
| **Wan 2.2 Spicy** 🌶️ | 14B | 720p | 最长 8秒 | ❌ | ❌ | ✅ | ✅ | **$0.03** |
| **Wan 2.2** | 14B / 1.3B | 720p | 最长 5秒 | ❌ | ❌ | ✅ | ❌ | — |
| **Wan 2.1** | 14B / 1.3B | 720p | 最长 5秒 | ❌ | ❌ | ✅ | ❌ | — |

### Atlas Cloud 可用模型

| 模型 | 类型 | 价格 | 亮点 |
|------|------|------|------|
| Wan 2.6 T2V | 文生视频 | $0.07/秒起（7折） | 5/10/15秒，最高 1920×1080，多镜头，音频 |
| Wan 2.6 I2V | 图生视频 | 可用 | 高保真图片动画 |
| Wan 2.6 I2V Flash | 图生视频 | 更快更便宜 | 速度优化版 |
| Wan 2.6 V2V | 视频转视频 | 可用 | 风格迁移与编辑 |
| Wan 2.6 图片编辑 | 图片编辑 | 可用 | AI 图片编辑 |
| Wan 2.6 T2I | 文生图 | 可用 | 高质量图片生成 |
| Wan 2.5 T2V | 文生视频 | 可用 | 稳定视频生成 |
| Wan 2.5 I2V | 图生视频 | 可用 | 稳定图片动画 |
| Wan 2.5 Fast | 文生视频 | 可用 | 速度优化版 |
| Wan 2.2 Spicy I2V 🌶️ | 图生视频 | **$0.03/秒起** | 无审查生成 |
| Wan 2.2 Spicy I2V LoRA | 图生视频 | 可用 | 支持 LoRA 微调 |
| Wan 2.2 换脸 | 视频特效 | 可用 | animate-mix 人脸替换 |
| Wan 2.2 图片转动画 | 动画 | 可用 | animate-move 动作迁移 |
| Van 2.6 / 2.5 | 优化版 | 可用 | Atlas Cloud 优化版 |

> *以上价格为每秒生成视频的起步价，实际费用取决于分辨率、时长和所选模型。*

> 🎁 **新用户优惠：** 首次充值额外赠送 25%（最高 $100 奖金）。[立即注册 →](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video)

---

## 🚀 快速开始

### 方式一：API（Atlas Cloud）— 最快捷

<details>
<summary><b>cURL 示例 — Wan 2.6 文生视频</b></summary>

```bash
# Wan 2.6 文本生成视频 API 调用
curl -X POST "https://api.atlascloud.ai/v1/video/generate" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "wan-2.6-t2v",
    "prompt": "一条雄伟的巨龙在日落时分穿越云层翱翔，电影级光影，4K画质",
    "duration": 10,
    "resolution": "1920x1080",
    "audio": true
  }'
```

</details>

<details>
<summary><b>cURL 示例 — Wan 2.2 Spicy（无审查）</b></summary>

```bash
# Wan 2.2 Spicy 无审查图片转视频 API 调用 — 仅需 $0.03/秒起
curl -X POST "https://api.atlascloud.ai/v1/video/generate" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "alibaba/wan-2.2-spicy/image-to-video",
    "image_url": "https://example.com/your-image.jpg",
    "prompt": "流畅自然的动作，艺术表达，高质量"
  }'
```

</details>

<details>
<summary><b>Python 示例 — 完整流程</b></summary>

```python
"""
Wan 视频生成完整示例
支持 Wan 2.6 T2V、I2V 以及 Wan 2.2 Spicy
"""
import requests
import time

# Atlas Cloud API 配置
API_KEY = "YOUR_API_KEY"
BASE_URL = "https://api.atlascloud.ai/v1"

def generate_video(prompt: str, model: str = "wan-2.6-t2v", **kwargs) -> str:
    """
    调用 Wan 模型生成视频

    参数:
        prompt: 视频描述文本
        model: 模型名称，默认使用 Wan 2.6
        **kwargs: 其他参数如 duration, resolution 等
    返回:
        视频下载链接
    """
    headers = {
        "Authorization": f"Bearer {API_KEY}",
        "Content-Type": "application/json"
    }

    payload = {
        "model": model,
        "prompt": prompt,
        **kwargs
    }

    # 提交生成任务
    response = requests.post(f"{BASE_URL}/video/generate", json=payload, headers=headers)
    task_id = response.json()["task_id"]

    # 轮询等待结果
    while True:
        status = requests.get(f"{BASE_URL}/video/status/{task_id}", headers=headers)
        result = status.json()

        if result["status"] == "completed":
            return result["video_url"]
        elif result["status"] == "failed":
            raise Exception(f"生成失败: {result.get('error', '未知错误')}")

        time.sleep(2)  # 每2秒检查一次状态

# ====== 使用示例 ======

# 示例 1: Wan 2.6 文本生成视频（支持多镜头 + 音频）
video_url = generate_video(
    prompt="A chef preparing sushi in a traditional Japanese kitchen, warm lighting, close-up shots",
    model="wan-2.6-t2v",
    duration=10,
    resolution="1920x1080",
    audio=True
)
print(f"视频已生成: {video_url}")

# 示例 2: Wan 2.2 Spicy 无审查生成（仅需 $0.03）
spicy_url = generate_video(
    prompt="Artistic figure study, classical painting style, natural movement",
    model="alibaba/wan-2.2-spicy/image-to-video"
)
print(f"Spicy 视频已生成: {spicy_url}")
```

</details>

### 方式二：本地部署（ComfyUI）

```bash
# 1. 安装 ComfyUI
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 2. 安装依赖
pip install -r requirements.txt

# 3. 下载 Wan 2.6 模型权重
# 从 Hugging Face 下载（需要约 28GB 磁盘空间）
huggingface-cli download Wan-AI/Wan2.6-T2V-14B --local-dir models/wan2.6/

# 4. 安装 Wan ComfyUI 节点
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
pip install -r ComfyUI-Wan/requirements.txt

# 5. 启动 ComfyUI
cd ..
python main.py --listen 0.0.0.0 --port 8188
```

### 方式三：Hugging Face Pipeline

```python
"""
使用 Hugging Face Diffusers 库本地运行 Wan 2.1
适合有 NVIDIA GPU 的用户
"""
from diffusers import WanPipeline
import torch

# 加载模型（1.3B 版本仅需 8.19GB 显存）
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16  # 使用 FP16 节省显存
)
pipe = pipe.to("cuda")

# 生成视频
video = pipe(
    prompt="一只金毛猎犬在秋叶中奔跑，慢动作，温暖的阳光",
    num_frames=81,        # 约5秒视频
    height=480,
    width=720,
    guidance_scale=7.5
).frames[0]

# 保存视频
from diffusers.utils import export_to_video
export_to_video(video, "output.mp4", fps=16)
print("视频已保存至 output.mp4")
```

### 方式四：Docker 部署

```dockerfile
# Wan 2.6 Docker 部署配置
FROM nvidia/cuda:12.1-runtime-ubuntu22.04

# 安装系统依赖
RUN apt-get update && apt-get install -y \
    python3 python3-pip git wget \
    && rm -rf /var/lib/apt/lists/*

# 安装 Python 依赖
RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu121
RUN pip3 install diffusers transformers accelerate safetensors

# 下载 Wan 模型
RUN huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B --local-dir /models/wan

# 复制推理脚本
COPY inference.py /app/inference.py

WORKDIR /app
CMD ["python3", "inference.py"]
```

```bash
# 构建并运行 Docker 容器
docker build -t wan-video .
docker run --gpus all -p 8080:8080 wan-video
```

---

## 🎨 提示词集合

> 30+ 精心打造的提示词，针对 Wan 模型优化。每个提示词包含完整文本、推荐模型、参数设置和使用技巧。

### 🎬 电影与影视

<details>
<summary><b>1. 史诗山脉风景</b></summary>

- **提示词：** `Sweeping aerial shot over snow-capped mountains at golden hour, dramatic clouds casting long shadows across alpine valleys, a winding river reflecting the amber sky, cinematic camera movement slowly pushing forward, volumetric lighting, 8K film grain`
- **模型：** Wan 2.6 T2V
- **时长：** 15秒
- **分辨率：** 1920×1080
- **技巧：** 开启多镜头模式获得更动态的序列。开启音频可获得环境风声。

</details>

<details>
<summary><b>2. 城市夜间追逐</b></summary>

- **提示词：** `Tracking shot through neon-lit Tokyo streets at night, rain-soaked asphalt reflecting pink and blue neon signs, a figure in a dark coat running through crowds, handheld camera shake, Blade Runner aesthetic, moody atmosphere, cinematic color grading`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 使用负面提示词 "blurry, low quality, static" 获得更清晰的运动效果。

</details>

<details>
<summary><b>3. 历史战争场景</b></summary>

- **提示词：** `Wide establishing shot of a medieval battlefield at dawn, thousands of soldiers in formation, banners waving in the wind, mist rolling across the field, dramatic orchestral music feel, Lord of the Rings inspired cinematography, epic scale, film grain`
- **模型：** Wan 2.6 T2V
- **时长：** 15秒
- **分辨率：** 1920×1080
- **技巧：** 多镜头模式在此场景中效果极佳，可在全景和特写之间切换。

</details>

<details>
<summary><b>4. 水下纪录片</b></summary>

- **提示词：** `Slow underwater tracking shot through a vibrant coral reef, tropical fish swimming in formation, sunbeams penetrating the crystal-clear blue water, a sea turtle gliding gracefully through the frame, National Geographic style, 4K clarity`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 添加 "smooth camera movement, steady" 避免水下抖动瑕疵。

</details>

<details>
<summary><b>5. 黑色电影侦探</b></summary>

- **提示词：** `Close-up of a detective in a dimly lit office, cigarette smoke curling through a single shaft of light from venetian blinds, black and white film noir style, slow camera dolly in, dramatic shadows, 1940s aesthetic, grain texture`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1280×720
- **技巧：** 明确指定 "black and white, monochrome" 以获得一致的黑色电影风格。

</details>

### 🌶️ NSFW / 创意自由（Wan 2.2 Spicy）

<details>
<summary><b>6. 古典人体研究</b></summary>

- **提示词：** `Renaissance-style figure study, soft diffused lighting on skin, classical painting composition, marble sculpture coming to life with subtle breathing movement, warm golden tones, museum gallery setting, artistic and elegant`
- **模型：** Wan 2.2 Spicy I2V
- **价格：** $0.03/秒起
- **技巧：** 搭配古典画作或雕塑参考图片效果最佳。

</details>

<details>
<summary><b>7. 前卫时尚大片</b></summary>

- **提示词：** `High fashion editorial, model in sheer flowing fabric, dramatic wind effect, stark white studio lighting, Helmut Newton inspired, bold poses transitioning fluidly, haute couture, magazine quality`
- **模型：** Wan 2.2 Spicy I2V
- **价格：** $0.03/秒起
- **技巧：** 使用 LoRA 变体可在多次生成中保持一致风格。

</details>

<details>
<summary><b>8. 艺术身体动态</b></summary>

- **提示词：** `Contemporary dance performance, fluid body movement, dramatic stage lighting, dancer's silhouette against colored backdrop, artistic expression through motion, modern ballet, intimate camera angles, professional choreography`
- **模型：** Wan 2.2 Spicy I2V
- **价格：** $0.03/秒起
- **技巧：** 图生视频模式效果最佳 — 提供一张舞者参考图片。

</details>

<details>
<summary><b>9. 神话场景</b></summary>

- **提示词：** `Birth of Venus reimagined, goddess emerging from ocean waves, flowing golden hair, seashells and foam, Pre-Raphaelite painting style, ethereal glow, mythological beauty, Botticelli inspired but cinematic`
- **模型：** Wan 2.2 Spicy I2V
- **价格：** $0.03/秒起
- **技巧：** 搭配古典艺术参考图片效果极佳。

</details>

<details>
<summary><b>10. 赛博朋克角色</b></summary>

- **提示词：** `Cyberpunk character in revealing neon-lit outfit, holographic tattoos glowing on skin, futuristic nightclub setting, pulsing LED lights, confident walking motion, sci-fi fashion, Blade Runner 2049 aesthetic`
- **模型：** Wan 2.2 Spicy I2V LoRA
- **价格：** $0.03/秒起
- **技巧：** 使用 LoRA 可在不同场景中保持角色外观一致。

</details>

### 📦 产品与商业

<details>
<summary><b>11. 奢侈手表展示</b></summary>

- **提示词：** `Macro close-up of a luxury watch rotating on a black velvet surface, golden light reflections dancing on polished metal, mechanical movement visible through transparent caseback, premium product photography, smooth 360-degree rotation`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 缓慢可控的旋转效果最佳。添加 "studio lighting, product photography" 获得商业级品质。

</details>

<details>
<summary><b>12. 美食广告 — 咖啡倾倒</b></summary>

- **提示词：** `Slow motion pour of steaming espresso into a white ceramic cup, rich crema forming on surface, steam rising in soft morning light, rustic wooden table, out-of-focus bakery background, food photography, warm color palette, 120fps slow motion feel`
- **模型：** Wan 2.6 T2V
- **时长：** 5秒
- **分辨率：** 1920×1080
- **技巧：** 短时长配合高细节对美食内容效果更好。

</details>

<details>
<summary><b>13. 运动鞋产品发布</b></summary>

- **提示词：** `Dynamic sneaker reveal, shoe floating and rotating in mid-air against gradient background, particles and light streaks surrounding the product, dramatic lighting transitions, Nike commercial style, clean product visualization`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 使用多镜头拍摄同一产品的不同角度。

</details>

<details>
<summary><b>14. 香水广告 — 空灵风</b></summary>

- **提示词：** `Glass perfume bottle on a reflective surface, golden liquid catching light, slow motion flower petals falling around it, soft bokeh background, luxury brand commercial aesthetic, Chanel No.5 inspired visual, elegant and sophisticated`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 添加 "glass reflections, caustics, luxury" 获得高端质感。

</details>

<details>
<summary><b>15. 科技产品开箱</b></summary>

- **提示词：** `Cinematic unboxing of a sleek smartphone, hands slowly lifting the lid of a minimalist white box, device rising with a subtle glow, holographic interface appearing above the screen, Apple keynote style presentation, clean and modern`
- **模型：** Wan 2.6 I2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 使用 I2V 模式配合实际产品图片以确保品牌准确性。

</details>

### 🎨 动画与卡通

<details>
<summary><b>16. 动漫樱花场景</b></summary>

- **提示词：** `Anime style, a young girl standing under a blooming cherry blossom tree, pink petals falling in slow motion, gentle breeze moving her hair and school uniform, soft watercolor background, Studio Ghibli aesthetic, warm spring lighting`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1280×720
- **技巧：** 添加 "anime, cel-shaded, 2D animation" 获得一致的动漫风格。

</details>

<details>
<summary><b>17. 像素风冒险</b></summary>

- **提示词：** `Retro pixel art game scene, 16-bit hero character walking through a mystical forest, glowing mushrooms, floating fireflies, parallax scrolling background layers, SNES-era RPG aesthetic, vibrant pixel colors`
- **模型：** Wan 2.5 T2V
- **时长：** 5秒
- **分辨率：** 1280×720
- **技巧：** 较低分辨率可增强复古像素艺术感。

</details>

<details>
<summary><b>18. 3D 卡通角色</b></summary>

- **提示词：** `Pixar-style 3D animated character, a small robot with big expressive eyes discovering a flower in a post-apocalyptic landscape, WALL-E inspired, smooth character animation, subsurface scattering on plastic materials, Pixar render quality`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** Wan 2.6 处理 3D 动画风格的效果非常出色。

</details>

<details>
<summary><b>19. 漫画风动作</b></summary>

- **提示词：** `Marvel comic book style action sequence, superhero landing pose with impact shockwave, bold ink outlines, halftone dot shading, dynamic camera angle from below, speech bubble appearing, vibrant primary colors, Jack Kirby inspired`
- **模型：** Wan 2.6 T2V
- **时长：** 5秒
- **分辨率：** 1280×720
- **技巧：** 短促的动作爆发最适合漫画书风格。

</details>

<details>
<summary><b>20. 水彩故事书</b></summary>

- **提示词：** `Watercolor illustration coming to life, a fox and rabbit having a tea party in an enchanted forest clearing, soft paint bleeding effects, storybook page turning animation, children's book illustration style, gentle pastel colors, whimsical`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1280×720
- **技巧：** 使用 "watercolor, illustration, painted" 关键词有助于保持艺术风格。

</details>

### 🔄 角色替换（Wan 2.2 animate-mix）

<details>
<summary><b>21. 名人模仿</b></summary>

- **提示词：** `Professional business presentation, confident speaker at a podium, formal attire, corporate event, smooth gestures and natural speech patterns`
- **模型：** Wan 2.2 角色替换（animate-mix）
- **技巧：** 上传演讲的源视频和目标人脸图片。正面、光线良好的面部效果最佳。

</details>

<details>
<summary><b>22. 历史人物复活</b></summary>

- **提示词：** `Historical documentary narration, period-appropriate setting, speaking directly to camera, educational content`
- **模型：** Wan 2.2 角色替换（animate-mix）
- **技巧：** 清晰高分辨率的参考照片效果最佳。保持源视频和目标之间光线一致。

</details>

<details>
<summary><b>23. 音乐视频换脸</b></summary>

- **提示词：** `Music performance, singer on stage, dynamic lighting, emotional expression, concert atmosphere`
- **模型：** Wan 2.2 角色替换（animate-mix）
- **技巧：** 适用于面部追踪稳定的音乐视频。避免极端的头部旋转。

</details>

### 🏃 动作迁移（Wan 2.2 animate-move）

<details>
<summary><b>24. 舞蹈编排迁移</b></summary>

- **提示词：** `Professional dance routine, hip-hop choreography, studio setting, full body visible, clean background`
- **模型：** Wan 2.2 图片转动画（animate-move）
- **技巧：** 上传舞蹈视频作为动作源和角色图片。干净背景的全身照效果最佳。

</details>

<details>
<summary><b>25. 卡通角色动画化</b></summary>

- **提示词：** `Animated character performing complex movements, cartoon style, expressive body language`
- **模型：** Wan 2.2 图片转动画（animate-move）
- **技巧：** 使用真人的动作视频来驱动任何 2D 或 3D 角色图片。

</details>

<details>
<summary><b>26. 品牌吉祥物动画</b></summary>

- **提示词：** `Brand mascot performing fun actions, waving, jumping, dancing, engaging personality`
- **模型：** Wan 2.2 图片转动画（animate-move）
- **技巧：** 非常适合为静态品牌吉祥物注入自然动态。

</details>

### 🌐 其他与进阶

<details>
<summary><b>27. 城市延时摄影</b></summary>

- **提示词：** `Hyper-lapse of a modern city skyline from day to night, clouds racing across the sky, lights gradually turning on in skyscrapers, traffic becoming streams of light, star trails appearing, 24-hour cycle compressed into seconds, urban time-lapse`
- **模型：** Wan 2.6 T2V
- **时长：** 15秒
- **分辨率：** 1920×1080
- **技巧：** 15秒时长非常适合日夜过渡。

</details>

<details>
<summary><b>28. 自然微距 — 蝴蝶羽化</b></summary>

- **提示词：** `Extreme macro shot of a monarch butterfly emerging from chrysalis, iridescent wing scales unfolding in slow motion, morning dew drops on wings, shallow depth of field, nature documentary quality, BBC Earth style`
- **模型：** Wan 2.6 T2V
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** 缓慢精细动作的微距主体能产生惊艳效果。

</details>

<details>
<summary><b>29. 科幻空间站</b></summary>

- **提示词：** `Exterior shot of a massive space station orbiting Earth, ISS-inspired design but futuristic, solar panels rotating to track the sun, a shuttle approaching for docking, Earth's blue glow illuminating the structure, Interstellar cinematography`
- **模型：** Wan 2.6 T2V
- **时长：** 15秒
- **分辨率：** 1920×1080
- **技巧：** 开启音频获得沉浸式太空氛围。多镜头模式可切换内外景。

</details>

<details>
<summary><b>30. 抽象流体艺术</b></summary>

- **提示词：** `Abstract fluid art in motion, vibrant acrylic paint pouring and mixing, golden veins forming between color pools, Kandinsky meets Jackson Pollock, mesmerizing organic patterns, satisfying ASMR-like visual, overhead camera view`
- **模型：** Wan 2.5 T2V
- **时长：** 10秒
- **分辨率：** 1280×720
- **技巧：** 抽象内容容错性高，始终能产生美丽的效果。

</details>

<details>
<summary><b>31. Wan 2.6 R2V — 角色参考</b></summary>

- **提示词：** `上传角色参考视频（捕捉外观+声音），然后在新场景中生成：在未来城市中行走，与全息显示屏互动，保持完全一致的外观和声音特征`
- **模型：** Wan 2.6 R2V（参考视频生成）
- **时长：** 10秒
- **分辨率：** 1920×1080
- **技巧：** Wan 2.6 R2V 从参考视频中保持角色身份（外观+声音）。提供 3-5 秒参考片段效果最佳。

</details>

<details>
<summary><b>32. 多镜头叙事</b></summary>

- **提示词：** `Shot 1: Wide establishing shot of a cozy café on a rainy Parisian street. Shot 2: Close-up of hands wrapping around a steaming coffee cup. Shot 3: Looking out the window as rain streams down the glass. Shot 4: Slow zoom out revealing the full café scene with warm interior lighting.`
- **模型：** Wan 2.6 T2V（多镜头）
- **时长：** 15秒
- **分辨率：** 1920×1080
- **技巧：** 使用 "Shot N:" 前缀分隔场景实现多镜头功能。Wan 2.6 会在镜头之间创建流畅的过渡。

</details>

---

## 🖥️ 本地部署指南

### 硬件要求

| 组件 | Wan 2.6 (14B) | Wan 2.1 (14B) | Wan 2.1 (1.3B) |
|------|---------------|---------------|-----------------|
| **GPU 显存** | 24GB+ | 24GB+ | **8.19GB** |
| **推荐 GPU** | RTX 4090 / A100 | RTX 4090 / A100 | RTX 3060 12GB |
| **系统内存** | 32GB+ | 32GB+ | 16GB |
| **磁盘空间** | ~56GB | ~28GB | ~5GB |
| **操作系统** | Linux / Windows | Linux / Windows | Linux / Windows |
| **CUDA** | 12.1+ | 11.8+ | 11.8+ |

### ComfyUI 安装（详细步骤）

```bash
# ======== 第一步：安装 ComfyUI ========
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 创建虚拟环境（推荐）
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# 安装 PyTorch（CUDA 12.1）
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# 安装 ComfyUI 依赖
pip install -r requirements.txt

# ======== 第二步：安装 Wan 节点 ========
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
cd ComfyUI-Wan
pip install -r requirements.txt
cd ../..

# ======== 第三步：下载模型 ========
# 选项 A：完整 14B 模型（推荐，但需要 24GB+ 显存）
huggingface-cli download Wan-AI/Wan2.6-T2V-14B \
    --local-dir models/wan2.6-14b/

# 选项 B：轻量 1.3B 模型（仅需 8.19GB 显存）
huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B \
    --local-dir models/wan2.1-1.3b/

# ======== 第四步：启动 ComfyUI ========
python main.py --listen 0.0.0.0 --port 8188

# 浏览器打开 http://localhost:8188
# 导入 Wan 工作流节点即可使用
```

### 显存优化技巧

```python
"""
显存优化技巧，帮助在消费级 GPU 上运行 Wan 模型
"""
import torch
from diffusers import WanPipeline

# 技巧 1: 使用半精度浮点（节省约 50% 显存）
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-14B",
    torch_dtype=torch.float16
)

# 技巧 2: 启用注意力切片（大幅降低显存峰值）
pipe.enable_attention_slicing(slice_size="auto")

# 技巧 3: 启用 VAE 切片（逐步解码视频帧）
pipe.enable_vae_slicing()

# 技巧 4: 启用 CPU 卸载（自动将不活跃模块移至 CPU）
pipe.enable_model_cpu_offload()

# 技巧 5: 使用 xformers 加速（需额外安装 xformers）
# pip install xformers
pipe.enable_xformers_memory_efficient_attention()

# 技巧 6: 降低分辨率和帧数
video = pipe(
    prompt="Your prompt here",
    num_frames=49,       # 减少帧数（49帧 ≈ 3秒）
    height=480,          # 降低分辨率
    width=720,
    guidance_scale=7.5
).frames[0]

# 技巧 7: 使用 1.3B 模型代替 14B
# 1.3B 模型仅需 8.19GB 显存，质量仍然出色
pipe_light = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16
).to("cuda")
```

---

## ✍️ 提示词工程

### Wan 专用高效关键词

| 类别 | 有效关键词 |
|------|-----------|
| **画质** | `8K, cinematic, film grain, high detail, professional, masterpiece` |
| **镜头** | `tracking shot, dolly zoom, aerial shot, close-up, macro, wide angle` |
| **光线** | `golden hour, volumetric lighting, rim lighting, neon glow, soft diffused` |
| **运动** | `slow motion, time-lapse, smooth pan, gentle movement, dynamic action` |
| **风格** | `photorealistic, anime, watercolor, oil painting, cyberpunk, noir` |
| **氛围** | `dramatic, ethereal, cozy, epic, melancholic, whimsical` |

### 负面提示词策略

```
# 推荐通用负面提示词
blurry, low quality, distorted, deformed, ugly, bad anatomy,
watermark, text overlay, logo, pixelated, noise, artifacts,
oversaturated, underexposed, static image, no movement,
extra fingers, missing limbs, unnatural proportions
```

### 多镜头技巧（Wan 2.6）

```
# 多镜头叙事模板
Shot 1: [全景/确立镜头] - 用环境和背景设定场景
Shot 2: [中景] - 引入主体或角色
Shot 3: [特写] - 情感细节或关键动作
Shot 4: [全景/拉远] - 结局或揭示

# 示例：咖啡广告多镜头
Shot 1: 日出时分哥伦比亚咖啡庄园的航拍，晨雾缭绕。
Shot 2: 农民粗糙的双手采摘成熟的咖啡果实。
Shot 3: 咖啡豆烘焙的极致特写，油光闪闪。
Shot 4: 现代咖啡馆中，一杯新鲜咖啡升起的蒸汽。
```

### 音频生成控制（Wan 2.6）

Wan 2.6 支持原生音频同步。最佳效果技巧：

- **环境音** 根据视觉内容自动生成
- 在提示词中添加音频线索：`"birds chirping"（鸟鸣）`、`"rain on window"（雨打窗户）`、`"crowd cheering"（人群欢呼）`
- 较长时长（10-15秒）音频质量更好
- API 调用中使用 `audio: true` 开启音频生成

### 分辨率与速度权衡

| 分辨率 | 显存占用 | 生成时间 | 最适合 |
|--------|---------|---------|--------|
| 1920×1080 | ~24GB | ~3-5 分钟 | 最终成片 |
| 1280×720 | ~16GB | ~1-3 分钟 | 草稿与测试 |
| 854×480 | ~10GB | ~30-60秒 | 快速原型 |
| 640×360 | ~8GB | ~15-30秒 | 快速预览 |

---

## 💰 API 价格对比

| 提供商 | Wan 2.6 T2V | Wan 2.5 T2V | Wan Spicy 🌶️ | 主要特点 |
|--------|-------------|-------------|---------------|---------|
| **Atlas Cloud** ⭐ | **$0.07/秒起**（7折） | 更低 | **$0.03/秒起** | ✅ 全模型、NSFW、LoRA、V2V、多镜头 |
| 阿里云 | $0.10+ | $0.08+ | 不可用 | ⚠️ 区域限制，无 NSFW |
| Replicate | $0.15+ | $0.12+ | 有限 | 基础 API |
| 自建服务器 | GPU 时费 | GPU 时费 | GPU 时费 | ✅ 完全控制，❌ 维护负担 |

> *以上价格为每秒生成视频的起步价，实际费用取决于分辨率、时长和所选模型。*

### 成本分析示例

| 使用场景 | 模型 | 月生成量 | Atlas Cloud 费用 | 自建（A100） |
|---------|------|---------|-----------------|-------------|
| 社交媒体创作者 | Wan 2.6 T2V | 500 个 | **$35/月** | ~$500/月 |
| NSFW 艺术创作 | Wan Spicy | 1,000 个 | **$30/月** | ~$500/月 |
| 商业制作 | Wan 2.6 T2V | 100 个 | **$7/月** | ~$500/月 |
| 业余爱好者 | Wan 2.5 T2V | 50 个 | **<$5/月** | ~$500/月 |

> 💡 **专业提示：** [注册 Atlas Cloud](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video) 首次充值 **额外赠送 25%**（最高 $100 奖金）。$100+$25 奖金可生成多达 1,785 个 Wan Spicy 视频或 1,785+ 个 Wan 2.6 视频！

### Atlas Cloud vs fal.ai 价格对比

| 模型 | fal.ai 价格 | Atlas Cloud 价格 | 节省幅度 |
|:------|:------------|:-----------------|:---------|
| **Kling** | $0.224/秒 (5秒 = $1.12) | $0.204/秒起 | **便宜 82%** |
| **Seedance** | ~$0.26/视频 | $0.044/秒起 | **便宜 15%** |
| **Wan 2.5** | $0.05/秒 (5秒 = $0.25) | $0.05/秒起 | **便宜 80%** |
| **Wan 2.6** | 相似定价 | $0.07/秒起 | 极具竞争力 |
| **Veo 3** | $0.40/秒 (8秒 = $3.20) | 即将推出 | 敬请期待 |
| **Vidu Q3-Pro** | — | $0.06/秒起 | Atlas 独家 |
| **Vidu Q3-Turbo** | — | $0.034/秒起 | Atlas 独家 |

> *以上价格为每秒生成视频的起步价，实际费用取决于分辨率、时长和所选模型。*

> 💡 Atlas Cloud 提供所有主流视频模型的**最低价格**。从 fal.ai 切换到 Atlas Cloud，视频生成成本最高可节省 **82%**。

---

## 📚 官方资源

### 模型权重与下载

| 资源 | 链接 | 说明 |
|------|------|------|
| Hugging Face — Wan-AI | [huggingface.co/Wan-AI](https://huggingface.co/Wan-AI) | 所有模型权重 |
| ModelScope — Wan | [modelscope.cn/Wan-Video](https://modelscope.cn/organization/Wan-Video) | 备选下载（亚洲更快） |
| Wan 2.6 T2V 14B | [HF 链接](https://huggingface.co/Wan-AI/Wan2.6-T2V-14B) | 最新文生视频 |
| Wan 2.6 I2V 14B | [HF 链接](https://huggingface.co/Wan-AI/Wan2.6-I2V-14B) | 最新图生视频 |
| Wan 2.1 T2V 1.3B | [HF 链接](https://huggingface.co/Wan-AI/Wan2.1-T2V-1.3B) | 轻量版，消费级 GPU |

### 论文与研究

| 论文 | 链接 | 描述 |
|------|------|------|
| Wan 2.1 技术报告 | [arXiv](https://arxiv.org/abs/2503.20314) | 架构与训练细节 |
| VBench 排行榜 | [vbench.org](https://vbench.org) | 基准测试排名 |

### 官方 GitHub 仓库

| 仓库 | 描述 |
|------|------|
| [Wan-Video/Wan2.6](https://github.com/Wan-Video/Wan2.6) | Wan 2.6 官方代码 |
| [Wan-Video/Wan2.1](https://github.com/Wan-Video/Wan2.1) | Wan 2.1 官方代码 |

---

## 🌐 社区与生态

### ComfyUI 扩展

| 扩展 | 描述 | 星标 |
|------|------|------|
| [ComfyUI-Wan](https://github.com/Wan-Video/ComfyUI-Wan) | 官方 Wan ComfyUI 节点 | ⭐ |
| [ComfyUI-WanVideoWrapper](https://github.com/kijai/ComfyUI-WanVideoWrapper) | 社区封装，附加功能 | ⭐ |

### LoRA 模型与微调

| 资源 | 描述 |
|------|------|
| [Civitai — Wan LoRAs](https://civitai.com/models?tags=wan) | 社区训练的 LoRA 模型 |
| [Wan LoRA 训练指南](https://github.com/Wan-Video/Wan2.1/blob/main/docs/lora.md) | 官方微调文档 |

### 社区中心

| 平台 | 链接 |
|------|------|
| Reddit — r/WanVideo | [reddit.com/r/WanVideo](https://reddit.com/r/WanVideo) |
| Discord — Wan 社区 | 社区 Discord 服务器 |
| Twitter/X — #WanVideo | [搜索 #WanVideo](https://twitter.com/search?q=%23WanVideo) |

### 教程与指南

| 标题 | 类型 | 链接 |
|------|------|------|
| Wan 2.6 完全指南 | 视频 | YouTube |
| ComfyUI + Wan 工作流 | 文章 | 博客 |
| Wan LoRA 训练教程 | 视频 | YouTube |
| Wan vs 可灵 vs Sora 对比 | 文章 | 博客 |

---

## ❓ 常见问题

<details>
<summary><b>什么是 Wan AI 视频模型？</b></summary>

Wan 是阿里巴巴推出的视频生成模型系列。其中 Wan 2.1/2.2 是**开源的**（Apache 2.0），权重可在 Hugging Face 下载并自部署；Wan 2.5/2.6 是**闭源商业 API** 模型。它使用扩散 Transformer 架构，基于 15 亿视频和 100 亿图片训练。Wan 2.1 模型在 **VBench 排行榜上排名第一**，得分 86.22%，超越 Sora (84.28%) 和 Luma (83.61%)。最新版本是 **Wan 2.6**，支持最长 15 秒的多镜头 1080p 视频生成，并带有原生音频同步，通过 API 提供服务。

</details>

<details>
<summary><b>如何在本地运行 Wan？</b></summary>

你可以通过以下方式在本地运行 Wan：
1. **ComfyUI** — 安装 Wan ComfyUI 节点并下载模型权重
2. **Hugging Face Diffusers** — 在 Python 中使用 `WanPipeline` 类
3. **Docker** — 使用我们提供的 Dockerfile 部署

**1.3B 模型仅需 8.19GB 显存**，消费级 GPU 如 RTX 3060 即可运行。14B 模型需要 24GB+ 显存（RTX 4090 或 A100）。

请参阅[本地部署指南](#-本地部署指南)获取详细步骤。

</details>

<details>
<summary><b>Wan vs Seedance vs 可灵 — 哪个更好？</b></summary>

| 特性 | Wan 2.6 | Seedance | 可灵 |
|------|---------|----------|------|
| 开源 | ❌ (2.1/2.2 开源) | ❌ | ❌ |
| 最长时长 | 15秒 | 10秒 | 10秒 |
| 音频 | ✅ | ❌ | ❌ |
| 多镜头 | ✅ | ❌ | ❌ |
| NSFW | ✅ (Spicy) | ❌ | ❌ |
| 本地部署 | ❌ (2.1/2.2 可以) | ❌ | ❌ |
| API 价格 | 低至 $0.03 | $0.20+ | $0.30+ |

**Wan 优势：** 定价优势、NSFW 支持和功能丰富度。Wan 2.1/2.2 提供开源灵活性和本地部署能力，Wan 2.5/2.6 通过 API 提供前沿质量。Seedance 和可灵在某些特定场景可能有不同的运动质量，但 Wan 的快速迭代使其成为最佳长期选择。

</details>

<details>
<summary><b>运行 Wan 2.6 最佳 GPU 是什么？</b></summary>

| GPU | 显存 | 可运行 | 性能 |
|-----|------|--------|------|
| RTX 3060 12GB | 12GB | ✅（仅 1.3B） | 基础 |
| RTX 3090 | 24GB | ✅（14B 需优化） | 良好 |
| RTX 4090 | 24GB | ✅（14B 全速） | 优秀 |
| A100 40GB | 40GB | ✅（所有模型，批量） | 专业 |
| A100 80GB | 80GB | ✅（所有模型，高批量） | 企业 |

**预算建议：** 本地部署推荐 RTX 4090，或使用 [Atlas Cloud API](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video) $0.03/秒起，无需硬件投资。

</details>

<details>
<summary><b>有无审查的 Wan 模型吗？</b></summary>

**有！** **Wan 2.2 Spicy** 🌶️ 是无审查/NSFW 变体，允许不受限制的创意内容生成。可通过以下方式获取：

- **Atlas Cloud API** 仅需 **$0.03/秒起** — 市面上最便宜的无审查视频生成 API
- 模型：`alibaba/wan-2.2-spicy/image-to-video` 和 `alibaba/wan-2.2-spicy/image-to-video-lora`（支持 LoRA）

[在 Atlas Cloud 上试用 Wan 2.2 Spicy →](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video)

</details>

<details>
<summary><b>通过 API 生成 Wan 视频需要多少钱？</b></summary>

Atlas Cloud 提供最实惠的 Wan API 定价：
- **Wan 2.2 Spicy（NSFW）：** $0.03/秒起
- **Wan 2.6 T2V（1080p，15秒）：** $0.07/秒起（7折优惠）
- **Wan 2.5 系列：** 更低价格
- 首次充值 **额外赠送 25%**（最高 $100）

对比 Sora（$0.50+/视频）或 Runway（$0.50+/视频）。[立即开始 →](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video)

</details>

<details>
<summary><b>什么是 Wan 2.6 R2V？</b></summary>

**Wan 2.6 R2V（参考视频生成）** 是一项独特功能，你可以上传一段角色参考视频，同时捕捉人物的 **外观和声音**。模型随后可以生成该角色在新场景中的视频，保持身份一致性。非常适合创建虚拟形象、个性化内容和角色驱动叙事。

</details>

<details>
<summary><b>Wan 2.7 什么时候发布？</b></summary>

**Wan 2.7** 目前正在开发中，即将发布。Atlas Cloud 将是首批提供 Wan 2.7 API 的平台之一。[注册 Atlas Cloud](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video) 以在 Wan 2.7 上线时第一时间获得通知。

</details>

---

## 🌊 立即开始使用 Wan 模型

<div align="center">

**从 Wan Spicy $0.03/秒起到 Wan 2.6 $0.07/秒起 — 最实惠的 AI 视频生成 API。**

| | |
|---|---|
| ✅ **无审查** | Wan 2.2 Spicy 释放不受限制的创意 |
| ✅ **开源 (2.1/2.2)** | 本地运行或通过 API 使用 |
| ✅ **Wan 2.7 即将上线** | 在 Atlas Cloud 上抢先体验 |
| ✅ **25% 奖金** | 首次充值额外赠送（最高 $100） |
| ✅ **全模型覆盖** | T2V、I2V、V2V、图片编辑、换脸、动画 |

<br />

[![在 Atlas Cloud 上试用 Wan](https://img.shields.io/badge/👉%20在%20Atlas%20Cloud%20上试用%20Wan-blue?style=for-the-badge&logo=cloud&logoColor=white)](https://www.atlascloud.ai?ref=JPM683&utm_source=github&utm_campaign=awesome-wan-video)

*无需 GPU。无需配置。只需提示词和视频。*

</div>

---

## ⭐ Star 历史

<div align="center">

如果你觉得这个资源有用，请给个 Star！帮助更多人发现 Wan 生态。

[![Star History Chart](https://api.star-history.com/svg?repos=your-org/awesome-wan-video&type=Date)](https://star-history.com/#your-org/awesome-wan-video&Date)

</div>

---

## 🤝 贡献指南

欢迎贡献！请在提交 PR 前阅读[贡献指南](CONTRIBUTING.md)。

### 如何贡献

1. Fork 本仓库
2. 创建功能分支：`git checkout -b add-new-resource`
3. 在相应部分添加你的资源
4. 提交更改：`git commit -m 'Add new resource'`
5. 推送到分支：`git push origin add-new-resource`
6. 提交 Pull Request

### 我们在寻找

- 新的 Wan 模型工具、扩展和集成
- 社区教程和指南
- LoRA 模型和微调资源
- 带有示例输出的提示词
- 基准测试结果和对比
- 其他语言翻译

---

## 📄 许可证

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

本项目采用 [MIT 许可证](LICENSE) 授权。

---

<div align="center">

**🌊 Wan — 持续突破 AI 视频生成的边界 🌊**

由开源社区用 ❤️ 打造

[⬆ 返回顶部](#-awesome-wan-视频生成)

</div>
