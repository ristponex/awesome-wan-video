<!-- markdownlint-disable MD033 MD041 -->

<div align="center">

# 🌊 Awesome Wan Video Generation

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Stars](https://img.shields.io/github/stars/your-org/awesome-wan-video?style=social)](https://github.com/your-org/awesome-wan-video)
[![VBench #1](https://img.shields.io/badge/VBench-No.1%20(86.22%25)-gold?style=flat-square&logo=data:image/svg+xml;base64,PHN2Zy8+)](https://vbench.org)
[![Downloads](https://img.shields.io/badge/Downloads-2.2M+-blue?style=flat-square&logo=huggingface)](https://huggingface.co/Wan-AI)
[![Wan 2.6](https://img.shields.io/badge/Latest-Wan%202.6-ff6b35?style=flat-square)](https://github.com/Wan-Video/Wan2.6)

**The Complete Resource for Alibaba Wan Video Generation Models**

*The world's leading AI video generation model family — open-source models (2.1/2.2) & cutting-edge API (2.5/2.6). Curated tools, prompts, guides, and resources.*

[English](./README.md) | [简体中文](./README_zh-CN.md) | [日本語](./README_ja.md) | [한국어](./README_ko.md)

---

🚀 **Generate Wan Videos via API — from $0.03/s** 🚀

[![Try on Atlas Cloud](https://img.shields.io/badge/Try%20Now-Atlas%20Cloud-blue?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?ref=JPM683)

*25% bonus on first recharge (up to $100) • Uncensored Wan Spicy available • Wan 2.7 coming soon!*

---

</div>

> 🔒 **Enterprise-Grade Security** — Atlas Cloud is **SOC I & II Certified** | **HIPAA Compliant** | US-based company with 99.9% uptime SLA.

> 🎨 **NSFW Whitelist Update** — In addition to Seedance and Kling, the **Vidu series** (Q3-Pro, Q3-Turbo) is now also whitelisted for uncensored content generation on Atlas Cloud.

## 📑 Table of Contents

- [About Wan Models](#-about-wan-models)
- [Model Comparison](#-model-comparison)
- [Quick Start](#-quick-start)
- [Prompt Collection](#-prompt-collection)
- [Local Deployment Guide](#-local-deployment-guide)
- [Prompt Engineering](#-prompt-engineering)
- [API Pricing Comparison](#-api-pricing-comparison)
- [Official Resources](#-official-resources)
- [Community & Ecosystem](#-community--ecosystem)
- [FAQ](#-faq)
- [Star History](#-star-history)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌊 About Wan Models

**Wan** is Alibaba's video generation model series that has taken the AI world by storm. Wan 2.1 and 2.2 are **fully open-source** (Apache 2.0) with weights available on Hugging Face, while Wan 2.5 and 2.6 are **closed-source commercial API** models with advanced capabilities. From its debut to its current **#1 position on the VBench leaderboard**, Wan has consistently pushed the boundaries of video AI.

### Why Wan?

- **🏆 VBench Champion** — Wan 2.1 scored **86.22%** on VBench, surpassing Sora (84.28%), Luma (83.61%), and all other models
- **🔓 Open Source (2.1/2.2)** — Unlike Sora, Kling, or Runway, Wan 2.1/2.2 are fully open-source (Apache 2.0) with weights available on Hugging Face for self-deployment
- **💻 Consumer GPU Friendly** — The 1.3B version needs only **8.19GB VRAM**, runs on a single RTX 3060
- **📊 Massive Training Data** — Trained on **1.5 billion videos** + **10 billion images**
- **🔥 2.2M+ Downloads** — Proven and validated by the global AI community on Hugging Face and ModelScope
- **🎬 Uncensored Option** — Wan 2.2 Spicy enables unrestricted creative freedom

### Model Family Tree

```
Wan 1.0 (2024 Q3)
  └── Wan 2.1 (2024 Q4) — VBench #1, 14B & 1.3B [Open Source, Apache 2.0]
       └── Wan 2.2 (2025 Q1) — Improved quality, Spicy variant 🌶️ [Open Source, Apache 2.0]
            ├── Wan 2.2 Spicy — NSFW/Uncensored generation [Proprietary, Atlas Cloud LoRA]
            └── Wan 2.5 (2025 Q2) — Audio sync, 1080p, 10s [Closed Source, API only]
                 └── Wan 2.6 (2025 Q3) — Multi-shot, 15s, character stability [Closed Source, API only]
                      └── Wan 2.7 (Coming Soon!) — 🔜 First on Atlas Cloud
```

### Key Differentiators vs Closed-Source Models

| Feature | Wan 2.1/2.2 | Wan 2.5/2.6 | Sora | Kling | Runway Gen-3 |
|---------|-------------|-------------|------|-------|---------------|
| Open Source | ✅ Apache 2.0 | ❌ API only | ❌ | ❌ | ❌ |
| Local Deployment | ✅ | ❌ | ❌ | ❌ | ❌ |
| Max Resolution | 720p | 1920×1080 | 1920×1080 | 1920×1080 | 1920×1080 |
| Max Duration | 5s | 15s | 20s | 10s | 10s |
| Native Audio | ❌ | ✅ | ✅ | ❌ | ❌ |
| Multi-Shot | ❌ | ✅ | ❌ | ❌ | ❌ |
| NSFW Support | ✅ (Spicy) | ❌ | ❌ | ❌ | ❌ |
| Price / Video | Self-host | From $0.03 | $0.50+ | $0.30+ | $0.50+ |
| Consumer GPU | ✅ (1.3B) | N/A | N/A | N/A | N/A |
| Fine-tuning | ✅ LoRA | ❌ | ❌ | ❌ | ❌ |

---

## 📊 Model Comparison

| Version | Parameters | Resolution | Duration | Audio | Multi-Shot | Open Source | NSFW | API Price |
|---------|-----------|------------|----------|-------|------------|------------|------|-----------|
| **Wan 2.6** | 14B | 1080p | Up to 15s | ✅ | ✅ | ❌ (API only) | ❌ | $0.07 |
| **Wan 2.5** | 14B | 1080p | Up to 10s | ✅ | ❌ | ❌ (API only) | ❌ | Lower |
| **Wan 2.2 Spicy** 🌶️ | 14B | 720p | Up to 8s | ❌ | ❌ | ✅ | ✅ | **$0.03** |
| **Wan 2.2** | 14B / 1.3B | 720p | Up to 5s | ❌ | ❌ | ✅ | ❌ | — |
| **Wan 2.1** | 14B / 1.3B | 720p | Up to 5s | ❌ | ❌ | ✅ | ❌ | — |

### Available Models on Atlas Cloud

| Model | Type | Price | Highlights |
|-------|------|-------|------------|
| Wan 2.6 T2V | Text-to-Video | from $0.07/s (70% off) | 5/10/15s, up to 1920×1080, multi-shot, audio |
| Wan 2.6 I2V | Image-to-Video | Available | High-fidelity image animation |
| Wan 2.6 I2V Flash | Image-to-Video | Faster & cheaper | Speed-optimized variant |
| Wan 2.6 V2V | Video-to-Video | Available | Style transfer & editing |
| Wan 2.6 Image-Edit | Image Editing | Available | AI-powered image editing |
| Wan 2.6 T2I | Text-to-Image | Available | High-quality image generation |
| Wan 2.5 T2V | Text-to-Video | Available | Reliable video generation |
| Wan 2.5 I2V | Image-to-Video | Available | Stable image animation |
| Wan 2.5 Fast | Text-to-Video | Available | Speed-optimized |
| Wan 2.2 Spicy I2V 🌶️ | Image-to-Video | **from $0.03/s** | Uncensored generation |
| Wan 2.2 Spicy I2V LoRA | Image-to-Video | Available | LoRA fine-tuning support |
| Wan 2.2 Character Swap | Video Effects | Available | animate-mix face swap |
| Wan 2.2 Image-to-Animation | Animation | Available | animate-move motion transfer |
| Van 2.6 / 2.5 | Optimized | Available | Atlas Cloud optimized variants |

> *Prices shown are starting prices per second of generated video. Actual cost depends on resolution, duration, and model selected.*

> 🎁 **New user offer:** 25% bonus on first recharge (up to $100). [Sign up now →](https://www.atlascloud.ai?ref=JPM683)

---

## 🚀 Quick Start

### Option 1: API (Atlas Cloud) — Fastest Way

<details>
<summary><b>cURL Example — Wan 2.6 Text-to-Video</b></summary>

```bash
# Wan 2.6 Text-to-Video API call
curl -X POST "https://api.atlascloud.ai/v1/video/generate" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "wan-2.6-t2v",
    "prompt": "A majestic dragon soaring through clouds at sunset, cinematic lighting, 4K quality",
    "duration": 10,
    "resolution": "1920x1080",
    "audio": true
  }'
```

</details>

<details>
<summary><b>cURL Example — Wan 2.2 Spicy (Uncensored)</b></summary>

```bash
# Wan 2.2 Spicy Uncensored Image-to-Video API call — only from $0.03/s
curl -X POST "https://api.atlascloud.ai/v1/video/generate" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "alibaba/wan-2.2-spicy/image-to-video",
    "image_url": "https://example.com/your-image.jpg",
    "prompt": "Smooth natural movement, artistic expression, high quality"
  }'
```

</details>

<details>
<summary><b>Python Example — Full Pipeline</b></summary>

```python
"""
Complete Wan video generation example
Supports Wan 2.6 T2V, I2V, and Wan 2.2 Spicy
"""
import requests
import time

# Atlas Cloud API configuration
API_KEY = "YOUR_API_KEY"
BASE_URL = "https://api.atlascloud.ai/v1"

def generate_video(prompt: str, model: str = "wan-2.6-t2v", **kwargs) -> str:
    """
    Call Wan model to generate video

    Args:
        prompt: Video description text
        model: Model name, defaults to Wan 2.6
        **kwargs: Other parameters such as duration, resolution, etc.
    Returns:
        Video download URL
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

    # Submit generation task
    response = requests.post(f"{BASE_URL}/video/generate", json=payload, headers=headers)
    task_id = response.json()["task_id"]

    # Poll for results
    while True:
        status = requests.get(f"{BASE_URL}/video/status/{task_id}", headers=headers)
        result = status.json()

        if result["status"] == "completed":
            return result["video_url"]
        elif result["status"] == "failed":
            raise Exception(f"Generation failed: {result.get('error', 'Unknown error')}")

        time.sleep(2)  # Check status every 2 seconds

# ====== Usage Examples ======

# Example 1: Wan 2.6 Text-to-Video (supports multi-shot + audio)
video_url = generate_video(
    prompt="A chef preparing sushi in a traditional Japanese kitchen, warm lighting, close-up shots",
    model="wan-2.6-t2v",
    duration=10,
    resolution="1920x1080",
    audio=True
)
print(f"Video generated: {video_url}")

# Example 2: Wan 2.2 Spicy Uncensored generation (only $0.03)
spicy_url = generate_video(
    prompt="Artistic figure study, classical painting style, natural movement",
    model="alibaba/wan-2.2-spicy/image-to-video"
)
print(f"Spicy video generated: {spicy_url}")
```

</details>

### Option 2: Local Deployment (ComfyUI)

```bash
# 1. Install ComfyUI
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download Wan 2.6 model weights
# Download from Hugging Face (requires approximately 28GB disk space)
huggingface-cli download Wan-AI/Wan2.6-T2V-14B --local-dir models/wan2.6/

# 4. Install Wan ComfyUI nodes
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
pip install -r ComfyUI-Wan/requirements.txt

# 5. Launch ComfyUI
cd ..
python main.py --listen 0.0.0.0 --port 8188
```

### Option 3: Hugging Face Pipeline

```python
"""
Run Wan 2.1 locally using the Hugging Face Diffusers library
Suitable for users with NVIDIA GPUs
"""
from diffusers import WanPipeline
import torch

# Load model (1.3B version only needs 8.19GB VRAM)
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16
)
pipe = pipe.to("cuda")

# Generate video
video = pipe(
    prompt="A golden retriever playing in autumn leaves, slow motion, warm sunlight",
    num_frames=81,        # approximately 5 second video
    height=480,
    width=720,
    guidance_scale=7.5
).frames[0]

# Save video
from diffusers.utils import export_to_video
export_to_video(video, "output.mp4", fps=16)
print("Video saved to output.mp4")
```

### Option 4: Docker Deployment

```dockerfile
# Wan 2.6 Docker deployment configuration
FROM nvidia/cuda:12.1-runtime-ubuntu22.04

# Install system dependencies
RUN apt-get update && apt-get install -y \
    python3 python3-pip git wget \
    && rm -rf /var/lib/apt/lists/*

# Install Python dependencies
RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu121
RUN pip3 install diffusers transformers accelerate safetensors

# Download Wan model
RUN huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B --local-dir /models/wan

# Copy inference script
COPY inference.py /app/inference.py

WORKDIR /app
CMD ["python3", "inference.py"]
```

```bash
# Build and run Docker container
docker build -t wan-video .
docker run --gpus all -p 8080:8080 wan-video
```

---

## 🎨 Prompt Collection

> 30+ carefully crafted prompts optimized for Wan models. Each includes the full prompt text, recommended model, settings, and tips.

### 🎬 Cinematic & Film

<details>
<summary><b>1. Epic Mountain Landscape</b></summary>

- **Prompt:** `Sweeping aerial shot over snow-capped mountains at golden hour, dramatic clouds casting long shadows across alpine valleys, a winding river reflecting the amber sky, cinematic camera movement slowly pushing forward, volumetric lighting, 8K film grain`
- **Model:** Wan 2.6 T2V
- **Duration:** 15s
- **Resolution:** 1920×1080
- **Tips:** Enable multi-shot for a more dynamic sequence. Add audio for ambient wind sounds.

</details>

<details>
<summary><b>2. Urban Night Chase</b></summary>

- **Prompt:** `Tracking shot through neon-lit Tokyo streets at night, rain-soaked asphalt reflecting pink and blue neon signs, a figure in a dark coat running through crowds, handheld camera shake, Blade Runner aesthetic, moody atmosphere, cinematic color grading`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Use negative prompt "blurry, low quality, static" for sharper motion.

</details>

<details>
<summary><b>3. Historical Battle Scene</b></summary>

- **Prompt:** `Wide establishing shot of a medieval battlefield at dawn, thousands of soldiers in formation, banners waving in the wind, mist rolling across the field, dramatic orchestral music feel, Lord of the Rings inspired cinematography, epic scale, film grain`
- **Model:** Wan 2.6 T2V
- **Duration:** 15s
- **Resolution:** 1920×1080
- **Tips:** Multi-shot mode works exceptionally well here for cut transitions between wide and close-up shots.

</details>

<details>
<summary><b>4. Underwater Documentary</b></summary>

- **Prompt:** `Slow underwater tracking shot through a vibrant coral reef, tropical fish swimming in formation, sunbeams penetrating the crystal-clear blue water, a sea turtle gliding gracefully through the frame, National Geographic style, 4K clarity`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Add "smooth camera movement, steady" to avoid shaky underwater artifacts.

</details>

<details>
<summary><b>5. Noir Detective Scene</b></summary>

- **Prompt:** `Close-up of a detective in a dimly lit office, cigarette smoke curling through a single shaft of light from venetian blinds, black and white film noir style, slow camera dolly in, dramatic shadows, 1940s aesthetic, grain texture`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1280×720
- **Tips:** Specify "black and white, monochrome" explicitly for consistent noir look.

</details>

### 🌶️ NSFW / Creative Freedom (Wan 2.2 Spicy)

<details>
<summary><b>6. Classical Figure Study</b></summary>

- **Prompt:** `Renaissance-style figure study, soft diffused lighting on skin, classical painting composition, marble sculpture coming to life with subtle breathing movement, warm golden tones, museum gallery setting, artistic and elegant`
- **Model:** Wan 2.2 Spicy I2V
- **Price:** from $0.03/s
- **Tips:** Pair with a classical painting or sculpture reference image for best results.

</details>

<details>
<summary><b>7. Fashion Editorial Avant-Garde</b></summary>

- **Prompt:** `High fashion editorial, model in sheer flowing fabric, dramatic wind effect, stark white studio lighting, Helmut Newton inspired, bold poses transitioning fluidly, haute couture, magazine quality`
- **Model:** Wan 2.2 Spicy I2V
- **Price:** from $0.03/s
- **Tips:** Use LoRA variant for consistent style across multiple generations.

</details>

<details>
<summary><b>8. Artistic Body Movement</b></summary>

- **Prompt:** `Contemporary dance performance, fluid body movement, dramatic stage lighting, dancer's silhouette against colored backdrop, artistic expression through motion, modern ballet, intimate camera angles, professional choreography`
- **Model:** Wan 2.2 Spicy I2V
- **Price:** from $0.03/s
- **Tips:** Image-to-video works best — provide a dancer reference image.

</details>

<details>
<summary><b>9. Mythological Scene</b></summary>

- **Prompt:** `Birth of Venus reimagined, goddess emerging from ocean waves, flowing golden hair, seashells and foam, Pre-Raphaelite painting style, ethereal glow, mythological beauty, Botticelli inspired but cinematic`
- **Model:** Wan 2.2 Spicy I2V
- **Price:** from $0.03/s
- **Tips:** Works beautifully with classical art reference images.

</details>

<details>
<summary><b>10. Cyberpunk Character</b></summary>

- **Prompt:** `Cyberpunk character in revealing neon-lit outfit, holographic tattoos glowing on skin, futuristic nightclub setting, pulsing LED lights, confident walking motion, sci-fi fashion, Blade Runner 2049 aesthetic`
- **Model:** Wan 2.2 Spicy I2V LoRA
- **Price:** from $0.03/s
- **Tips:** Use LoRA for consistent character appearance across scenes.

</details>

### 📦 Product & Commercial

<details>
<summary><b>11. Luxury Watch Showcase</b></summary>

- **Prompt:** `Macro close-up of a luxury watch rotating on a black velvet surface, golden light reflections dancing on polished metal, mechanical movement visible through transparent caseback, premium product photography, smooth 360-degree rotation`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Slow, controlled rotation works best. Add "studio lighting, product photography" for commercial quality.

</details>

<details>
<summary><b>12. Food Commercial — Coffee Pour</b></summary>

- **Prompt:** `Slow motion pour of steaming espresso into a white ceramic cup, rich crema forming on surface, steam rising in soft morning light, rustic wooden table, out-of-focus bakery background, food photography, warm color palette, 120fps slow motion feel`
- **Model:** Wan 2.6 T2V
- **Duration:** 5s
- **Resolution:** 1920×1080
- **Tips:** Short duration with high detail works better for food content.

</details>

<details>
<summary><b>13. Sneaker Product Launch</b></summary>

- **Prompt:** `Dynamic sneaker reveal, shoe floating and rotating in mid-air against gradient background, particles and light streaks surrounding the product, dramatic lighting transitions, Nike commercial style, clean product visualization`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Use multi-shot for different angles of the same product.

</details>

<details>
<summary><b>14. Perfume Ad — Ethereal</b></summary>

- **Prompt:** `Glass perfume bottle on a reflective surface, golden liquid catching light, slow motion flower petals falling around it, soft bokeh background, luxury brand commercial aesthetic, Chanel No.5 inspired visual, elegant and sophisticated`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Add "glass reflections, caustics, luxury" for premium feel.

</details>

<details>
<summary><b>15. Tech Product Unboxing</b></summary>

- **Prompt:** `Cinematic unboxing of a sleek smartphone, hands slowly lifting the lid of a minimalist white box, device rising with a subtle glow, holographic interface appearing above the screen, Apple keynote style presentation, clean and modern`
- **Model:** Wan 2.6 I2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Use I2V with an actual product image for brand accuracy.

</details>

### 🎨 Animation & Cartoon

<details>
<summary><b>16. Anime Sakura Scene</b></summary>

- **Prompt:** `Anime style, a young girl standing under a blooming cherry blossom tree, pink petals falling in slow motion, gentle breeze moving her hair and school uniform, soft watercolor background, Studio Ghibli aesthetic, warm spring lighting`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1280×720
- **Tips:** Add "anime, cel-shaded, 2D animation" for consistent style.

</details>

<details>
<summary><b>17. Pixel Art Adventure</b></summary>

- **Prompt:** `Retro pixel art game scene, 16-bit hero character walking through a mystical forest, glowing mushrooms, floating fireflies, parallax scrolling background layers, SNES-era RPG aesthetic, vibrant pixel colors`
- **Model:** Wan 2.5 T2V
- **Duration:** 5s
- **Resolution:** 1280×720
- **Tips:** Lower resolution enhances the retro pixel art feel.

</details>

<details>
<summary><b>18. 3D Cartoon Character</b></summary>

- **Prompt:** `Pixar-style 3D animated character, a small robot with big expressive eyes discovering a flower in a post-apocalyptic landscape, WALL-E inspired, smooth character animation, subsurface scattering on plastic materials, Pixar render quality`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Wan 2.6 handles 3D animation styles remarkably well.

</details>

<details>
<summary><b>19. Comic Book Action</b></summary>

- **Prompt:** `Marvel comic book style action sequence, superhero landing pose with impact shockwave, bold ink outlines, halftone dot shading, dynamic camera angle from below, speech bubble appearing, vibrant primary colors, Jack Kirby inspired`
- **Model:** Wan 2.6 T2V
- **Duration:** 5s
- **Resolution:** 1280×720
- **Tips:** Short bursts of action work best for comic book style.

</details>

<details>
<summary><b>20. Watercolor Storybook</b></summary>

- **Prompt:** `Watercolor illustration coming to life, a fox and rabbit having a tea party in an enchanted forest clearing, soft paint bleeding effects, storybook page turning animation, children's book illustration style, gentle pastel colors, whimsical`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1280×720
- **Tips:** "Watercolor, illustration, painted" keywords help maintain the artistic style.

</details>

### 🔄 Character Swap (Wan 2.2 animate-mix)

<details>
<summary><b>21. Celebrity Impression</b></summary>

- **Prompt:** `Professional business presentation, confident speaker at a podium, formal attire, corporate event, smooth gestures and natural speech patterns`
- **Model:** Wan 2.2 Character Swap (animate-mix)
- **Tips:** Upload a source video of the presentation and a target face image. Works best with front-facing, well-lit source faces.

</details>

<details>
<summary><b>22. Historical Figure Revival</b></summary>

- **Prompt:** `Historical documentary narration, period-appropriate setting, speaking directly to camera, educational content`
- **Model:** Wan 2.2 Character Swap (animate-mix)
- **Tips:** Best results with clear, high-resolution reference photos. Maintain consistent lighting between source and target.

</details>

<details>
<summary><b>23. Music Video Face Swap</b></summary>

- **Prompt:** `Music performance, singer on stage, dynamic lighting, emotional expression, concert atmosphere`
- **Model:** Wan 2.2 Character Swap (animate-mix)
- **Tips:** Works well with music videos that have stable face tracking. Avoid extreme head rotations.

</details>

### 🏃 Motion Transfer (Wan 2.2 animate-move)

<details>
<summary><b>24. Dance Choreography Transfer</b></summary>

- **Prompt:** `Professional dance routine, hip-hop choreography, studio setting, full body visible, clean background`
- **Model:** Wan 2.2 Image-to-Animation (animate-move)
- **Tips:** Upload a dance video as motion source and a character image. Full-body shots with clean backgrounds work best.

</details>

<details>
<summary><b>25. Cartoon Character Animation</b></summary>

- **Prompt:** `Animated character performing complex movements, cartoon style, expressive body language`
- **Model:** Wan 2.2 Image-to-Animation (animate-move)
- **Tips:** Use a real person's motion video to animate any 2D or 3D character image.

</details>

<details>
<summary><b>26. Product Mascot Animation</b></summary>

- **Prompt:** `Brand mascot performing fun actions, waving, jumping, dancing, engaging personality`
- **Model:** Wan 2.2 Image-to-Animation (animate-move)
- **Tips:** Perfect for bringing static brand mascots to life with natural movement.

</details>

### 🌐 Miscellaneous & Advanced

<details>
<summary><b>27. Time-Lapse City</b></summary>

- **Prompt:** `Hyper-lapse of a modern city skyline from day to night, clouds racing across the sky, lights gradually turning on in skyscrapers, traffic becoming streams of light, star trails appearing, 24-hour cycle compressed into seconds, urban time-lapse`
- **Model:** Wan 2.6 T2V
- **Duration:** 15s
- **Resolution:** 1920×1080
- **Tips:** 15s duration is ideal for day-to-night transitions.

</details>

<details>
<summary><b>28. Nature Macro — Butterfly Emergence</b></summary>

- **Prompt:** `Extreme macro shot of a monarch butterfly emerging from chrysalis, iridescent wing scales unfolding in slow motion, morning dew drops on wings, shallow depth of field, nature documentary quality, BBC Earth style`
- **Model:** Wan 2.6 T2V
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Macro subjects with slow, deliberate motion produce stunning results.

</details>

<details>
<summary><b>29. Sci-Fi Space Station</b></summary>

- **Prompt:** `Exterior shot of a massive space station orbiting Earth, ISS-inspired design but futuristic, solar panels rotating to track the sun, a shuttle approaching for docking, Earth's blue glow illuminating the structure, Interstellar cinematography`
- **Model:** Wan 2.6 T2V
- **Duration:** 15s
- **Resolution:** 1920×1080
- **Tips:** Add audio for immersive space ambience. Multi-shot for interior/exterior cuts.

</details>

<details>
<summary><b>30. Abstract Art in Motion</b></summary>

- **Prompt:** `Abstract fluid art in motion, vibrant acrylic paint pouring and mixing, golden veins forming between color pools, Kandinsky meets Jackson Pollock, mesmerizing organic patterns, satisfying ASMR-like visual, overhead camera view`
- **Model:** Wan 2.5 T2V
- **Duration:** 10s
- **Resolution:** 1280×720
- **Tips:** Abstract content is very forgiving and consistently produces beautiful results.

</details>

<details>
<summary><b>31. Wan 2.6 R2V — Character Reference</b></summary>

- **Prompt:** `Upload a reference video of a person (captures look + voice), then generate them in a new scene: walking through a futuristic city, interacting with holographic displays, maintaining exact appearance and voice characteristics`
- **Model:** Wan 2.6 R2V (Reference-to-Video)
- **Duration:** 10s
- **Resolution:** 1920×1080
- **Tips:** Wan 2.6 R2V maintains character identity (appearance + voice) from a reference video. Provide 3-5 second reference clip for best results.

</details>

<details>
<summary><b>32. Multi-Shot Narrative</b></summary>

- **Prompt:** `Shot 1: Wide establishing shot of a cozy café on a rainy Parisian street. Shot 2: Close-up of hands wrapping around a steaming coffee cup. Shot 3: Looking out the window as rain streams down the glass. Shot 4: Slow zoom out revealing the full café scene with warm interior lighting.`
- **Model:** Wan 2.6 T2V (Multi-Shot)
- **Duration:** 15s
- **Resolution:** 1920×1080
- **Tips:** Use the multi-shot feature by separating scenes with "Shot N:" prefix. Wan 2.6 will create smooth transitions between shots.

</details>

---

## 🖥️ Local Deployment Guide

### Hardware Requirements

| Component | Wan 2.6 (14B) | Wan 2.1 (14B) | Wan 2.1 (1.3B) |
|-----------|---------------|---------------|-----------------|
| **GPU VRAM** | 24GB+ | 24GB+ | **8.19GB** |
| **Recommended GPU** | RTX 4090 / A100 | RTX 4090 / A100 | RTX 3060 12GB |
| **System RAM** | 32GB+ | 32GB+ | 16GB |
| **Disk Space** | ~56GB | ~28GB | ~5GB |
| **OS** | Linux / Windows | Linux / Windows | Linux / Windows |
| **CUDA** | 12.1+ | 11.8+ | 11.8+ |

### ComfyUI Setup (Step-by-Step)

```bash
# ======== Step 1: Install ComfyUI ========
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# Create virtual environment (Recommended)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# Install PyTorch (CUDA 12.1)
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# Install ComfyUI dependencies
pip install -r requirements.txt

# ======== Step 2: Install Wan Nodes ========
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
cd ComfyUI-Wan
pip install -r requirements.txt
cd ../..

# ======== Step 3: Download Models ========
# Option A: Full 14B model (Recommended, but requires 24GB+ VRAM)
huggingface-cli download Wan-AI/Wan2.6-T2V-14B \
    --local-dir models/wan2.6-14b/

# Option B: Lightweight 1.3B model (only needs 8.19GB VRAM)
huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B \
    --local-dir models/wan2.1-1.3b/

# ======== Step 4: Launch ComfyUI ========
python main.py --listen 0.0.0.0 --port 8188

# Open in browser http://localhost:8188
# Import Wan workflow nodes to start using
```

### GPU Memory Optimization Tips

```python
"""
VRAM optimization tips to help run Wan models on consumer GPUs
"""
import torch
from diffusers import WanPipeline

# Tip 1: Use half-precision floating point (save approximately 50% VRAM)
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-14B",
    torch_dtype=torch.float16  # Use FP16 instead of FP32
)

# Tip 2: Enable attention slicing (significantly reduce peak VRAM usage)
pipe.enable_attention_slicing(slice_size="auto")

# Tip 3: Enable VAE slicing (progressively decode video frames)
pipe.enable_vae_slicing()

# Tip 4: Enable CPU offload (automatically move inactive modules to CPU)
pipe.enable_model_cpu_offload()

# Tip 5: Use xformers for acceleration (requires additional installation of xformers)
# pip install xformers
pipe.enable_xformers_memory_efficient_attention()

# Tip 6: Reduce resolution and frame count
video = pipe(
    prompt="Your prompt here",
    num_frames=49,       # Reduce frame count (49 frames ≈ 3 seconds)
    height=480,          # Reduce resolution
    width=720,
    guidance_scale=7.5
).frames[0]

# Tip 7: Use 1.3B model instead of 14B
# 1.3B model only needs 8.19GB VRAM, quality remains excellent
pipe_light = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16
).to("cuda")
```

---

## ✍️ Prompt Engineering

### Wan-Specific Keywords That Work Well

| Category | Effective Keywords |
|----------|-------------------|
| **Quality** | `8K, cinematic, film grain, high detail, professional, masterpiece` |
| **Camera** | `tracking shot, dolly zoom, aerial shot, close-up, macro, wide angle` |
| **Lighting** | `golden hour, volumetric lighting, rim lighting, neon glow, soft diffused` |
| **Motion** | `slow motion, time-lapse, smooth pan, gentle movement, dynamic action` |
| **Style** | `photorealistic, anime, watercolor, oil painting, cyberpunk, noir` |
| **Mood** | `dramatic, ethereal, cozy, epic, melancholic, whimsical` |

### Negative Prompt Strategies

```
# Recommended universal negative prompts
blurry, low quality, distorted, deformed, ugly, bad anatomy,
watermark, text overlay, logo, pixelated, noise, artifacts,
oversaturated, underexposed, static image, no movement,
extra fingers, missing limbs, unnatural proportions
```

### Multi-Shot Techniques (Wan 2.6)

```
# Multi-shot narrative template
Shot 1: [Wide/Establishing] - Set the scene with environment and context
Shot 2: [Medium] - Introduce the subject or character
Shot 3: [Close-up] - Emotional detail or key action
Shot 4: [Wide/Pull-back] - Resolution or reveal

# Example: Coffee commercial multi-shot
Shot 1: Aerial view of a Colombian coffee plantation at sunrise, morning mist.
Shot 2: Farmer's weathered hands picking ripe coffee cherries.
Shot 3: Extreme close-up of coffee beans being roasted, oils glistening.
Shot 4: Steam rising from a freshly poured cup in a modern café.
```

### Audio Generation Control (Wan 2.6)

Wan 2.6 supports native audio synchronization. Tips for best results:

- **Environmental sounds** are generated automatically based on visual content
- Add audio-specific cues in your prompt: `"birds chirping"`, `"rain on window"`, `"crowd cheering"`
- Audio quality improves with longer duration (10-15s)
- Use `audio: true` in API calls to enable audio generation

### Resolution vs Speed Tradeoffs

| Resolution | VRAM Usage | Generation Time | Best For |
|-----------|------------|-----------------|----------|
| 1920×1080 | ~24GB | ~3-5 min | Final production |
| 1280×720 | ~16GB | ~1-3 min | Draft & testing |
| 854×480 | ~10GB | ~30-60s | Rapid prototyping |
| 640×360 | ~8GB | ~15-30s | Quick preview |

---

## 💰 API Pricing Comparison

| Provider | Wan 2.6 T2V | Wan 2.5 T2V | Wan Spicy 🌶️ | Key Features |
|----------|-------------|-------------|---------------|--------------|
| **Atlas Cloud** ⭐ | **from $0.07/s** (70% off) | Lower | **from $0.03/s** | ✅ All models, NSFW, LoRA, V2V, Multi-shot |
| Alibaba Cloud | $0.10+ | $0.08+ | N/A | ⚠️ Region restricted, no NSFW |
| Replicate | $0.15+ | $0.12+ | Limited | Basic API only |
| Self-hosted | GPU cost/hr | GPU cost/hr | GPU cost/hr | ✅ Full control, ❌ maintenance burden |

> *Prices shown are starting prices per second of generated video. Actual cost depends on resolution, duration, and model selected.*

### Cost Breakdown Example

| Use Case | Model | Videos/Month | Atlas Cloud Cost | Self-Hosted (A100) |
|----------|-------|-------------|-----------------|---------------------|
| Social Media Creator | Wan 2.6 T2V | 500 | **$35/mo** | ~$500/mo |
| NSFW Art Creator | Wan Spicy | 1,000 | **$30/mo** | ~$500/mo |
| Commercial Production | Wan 2.6 T2V | 100 | **$7/mo** | ~$500/mo |
| Hobbyist | Wan 2.5 T2V | 50 | **<$5/mo** | ~$500/mo |

> 💡 **Pro tip:** [Sign up for Atlas Cloud](https://www.atlascloud.ai?ref=JPM683) and get **25% bonus on your first recharge** (up to $100 bonus). That's up to 1,785 Wan Spicy videos or 1,785+ Wan 2.6 videos for $100+$25 bonus!

### Atlas Cloud vs fal.ai Pricing

| Model | fal.ai Price | Atlas Cloud Price | You Save |
|:------|:------------|:-----------------|:---------|
| **Kling** | $0.224/sec (5s = $1.12) | from $0.204/s | **82% cheaper** |
| **Seedance** | ~$0.26/video | from $0.044/s | **15% cheaper** |
| **Wan 2.5** | $0.05/sec (5s = $0.25) | from $0.05/s | **80% cheaper** |
| **Wan 2.6** | Similar pricing | from $0.07/s | Competitive |
| **Veo 3** | $0.40/sec (8s = $3.20) | TBD | Coming soon |
| **Vidu Q3-Pro** | — | from $0.06/s | Atlas exclusive |
| **Vidu Q3-Turbo** | — | from $0.034/s | Atlas exclusive |

> *Prices shown are starting prices per second of generated video. Actual cost depends on resolution, duration, and model selected.*

> 💡 Atlas Cloud offers the **lowest prices** across all major video models. Switch from fal.ai and save up to **82%** on your video generation costs.

---

## 📚 Official Resources

### Model Weights & Downloads

| Resource | Link | Notes |
|----------|------|-------|
| Hugging Face — Wan-AI | [huggingface.co/Wan-AI](https://huggingface.co/Wan-AI) | All model weights |
| ModelScope — Wan | [modelscope.cn/Wan-Video](https://modelscope.cn/organization/Wan-Video) | Alternative download (faster in Asia) |
| Wan 2.6 T2V 14B | [HF Link](https://huggingface.co/Wan-AI/Wan2.6-T2V-14B) | Latest text-to-video |
| Wan 2.6 I2V 14B | [HF Link](https://huggingface.co/Wan-AI/Wan2.6-I2V-14B) | Latest image-to-video |
| Wan 2.1 T2V 1.3B | [HF Link](https://huggingface.co/Wan-AI/Wan2.1-T2V-1.3B) | Lightweight, consumer GPU |

### Papers & Research

| Paper | Link | Description |
|-------|------|-------------|
| Wan 2.1 Technical Report | [arXiv](https://arxiv.org/abs/2503.20314) | Architecture & training details |
| VBench Leaderboard | [vbench.org](https://vbench.org) | Benchmark rankings |

### Official GitHub Repositories

| Repository | Description |
|------------|-------------|
| [Wan-Video/Wan2.6](https://github.com/Wan-Video/Wan2.6) | Wan 2.6 official code |
| [Wan-Video/Wan2.1](https://github.com/Wan-Video/Wan2.1) | Wan 2.1 official code |

---

## 🌐 Community & Ecosystem

### ComfyUI Extensions

| Extension | Description | Stars |
|-----------|-------------|-------|
| [ComfyUI-Wan](https://github.com/Wan-Video/ComfyUI-Wan) | Official Wan nodes for ComfyUI | ⭐ |
| [ComfyUI-WanVideoWrapper](https://github.com/kijai/ComfyUI-WanVideoWrapper) | Community wrapper with extra features | ⭐ |

### LoRA Models & Fine-Tuning

| Resource | Description |
|----------|-------------|
| [Civitai — Wan LoRAs](https://civitai.com/models?tags=wan) | Community-trained LoRA models |
| [Wan LoRA Training Guide](https://github.com/Wan-Video/Wan2.1/blob/main/docs/lora.md) | Official fine-tuning documentation |

### Community Hubs

| Platform | Link |
|----------|------|
| Reddit — r/WanVideo | [reddit.com/r/WanVideo](https://reddit.com/r/WanVideo) |
| Discord — Wan Community | Community Discord server |
| Twitter/X — #WanVideo | [Search #WanVideo](https://twitter.com/search?q=%23WanVideo) |

### Tutorials & Guides

| Title | Type | Link |
|-------|------|------|
| Wan 2.6 Complete Guide | Video | YouTube |
| ComfyUI + Wan Workflow | Article | Blog |
| Wan LoRA Training Tutorial | Video | YouTube |
| Wan vs Kling vs Sora Comparison | Article | Blog |

---

## ❓ FAQ

<details>
<summary><b>What is the Wan AI video model?</b></summary>

Wan is Alibaba's video generation model series. Wan 2.1 and 2.2 are **open-source (Apache 2.0)** with weights available on Hugging Face for self-deployment, while Wan 2.5 and 2.6 are **closed-source commercial API** models. It uses a diffusion transformer architecture trained on 1.5 billion videos and 10 billion images. The Wan 2.1 model achieved the **#1 position on the VBench leaderboard** with a score of 86.22%, surpassing Sora (84.28%) and Luma (83.61%). The latest version is **Wan 2.6**, which supports multi-shot 1080p video generation up to 15 seconds with native audio synchronization, available via API.

</details>

<details>
<summary><b>How to run Wan locally?</b></summary>

You can run Wan locally using:
1. **ComfyUI** — Install the Wan ComfyUI nodes and download model weights
2. **Hugging Face Diffusers** — Use the `WanPipeline` class in Python
3. **Docker** — Deploy with our provided Dockerfile

The **1.3B model requires only 8.19GB VRAM**, making it accessible on consumer GPUs like the RTX 3060. The 14B model needs 24GB+ VRAM (RTX 4090 or A100).

See the [Local Deployment Guide](#-local-deployment-guide) for step-by-step instructions.

</details>

<details>
<summary><b>Wan vs Seedance vs Kling — Which is better?</b></summary>

| Feature | Wan 2.6 | Seedance | Kling |
|---------|---------|----------|-------|
| Open Source | ❌ (2.1/2.2 are open) | ❌ | ❌ |
| Max Duration | 15s | 10s | 10s |
| Audio | ✅ | ❌ | ❌ |
| Multi-Shot | ✅ | ❌ | ❌ |
| NSFW | ✅ (Spicy) | ❌ | ❌ |
| Local Deploy | ❌ (2.1/2.2 can) | ❌ | ❌ |
| API Price | From $0.03 | $0.20+ | $0.30+ |

**Wan wins on**: pricing, NSFW support, and features. Wan 2.1/2.2 offer open-source flexibility with local deployment, while Wan 2.5/2.6 provide cutting-edge quality via API. Seedance and Kling may have slightly different motion quality for specific use cases, but Wan's rapid iteration makes it the best long-term choice.

</details>

<details>
<summary><b>What is the best GPU for Wan 2.6?</b></summary>

| GPU | VRAM | Can Run | Performance |
|-----|------|---------|-------------|
| RTX 3060 12GB | 12GB | ✅ (1.3B only) | Basic |
| RTX 3090 | 24GB | ✅ (14B with optimization) | Good |
| RTX 4090 | 24GB | ✅ (14B full speed) | Excellent |
| A100 40GB | 40GB | ✅ (all models, batch) | Professional |
| A100 80GB | 80GB | ✅ (all models, high batch) | Enterprise |

**Budget recommendation:** RTX 4090 for local deployment, or use [Atlas Cloud API](https://www.atlascloud.ai?ref=JPM683) from $0.03/s if you don't want to invest in hardware.

</details>

<details>
<summary><b>Is there an uncensored Wan model?</b></summary>

**Yes!** The **Wan 2.2 Spicy** 🌶️ is an uncensored/NSFW variant that allows unrestricted creative content generation. It's available via:

- **Atlas Cloud API** at just **from $0.03/s** — the cheapest uncensored video generation API available
- Models: `alibaba/wan-2.2-spicy/image-to-video` and `alibaba/wan-2.2-spicy/image-to-video-lora` (with LoRA support)

[Try Wan 2.2 Spicy on Atlas Cloud →](https://www.atlascloud.ai?ref=JPM683)

</details>

<details>
<summary><b>How much does Wan video generation cost via API?</b></summary>

Atlas Cloud offers the most affordable Wan API pricing:
- **Wan 2.2 Spicy (NSFW):** from $0.03/s
- **Wan 2.6 T2V (1080p, 15s):** from $0.07/s (70% discount)
- **Wan 2.5 variants:** Even lower pricing
- **25% bonus** on first recharge (up to $100)

Compare this to Sora ($0.50+/video) or Runway ($0.50+/video). [Get started →](https://www.atlascloud.ai?ref=JPM683)

</details>

<details>
<summary><b>What is Wan 2.6 R2V?</b></summary>

**Wan 2.6 R2V (Reference-to-Video)** is a unique feature where you upload a character reference video that captures both the person's **appearance and voice**. The model then generates new video scenes featuring that same character with consistent identity. This is perfect for creating virtual avatars, personalized content, and character-driven narratives.

</details>

<details>
<summary><b>When is Wan 2.7 coming out?</b></summary>

**Wan 2.7** is currently in development and will be available soon. Atlas Cloud will be among the first platforms to offer Wan 2.7 via API. [Sign up for Atlas Cloud](https://www.atlascloud.ai?ref=JPM683) to be notified when Wan 2.7 launches.

</details>

---

## 🌊 Start Creating with Wan Models

<div align="center">

**From $0.03/s with Wan Spicy to $0.07/s for Wan 2.6 — the most affordable AI video generation API.**

| | |
|---|---|
| ✅ **Uncensored** | Wan 2.2 Spicy for unrestricted creativity |
| ✅ **Open Source (2.1/2.2)** | Run locally or use via API |
| ✅ **Wan 2.7 Coming Soon** | Be the first to access on Atlas Cloud |
| ✅ **25% Bonus** | On first top-up (up to $100 bonus) |
| ✅ **All Models** | T2V, I2V, V2V, Image-Edit, Character Swap, Animation |

<br />

[![Try Wan on Atlas Cloud](https://img.shields.io/badge/👉%20Try%20Wan%20on%20Atlas%20Cloud-blue?style=for-the-badge&logo=cloud&logoColor=white)](https://www.atlascloud.ai?ref=JPM683)

*No GPU required. No setup. Just prompts and videos.*

</div>

---

## ⭐ Star History

<div align="center">

If you find this resource helpful, please give it a star! It helps others discover the Wan ecosystem.

[![Star History Chart](https://api.star-history.com/svg?repos=your-org/awesome-wan-video&type=Date)](https://star-history.com/#your-org/awesome-wan-video&Date)

</div>

---

## 🤝 Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) before submitting a PR.

### How to Contribute

1. Fork this repository
2. Create your feature branch: `git checkout -b add-new-resource`
3. Add your resource in the appropriate section
4. Commit your changes: `git commit -m 'Add new resource'`
5. Push to the branch: `git push origin add-new-resource`
6. Submit a pull request

### What We're Looking For

- New Wan model tools, extensions, and integrations
- Community tutorials and guides
- LoRA models and fine-tuning resources
- Prompt examples with sample outputs
- Benchmark results and comparisons
- Translations to other languages

---

## 📄 License

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

This work is licensed under the [MIT License](LICENSE).

---

<div align="center">

**🌊 Wan — Pushing the Boundaries of AI Video Generation 🌊**

Made with ❤️ by the open-source community

[⬆ Back to Top](#-awesome-wan-video-generation)

</div>
