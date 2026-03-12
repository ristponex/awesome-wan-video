<!-- markdownlint-disable MD033 MD041 -->

<div align="center">

# 🌊 Awesome Wan 비디오 생성

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Stars](https://img.shields.io/github/stars/your-org/awesome-wan-video?style=social)](https://github.com/your-org/awesome-wan-video)
[![VBench #1](https://img.shields.io/badge/VBench-No.1%20(86.22%25)-gold?style=flat-square&logo=data:image/svg+xml;base64,PHN2Zy8+)](https://vbench.org)
[![Downloads](https://img.shields.io/badge/다운로드-2.2M+-blue?style=flat-square&logo=huggingface)](https://huggingface.co/Wan-AI)
[![Wan 2.6](https://img.shields.io/badge/최신버전-Wan%202.6-ff6b35?style=flat-square)](https://github.com/Wan-Video/Wan2.6)

**알리바바 Wan 비디오 생성 모델 완전 리소스 가이드**

*세계 1위 오픈소스 AI 비디오 생성 모델 — 엄선된 도구, 프롬프트, 가이드, 리소스 모음.*

[English](./README.md) | [简体中文](./README_zh-CN.md) | [日本語](./README_ja.md) | [한국어](./README_ko.md)

---

🚀 **API로 Wan 비디오 생성 — 요청당 $0.03부터** 🚀

[![Atlas Cloud에서 사용해보기](https://img.shields.io/badge/지금%20사용해보기-Atlas%20Cloud-blue?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?ref=JPM683)

*첫 충전 시 25% 보너스 (최대 $100) • 무검열 Wan Spicy 지원 • Wan 2.7 곧 출시!*

---

</div>

> 🔒 **엔터프라이즈급 보안** — Atlas Cloud는 **SOC I & II 인증** | **HIPAA 준수** | 미국 기업, 99.9% 가동률 SLA 보장.

> 🎨 **NSFW 화이트리스트 업데이트** — Seedance와 Kling 외에도 **Vidu 시리즈** (Q3-Pro, Q3-Turbo)가 Atlas Cloud의 무검열 콘텐츠 생성 화이트리스트에 추가되었습니다.

## 📑 목차

- [Wan 모델 소개](#-wan-모델-소개)
- [모델 비교](#-모델-비교)
- [빠른 시작](#-빠른-시작)
- [프롬프트 컬렉션](#-프롬프트-컬렉션)
- [로컬 배포 가이드](#-로컬-배포-가이드)
- [프롬프트 엔지니어링](#-프롬프트-엔지니어링)
- [API 가격 비교](#-api-가격-비교)
- [공식 리소스](#-공식-리소스)
- [커뮤니티 & 에코시스템](#-커뮤니티--에코시스템)
- [FAQ](#-faq)
- [Star 히스토리](#-star-히스토리)
- [기여하기](#-기여하기)
- [라이선스](#-라이선스)

---

## 🌊 Wan 모델 소개

**Wan**은 알리바바가 개발한 오픈소스 비디오 생성 모델 시리즈입니다. 데뷔 이래 **VBench 리더보드 1위**까지, Wan은 오픈소스 비디오 AI의 한계를 지속적으로 확장하고 있습니다.

### 왜 Wan인가?

- **🏆 VBench 챔피언** — Wan 2.1은 VBench에서 **86.22%** 점수를 달성하여 Sora(84.28%), Luma(83.61%) 등 모든 모델을 능가
- **🔓 완전 오픈소스** — Sora, Kling, Runway와 달리, Wan 모델은 완전 오픈소스로 Hugging Face에서 가중치 다운로드 가능
- **💻 소비자용 GPU 호환** — 1.3B 버전은 **8.19GB VRAM**만 필요, RTX 3060 한 장으로 실행 가능
- **📊 대규모 학습 데이터** — **15억 개의 비디오** + **100억 개의 이미지**로 학습
- **🔥 220만 이상 다운로드** — Hugging Face와 ModelScope에서 글로벌 AI 커뮤니티에 의해 검증
- **🎬 무검열 옵션** — Wan 2.2 Spicy로 무제한 크리에이티브 자유

### 모델 패밀리 트리

```
Wan 1.0 (2024 Q3)
  └── Wan 2.1 (2024 Q4) — VBench 1위, 14B & 1.3B
       └── Wan 2.2 (2025 Q1) — 품질 향상, Spicy 변형 🌶️
            ├── Wan 2.2 Spicy — NSFW/무검열 생성
            └── Wan 2.5 (2025 Q2) — 오디오 동기화, 1080p, 10초
                 └── Wan 2.6 (2025 Q3) — 멀티샷, 15초, 캐릭터 안정성
                      └── Wan 2.7 (곧 출시!) — 🔜 Atlas Cloud에서 최초 제공
```

### 클로즈드 소스 모델과의 주요 차이점

| 기능 | Wan 2.6 | Sora | Kling | Runway Gen-3 |
|------|---------|------|-------|---------------|
| 오픈소스 | ✅ | ❌ | ❌ | ❌ |
| 로컬 배포 | ✅ | ❌ | ❌ | ❌ |
| 최대 해상도 | 1920×1080 | 1920×1080 | 1920×1080 | 1920×1080 |
| 최대 길이 | 15초 | 20초 | 10초 | 10초 |
| 네이티브 오디오 | ✅ | ✅ | ❌ | ❌ |
| 멀티샷 | ✅ | ❌ | ❌ | ❌ |
| NSFW 지원 | ✅ (Spicy) | ❌ | ❌ | ❌ |
| 비디오당 가격 | $0.03부터 | $0.50+ | $0.30+ | $0.50+ |
| 소비자용 GPU | ✅ (1.3B) | N/A | N/A | N/A |
| 파인튜닝 | ✅ LoRA | ❌ | ❌ | ❌ |

---

## 📊 모델 비교

| 버전 | 파라미터 | 해상도 | 길이 | 오디오 | 멀티샷 | 오픈소스 | NSFW | API 가격 |
|------|---------|--------|------|--------|--------|---------|------|---------|
| **Wan 2.6** | 14B | 1080p | 최대 15초 | ✅ | ✅ | ✅ | ❌ | $0.07 |
| **Wan 2.5** | 14B | 1080p | 최대 10초 | ✅ | ❌ | ✅ | ❌ | 더 낮음 |
| **Wan 2.2 Spicy** 🌶️ | 14B | 720p | 최대 8초 | ❌ | ❌ | ✅ | ✅ | **$0.03** |
| **Wan 2.2** | 14B / 1.3B | 720p | 최대 5초 | ❌ | ❌ | ✅ | ❌ | — |
| **Wan 2.1** | 14B / 1.3B | 720p | 최대 5초 | ❌ | ❌ | ✅ | ❌ | — |

### Atlas Cloud에서 사용 가능한 모델

| 모델 | 유형 | 가격 | 하이라이트 |
|------|------|------|-----------|
| Wan 2.6 T2V | 텍스트→비디오 | $0.07/회 (70% 할인) | 5/10/15초, 최대 1920×1080, 멀티샷, 오디오 |
| Wan 2.6 I2V | 이미지→비디오 | 이용 가능 | 고충실도 이미지 애니메이션 |
| Wan 2.6 I2V Flash | 이미지→비디오 | 더 빠르고 저렴 | 속도 최적화 변형 |
| Wan 2.6 V2V | 비디오→비디오 | 이용 가능 | 스타일 전환 & 편집 |
| Wan 2.6 이미지 편집 | 이미지 편집 | 이용 가능 | AI 이미지 편집 |
| Wan 2.6 T2I | 텍스트→이미지 | 이용 가능 | 고품질 이미지 생성 |
| Wan 2.5 T2V | 텍스트→비디오 | 이용 가능 | 안정적인 비디오 생성 |
| Wan 2.5 I2V | 이미지→비디오 | 이용 가능 | 안정적인 이미지 애니메이션 |
| Wan 2.5 Fast | 텍스트→비디오 | 이용 가능 | 속도 최적화 |
| Wan 2.2 Spicy I2V 🌶️ | 이미지→비디오 | **$0.03/회** | 무검열 생성 |
| Wan 2.2 Spicy I2V LoRA | 이미지→비디오 | 이용 가능 | LoRA 파인튜닝 지원 |
| Wan 2.2 캐릭터 스왑 | 비디오 효과 | 이용 가능 | animate-mix 페이스 스왑 |
| Wan 2.2 이미지→애니메이션 | 애니메이션 | 이용 가능 | animate-move 모션 전송 |
| Van 2.6 / 2.5 | 최적화 버전 | 이용 가능 | Atlas Cloud 최적화 변형 |

> 🎁 **신규 사용자 혜택:** 첫 충전 시 25% 보너스 (최대 $100 보너스). [지금 가입 →](https://www.atlascloud.ai?ref=JPM683)

---

## 🚀 빠른 시작

### 옵션 1: API (Atlas Cloud) — 가장 빠른 방법

<details>
<summary><b>cURL 예제 — Wan 2.6 텍스트→비디오</b></summary>

```bash
# Wan 2.6 텍스트에서 비디오 생성 API 호출
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
<summary><b>cURL 예제 — Wan 2.2 Spicy (무검열)</b></summary>

```bash
# Wan 2.2 Spicy 무검열 이미지에서 비디오 API 호출 — 단 $0.03/회
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
<summary><b>Python 예제 — 전체 파이프라인</b></summary>

```python
"""
Wan 비디오 생성 전체 예제
Wan 2.6 T2V, I2V 및 Wan 2.2 Spicy 지원
"""
import requests
import time

# Atlas Cloud API 설정
API_KEY = "YOUR_API_KEY"
BASE_URL = "https://api.atlascloud.ai/v1"

def generate_video(prompt: str, model: str = "wan-2.6-t2v", **kwargs) -> str:
    """
    Wan 모델로 비디오 생성

    매개변수:
        prompt: 비디오 설명 텍스트
        model: 모델 이름, 기본값 Wan 2.6
        **kwargs: duration, resolution 등 추가 매개변수
    반환값:
        비디오 다운로드 URL
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

    # 생성 작업 제출
    response = requests.post(f"{BASE_URL}/video/generate", json=payload, headers=headers)
    task_id = response.json()["task_id"]

    # 결과 폴링
    while True:
        status = requests.get(f"{BASE_URL}/video/status/{task_id}", headers=headers)
        result = status.json()

        if result["status"] == "completed":
            return result["video_url"]
        elif result["status"] == "failed":
            raise Exception(f"생성 실패: {result.get('error', '알 수 없는 오류')}")

        time.sleep(2)  # 2초마다 상태 확인

# ====== 사용 예제 ======

# 예제 1: Wan 2.6 텍스트→비디오 (멀티샷 + 오디오 지원)
video_url = generate_video(
    prompt="A chef preparing sushi in a traditional Japanese kitchen, warm lighting, close-up shots",
    model="wan-2.6-t2v",
    duration=10,
    resolution="1920x1080",
    audio=True
)
print(f"비디오 생성 완료: {video_url}")

# 예제 2: Wan 2.2 Spicy 무검열 생성 (단 $0.03)
spicy_url = generate_video(
    prompt="Artistic figure study, classical painting style, natural movement",
    model="alibaba/wan-2.2-spicy/image-to-video"
)
print(f"Spicy 비디오 생성 완료: {spicy_url}")
```

</details>

### 옵션 2: 로컬 배포 (ComfyUI)

```bash
# 1. ComfyUI 설치
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 2. 의존성 설치
pip install -r requirements.txt

# 3. Wan 2.6 모델 가중치 다운로드
# Hugging Face에서 다운로드 (약 28GB 디스크 공간 필요)
huggingface-cli download Wan-AI/Wan2.6-T2V-14B --local-dir models/wan2.6/

# 4. Wan ComfyUI 노드 설치
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
pip install -r ComfyUI-Wan/requirements.txt

# 5. ComfyUI 시작
cd ..
python main.py --listen 0.0.0.0 --port 8188
```

### 옵션 3: Hugging Face Pipeline

```python
"""
Hugging Face Diffusers 라이브러리를 사용하여 Wan 2.1 로컬 실행
NVIDIA GPU가 있는 환경용
"""
from diffusers import WanPipeline
import torch

# 모델 로드 (1.3B 버전은 8.19GB VRAM만 필요)
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16  # FP16으로 VRAM 절약
)
pipe = pipe.to("cuda")

# 비디오 생성
video = pipe(
    prompt="A golden retriever playing in autumn leaves, slow motion, warm sunlight",
    num_frames=81,        # 약 5초 비디오
    height=480,
    width=720,
    guidance_scale=7.5
).frames[0]

# 비디오 저장
from diffusers.utils import export_to_video
export_to_video(video, "output.mp4", fps=16)
print("비디오가 output.mp4에 저장되었습니다")
```

### 옵션 4: Docker 배포

```dockerfile
# Wan 2.6 Docker 배포 설정
FROM nvidia/cuda:12.1-runtime-ubuntu22.04

# 시스템 의존성 설치
RUN apt-get update && apt-get install -y \
    python3 python3-pip git wget \
    && rm -rf /var/lib/apt/lists/*

# Python 의존성 설치
RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu121
RUN pip3 install diffusers transformers accelerate safetensors

# Wan 모델 다운로드
RUN huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B --local-dir /models/wan

# 추론 스크립트 복사
COPY inference.py /app/inference.py

WORKDIR /app
CMD ["python3", "inference.py"]
```

```bash
# Docker 컨테이너 빌드 및 실행
docker build -t wan-video .
docker run --gpus all -p 8080:8080 wan-video
```

---

## 🎨 프롬프트 컬렉션

> Wan 모델에 최적화된 30개 이상의 엄선된 프롬프트. 각 프롬프트에 전체 텍스트, 권장 모델, 설정, 팁 포함.

### 🎬 시네마틱 & 영화

<details>
<summary><b>1. 장엄한 산악 풍경</b></summary>

- **프롬프트:** `Sweeping aerial shot over snow-capped mountains at golden hour, dramatic clouds casting long shadows across alpine valleys, a winding river reflecting the amber sky, cinematic camera movement slowly pushing forward, volumetric lighting, 8K film grain`
- **모델:** Wan 2.6 T2V
- **길이:** 15초
- **해상도:** 1920×1080
- **팁:** 멀티샷을 활성화하면 더 역동적인 시퀀스가 됩니다. 오디오를 추가하면 바람 소리가 생성됩니다.

</details>

<details>
<summary><b>2. 도시의 야간 추격</b></summary>

- **프롬프트:** `Tracking shot through neon-lit Tokyo streets at night, rain-soaked asphalt reflecting pink and blue neon signs, a figure in a dark coat running through crowds, handheld camera shake, Blade Runner aesthetic, moody atmosphere, cinematic color grading`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** 네거티브 프롬프트 "blurry, low quality, static"을 사용하면 더 선명한 움직임을 얻을 수 있습니다.

</details>

<details>
<summary><b>3. 역사적 전투 장면</b></summary>

- **프롬프트:** `Wide establishing shot of a medieval battlefield at dawn, thousands of soldiers in formation, banners waving in the wind, mist rolling across the field, dramatic orchestral music feel, Lord of the Rings inspired cinematography, epic scale, film grain`
- **모델:** Wan 2.6 T2V
- **길이:** 15초
- **해상도:** 1920×1080
- **팁:** 멀티샷 모드는 이 장면에서 특히 뛰어나며, 와이드와 클로즈업 사이의 컷 전환이 가능합니다.

</details>

<details>
<summary><b>4. 수중 다큐멘터리</b></summary>

- **프롬프트:** `Slow underwater tracking shot through a vibrant coral reef, tropical fish swimming in formation, sunbeams penetrating the crystal-clear blue water, a sea turtle gliding gracefully through the frame, National Geographic style, 4K clarity`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** "smooth camera movement, steady"를 추가하여 수중 흔들림 아티팩트를 방지합니다.

</details>

<details>
<summary><b>5. 필름 누아르 탐정</b></summary>

- **프롬프트:** `Close-up of a detective in a dimly lit office, cigarette smoke curling through a single shaft of light from venetian blinds, black and white film noir style, slow camera dolly in, dramatic shadows, 1940s aesthetic, grain texture`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1280×720
- **팁:** "black and white, monochrome"을 명시적으로 지정하면 일관된 누아르 룩을 얻을 수 있습니다.

</details>

### 🌶️ NSFW / 크리에이티브 프리덤 (Wan 2.2 Spicy)

<details>
<summary><b>6. 고전적 인체 연구</b></summary>

- **프롬프트:** `Renaissance-style figure study, soft diffused lighting on skin, classical painting composition, marble sculpture coming to life with subtle breathing movement, warm golden tones, museum gallery setting, artistic and elegant`
- **모델:** Wan 2.2 Spicy I2V
- **가격:** $0.03/회
- **팁:** 고전 회화나 조각 참조 이미지와 함께 사용하면 최상의 결과를 얻을 수 있습니다.

</details>

<details>
<summary><b>7. 아방가르드 패션 에디토리얼</b></summary>

- **프롬프트:** `High fashion editorial, model in sheer flowing fabric, dramatic wind effect, stark white studio lighting, Helmut Newton inspired, bold poses transitioning fluidly, haute couture, magazine quality`
- **모델:** Wan 2.2 Spicy I2V
- **가격:** $0.03/회
- **팁:** LoRA 변형을 사용하면 여러 생성에서 일관된 스타일을 유지할 수 있습니다.

</details>

<details>
<summary><b>8. 예술적 신체 움직임</b></summary>

- **프롬프트:** `Contemporary dance performance, fluid body movement, dramatic stage lighting, dancer's silhouette against colored backdrop, artistic expression through motion, modern ballet, intimate camera angles, professional choreography`
- **모델:** Wan 2.2 Spicy I2V
- **가격:** $0.03/회
- **팁:** 이미지→비디오 모드가 가장 잘 작동합니다 — 댄서 참조 이미지를 제공하세요.

</details>

<details>
<summary><b>9. 신화 장면</b></summary>

- **프롬프트:** `Birth of Venus reimagined, goddess emerging from ocean waves, flowing golden hair, seashells and foam, Pre-Raphaelite painting style, ethereal glow, mythological beauty, Botticelli inspired but cinematic`
- **모델:** Wan 2.2 Spicy I2V
- **가격:** $0.03/회
- **팁:** 고전 미술 참조 이미지와의 궁합이 뛰어납니다.

</details>

<details>
<summary><b>10. 사이버펑크 캐릭터</b></summary>

- **프롬프트:** `Cyberpunk character in revealing neon-lit outfit, holographic tattoos glowing on skin, futuristic nightclub setting, pulsing LED lights, confident walking motion, sci-fi fashion, Blade Runner 2049 aesthetic`
- **모델:** Wan 2.2 Spicy I2V LoRA
- **가격:** $0.03/회
- **팁:** LoRA를 사용하면 다른 장면에서도 캐릭터 외관을 일관되게 유지할 수 있습니다.

</details>

### 📦 제품 & 상업

<details>
<summary><b>11. 럭셔리 시계 쇼케이스</b></summary>

- **프롬프트:** `Macro close-up of a luxury watch rotating on a black velvet surface, golden light reflections dancing on polished metal, mechanical movement visible through transparent caseback, premium product photography, smooth 360-degree rotation`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** 느리고 제어된 회전이 가장 효과적입니다. "studio lighting, product photography"를 추가하면 상업적 품질이 됩니다.

</details>

<details>
<summary><b>12. 음식 광고 — 커피 붓기</b></summary>

- **프롬프트:** `Slow motion pour of steaming espresso into a white ceramic cup, rich crema forming on surface, steam rising in soft morning light, rustic wooden table, out-of-focus bakery background, food photography, warm color palette, 120fps slow motion feel`
- **모델:** Wan 2.6 T2V
- **길이:** 5초
- **해상도:** 1920×1080
- **팁:** 짧은 길이에 높은 디테일이 음식 콘텐츠에 더 효과적입니다.

</details>

<details>
<summary><b>13. 스니커즈 제품 런칭</b></summary>

- **프롬프트:** `Dynamic sneaker reveal, shoe floating and rotating in mid-air against gradient background, particles and light streaks surrounding the product, dramatic lighting transitions, Nike commercial style, clean product visualization`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** 멀티샷으로 같은 제품을 다양한 각도에서 촬영할 수 있습니다.

</details>

<details>
<summary><b>14. 향수 광고 — 에테리얼</b></summary>

- **프롬프트:** `Glass perfume bottle on a reflective surface, golden liquid catching light, slow motion flower petals falling around it, soft bokeh background, luxury brand commercial aesthetic, Chanel No.5 inspired visual, elegant and sophisticated`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** "glass reflections, caustics, luxury"를 추가하면 프리미엄 느낌이 됩니다.

</details>

<details>
<summary><b>15. 테크 제품 언박싱</b></summary>

- **프롬프트:** `Cinematic unboxing of a sleek smartphone, hands slowly lifting the lid of a minimalist white box, device rising with a subtle glow, holographic interface appearing above the screen, Apple keynote style presentation, clean and modern`
- **모델:** Wan 2.6 I2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** 실제 제품 이미지와 함께 I2V 모드를 사용하면 브랜드 정확성이 향상됩니다.

</details>

### 🎨 애니메이션 & 카툰

<details>
<summary><b>16. 애니메이션 벚꽃 장면</b></summary>

- **프롬프트:** `Anime style, a young girl standing under a blooming cherry blossom tree, pink petals falling in slow motion, gentle breeze moving her hair and school uniform, soft watercolor background, Studio Ghibli aesthetic, warm spring lighting`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1280×720
- **팁:** "anime, cel-shaded, 2D animation"을 추가하면 일관된 애니메이션 스타일이 됩니다.

</details>

<details>
<summary><b>17. 픽셀 아트 어드벤처</b></summary>

- **프롬프트:** `Retro pixel art game scene, 16-bit hero character walking through a mystical forest, glowing mushrooms, floating fireflies, parallax scrolling background layers, SNES-era RPG aesthetic, vibrant pixel colors`
- **모델:** Wan 2.5 T2V
- **길이:** 5초
- **해상도:** 1280×720
- **팁:** 낮은 해상도가 레트로 픽셀 아트 느낌을 향상시킵니다.

</details>

<details>
<summary><b>18. 3D 카툰 캐릭터</b></summary>

- **프롬프트:** `Pixar-style 3D animated character, a small robot with big expressive eyes discovering a flower in a post-apocalyptic landscape, WALL-E inspired, smooth character animation, subsurface scattering on plastic materials, Pixar render quality`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** Wan 2.6은 3D 애니메이션 스타일 처리가 매우 뛰어납니다.

</details>

<details>
<summary><b>19. 만화책 액션</b></summary>

- **프롬프트:** `Marvel comic book style action sequence, superhero landing pose with impact shockwave, bold ink outlines, halftone dot shading, dynamic camera angle from below, speech bubble appearing, vibrant primary colors, Jack Kirby inspired`
- **모델:** Wan 2.6 T2V
- **길이:** 5초
- **해상도:** 1280×720
- **팁:** 짧고 강렬한 액션이 만화책 스타일에 가장 잘 어울립니다.

</details>

<details>
<summary><b>20. 수채화 그림책</b></summary>

- **프롬프트:** `Watercolor illustration coming to life, a fox and rabbit having a tea party in an enchanted forest clearing, soft paint bleeding effects, storybook page turning animation, children's book illustration style, gentle pastel colors, whimsical`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1280×720
- **팁:** "watercolor, illustration, painted" 키워드가 예술적 스타일 유지에 도움됩니다.

</details>

### 🔄 캐릭터 스왑 (Wan 2.2 animate-mix)

<details>
<summary><b>21. 셀러브리티 임프레션</b></summary>

- **프롬프트:** `Professional business presentation, confident speaker at a podium, formal attire, corporate event, smooth gestures and natural speech patterns`
- **모델:** Wan 2.2 캐릭터 스왑 (animate-mix)
- **팁:** 프레젠테이션의 소스 비디오와 타겟 얼굴 이미지를 업로드합니다. 정면, 조명이 좋은 얼굴에서 최적의 결과를 얻을 수 있습니다.

</details>

<details>
<summary><b>22. 역사적 인물 부활</b></summary>

- **프롬프트:** `Historical documentary narration, period-appropriate setting, speaking directly to camera, educational content`
- **모델:** Wan 2.2 캐릭터 스왑 (animate-mix)
- **팁:** 선명하고 고해상도의 참조 사진에서 최상의 결과가 나옵니다. 소스와 타겟 간의 조명 일관성을 유지하세요.

</details>

<details>
<summary><b>23. 뮤직비디오 페이스 스왑</b></summary>

- **프롬프트:** `Music performance, singer on stage, dynamic lighting, emotional expression, concert atmosphere`
- **모델:** Wan 2.2 캐릭터 스왑 (animate-mix)
- **팁:** 얼굴 트래킹이 안정적인 뮤직비디오에서 잘 작동합니다. 극단적인 머리 회전은 피하세요.

</details>

### 🏃 모션 전송 (Wan 2.2 animate-move)

<details>
<summary><b>24. 댄스 안무 전송</b></summary>

- **프롬프트:** `Professional dance routine, hip-hop choreography, studio setting, full body visible, clean background`
- **모델:** Wan 2.2 이미지→애니메이션 (animate-move)
- **팁:** 댄스 비디오를 모션 소스로, 캐릭터 이미지를 업로드합니다. 깨끗한 배경의 전신 촬영이 최적입니다.

</details>

<details>
<summary><b>25. 카툰 캐릭터 애니메이션</b></summary>

- **프롬프트:** `Animated character performing complex movements, cartoon style, expressive body language`
- **모델:** Wan 2.2 이미지→애니메이션 (animate-move)
- **팁:** 실제 사람의 모션 비디오를 사용하여 2D 또는 3D 캐릭터 이미지에 애니메이션을 적용합니다.

</details>

<details>
<summary><b>26. 브랜드 마스코트 애니메이션</b></summary>

- **프롬프트:** `Brand mascot performing fun actions, waving, jumping, dancing, engaging personality`
- **모델:** Wan 2.2 이미지→애니메이션 (animate-move)
- **팁:** 정적인 브랜드 마스코트에 자연스러운 움직임을 부여하는 데 완벽합니다.

</details>

### 🌐 기타 & 고급

<details>
<summary><b>27. 타임랩스 시티</b></summary>

- **프롬프트:** `Hyper-lapse of a modern city skyline from day to night, clouds racing across the sky, lights gradually turning on in skyscrapers, traffic becoming streams of light, star trails appearing, 24-hour cycle compressed into seconds, urban time-lapse`
- **모델:** Wan 2.6 T2V
- **길이:** 15초
- **해상도:** 1920×1080
- **팁:** 15초 길이가 주야간 전환에 이상적입니다.

</details>

<details>
<summary><b>28. 자연 매크로 — 나비 우화</b></summary>

- **프롬프트:** `Extreme macro shot of a monarch butterfly emerging from chrysalis, iridescent wing scales unfolding in slow motion, morning dew drops on wings, shallow depth of field, nature documentary quality, BBC Earth style`
- **모델:** Wan 2.6 T2V
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** 느리고 정밀한 움직임의 매크로 피사체가 놀라운 결과를 만들어냅니다.

</details>

<details>
<summary><b>29. SF 우주 정거장</b></summary>

- **프롬프트:** `Exterior shot of a massive space station orbiting Earth, ISS-inspired design but futuristic, solar panels rotating to track the sun, a shuttle approaching for docking, Earth's blue glow illuminating the structure, Interstellar cinematography`
- **모델:** Wan 2.6 T2V
- **길이:** 15초
- **해상도:** 1920×1080
- **팁:** 오디오를 추가하면 몰입감 있는 우주 분위기가 됩니다. 멀티샷으로 내부/외부 전환이 가능합니다.

</details>

<details>
<summary><b>30. 추상 플루이드 아트</b></summary>

- **프롬프트:** `Abstract fluid art in motion, vibrant acrylic paint pouring and mixing, golden veins forming between color pools, Kandinsky meets Jackson Pollock, mesmerizing organic patterns, satisfying ASMR-like visual, overhead camera view`
- **모델:** Wan 2.5 T2V
- **길이:** 10초
- **해상도:** 1280×720
- **팁:** 추상 콘텐츠는 오류 허용도가 높아 항상 아름다운 결과를 생성합니다.

</details>

<details>
<summary><b>31. Wan 2.6 R2V — 캐릭터 레퍼런스</b></summary>

- **프롬프트:** `캐릭터 참조 비디오를 업로드(외모+음성 캡처)하여 새로운 장면에서 생성: 미래 도시를 걸으며 홀로그래픽 디스플레이와 상호작용, 정확한 외모와 음성 특성 유지`
- **모델:** Wan 2.6 R2V (레퍼런스→비디오)
- **길이:** 10초
- **해상도:** 1920×1080
- **팁:** Wan 2.6 R2V는 참조 비디오에서 캐릭터 아이덴티티(외모+음성)를 유지합니다. 3-5초 참조 클립에서 최상의 결과를 얻을 수 있습니다.

</details>

<details>
<summary><b>32. 멀티샷 내러티브</b></summary>

- **프롬프트:** `Shot 1: Wide establishing shot of a cozy café on a rainy Parisian street. Shot 2: Close-up of hands wrapping around a steaming coffee cup. Shot 3: Looking out the window as rain streams down the glass. Shot 4: Slow zoom out revealing the full café scene with warm interior lighting.`
- **모델:** Wan 2.6 T2V (멀티샷)
- **길이:** 15초
- **해상도:** 1920×1080
- **팁:** "Shot N:" 접두사로 장면을 분리하여 멀티샷 기능을 사용합니다. Wan 2.6이 샷 간 부드러운 전환을 만들어줍니다.

</details>

---

## 🖥️ 로컬 배포 가이드

### 하드웨어 요구사항

| 컴포넌트 | Wan 2.6 (14B) | Wan 2.1 (14B) | Wan 2.1 (1.3B) |
|---------|---------------|---------------|-----------------|
| **GPU VRAM** | 24GB 이상 | 24GB 이상 | **8.19GB** |
| **권장 GPU** | RTX 4090 / A100 | RTX 4090 / A100 | RTX 3060 12GB |
| **시스템 RAM** | 32GB 이상 | 32GB 이상 | 16GB |
| **디스크 공간** | 약 56GB | 약 28GB | 약 5GB |
| **OS** | Linux / Windows | Linux / Windows | Linux / Windows |
| **CUDA** | 12.1 이상 | 11.8 이상 | 11.8 이상 |

### ComfyUI 설정 (단계별)

```bash
# ======== 1단계: ComfyUI 설치 ========
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 가상 환경 생성 (권장)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# PyTorch 설치 (CUDA 12.1)
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# ComfyUI 의존성 설치
pip install -r requirements.txt

# ======== 2단계: Wan 노드 설치 ========
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
cd ComfyUI-Wan
pip install -r requirements.txt
cd ../..

# ======== 3단계: 모델 다운로드 ========
# 옵션 A: 전체 14B 모델 (권장, 24GB 이상 VRAM 필요)
huggingface-cli download Wan-AI/Wan2.6-T2V-14B \
    --local-dir models/wan2.6-14b/

# 옵션 B: 경량 1.3B 모델 (8.19GB VRAM만 필요)
huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B \
    --local-dir models/wan2.1-1.3b/

# ======== 4단계: ComfyUI 시작 ========
python main.py --listen 0.0.0.0 --port 8188

# 브라우저에서 http://localhost:8188 접속
# Wan 워크플로우 노드를 임포트하여 사용
```

### GPU 메모리 최적화 팁

```python
"""
VRAM 최적화 기법, 소비자용 GPU에서 Wan 모델 실행에 유용
"""
import torch
from diffusers import WanPipeline

# 기법 1: 반정밀 부동소수점 사용 (약 50% VRAM 절약)
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-14B",
    torch_dtype=torch.float16
)

# 기법 2: 어텐션 슬라이싱 활성화 (VRAM 피크를 크게 감소)
pipe.enable_attention_slicing(slice_size="auto")

# 기법 3: VAE 슬라이싱 활성화 (비디오 프레임을 단계적으로 디코딩)
pipe.enable_vae_slicing()

# 기법 4: CPU 오프로딩 활성화 (비활성 모듈을 자동으로 CPU로 이동)
pipe.enable_model_cpu_offload()

# 기법 5: xformers로 가속 (xformers 추가 설치 필요)
# pip install xformers
pipe.enable_xformers_memory_efficient_attention()

# 기법 6: 해상도와 프레임 수 낮추기
video = pipe(
    prompt="Your prompt here",
    num_frames=49,       # 프레임 수 줄이기 (49프레임 ≈ 3초)
    height=480,          # 해상도 낮추기
    width=720,
    guidance_scale=7.5
).frames[0]

# 기법 7: 14B 대신 1.3B 모델 사용
# 1.3B 모델은 8.19GB VRAM만 필요하며 품질도 우수
pipe_light = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16
).to("cuda")
```

---

## ✍️ 프롬프트 엔지니어링

### Wan 전용 효과적인 키워드

| 카테고리 | 효과적인 키워드 |
|---------|---------------|
| **화질** | `8K, cinematic, film grain, high detail, professional, masterpiece` |
| **카메라** | `tracking shot, dolly zoom, aerial shot, close-up, macro, wide angle` |
| **조명** | `golden hour, volumetric lighting, rim lighting, neon glow, soft diffused` |
| **모션** | `slow motion, time-lapse, smooth pan, gentle movement, dynamic action` |
| **스타일** | `photorealistic, anime, watercolor, oil painting, cyberpunk, noir` |
| **분위기** | `dramatic, ethereal, cozy, epic, melancholic, whimsical` |

### 네거티브 프롬프트 전략

```
# 권장 범용 네거티브 프롬프트
blurry, low quality, distorted, deformed, ugly, bad anatomy,
watermark, text overlay, logo, pixelated, noise, artifacts,
oversaturated, underexposed, static image, no movement,
extra fingers, missing limbs, unnatural proportions
```

### 멀티샷 기법 (Wan 2.6)

```
# 멀티샷 내러티브 템플릿
Shot 1: [와이드/확립 샷] - 환경과 맥락으로 장면 설정
Shot 2: [미디엄] - 피사체 또는 캐릭터 소개
Shot 3: [클로즈업] - 감정적 디테일 또는 핵심 액션
Shot 4: [와이드/풀백] - 결말 또는 리빌

# 예시: 커피 광고 멀티샷
Shot 1: 일출 시 콜롬비아 커피 농장의 항공 촬영, 아침 안개.
Shot 2: 잘 익은 커피 체리를 따는 농부의 손.
Shot 3: 로스팅되는 커피 원두의 극단적 클로즈업, 오일이 반짝임.
Shot 4: 모던 카페에서 갓 내린 커피에서 피어오르는 김.
```

### 오디오 생성 제어 (Wan 2.6)

Wan 2.6은 네이티브 오디오 동기화를 지원합니다. 최상의 결과를 위한 팁:

- **환경음**은 시각적 콘텐츠를 기반으로 자동 생성
- 프롬프트에 오디오 단서 추가: `"birds chirping"`, `"rain on window"`, `"crowd cheering"`
- 더 긴 길이(10-15초)에서 오디오 품질 향상
- API 호출에서 `audio: true`로 오디오 생성 활성화

### 해상도 vs 속도 트레이드오프

| 해상도 | VRAM 사용량 | 생성 시간 | 최적 용도 |
|--------|-----------|---------|---------|
| 1920×1080 | 약 24GB | 약 3-5분 | 최종 프로덕션 |
| 1280×720 | 약 16GB | 약 1-3분 | 초안 & 테스트 |
| 854×480 | 약 10GB | 약 30-60초 | 빠른 프로토타이핑 |
| 640×360 | 약 8GB | 약 15-30초 | 빠른 미리보기 |

---

## 💰 API 가격 비교

| 제공업체 | Wan 2.6 T2V | Wan 2.5 T2V | Wan Spicy 🌶️ | 주요 기능 |
|---------|-------------|-------------|---------------|---------|
| **Atlas Cloud** ⭐ | **$0.07/회** (70% 할인) | 더 낮음 | **$0.03/회** | ✅ 전 모델, NSFW, LoRA, V2V, 멀티샷 |
| Alibaba Cloud | $0.10 이상 | $0.08 이상 | N/A | ⚠️ 리전 제한, NSFW 없음 |
| Replicate | $0.15 이상 | $0.12 이상 | 제한적 | 기본 API만 |
| 자체 호스팅 | GPU 시간 비용 | GPU 시간 비용 | GPU 시간 비용 | ✅ 완전 제어, ❌ 유지보수 부담 |

### 비용 분석 예시

| 사용 사례 | 모델 | 월간 생성량 | Atlas Cloud 비용 | 자체 호스팅 (A100) |
|---------|------|----------|-----------------|---------------------|
| SNS 크리에이터 | Wan 2.6 T2V | 500개 | **$35/월** | 약 $500/월 |
| NSFW 아트 크리에이터 | Wan Spicy | 1,000개 | **$30/월** | 약 $500/월 |
| 상업 제작 | Wan 2.6 T2V | 100개 | **$7/월** | 약 $500/월 |
| 취미 사용자 | Wan 2.5 T2V | 50개 | **$5 미만/월** | 약 $500/월 |

> 💡 **프로 팁:** [Atlas Cloud에 가입](https://www.atlascloud.ai?ref=JPM683)하면 첫 충전 시 **25% 보너스** (최대 $100 보너스). $100+$25 보너스로 최대 1,785개의 Wan Spicy 비디오 또는 Wan 2.6 비디오 생성 가능!

### Atlas Cloud vs fal.ai 가격 비교

| 모델 | fal.ai 가격 | Atlas Cloud 가격 | 절약 |
|:------|:------------|:-----------------|:---------|
| **Kling** | $0.224/초 (5초 = $1.12) | $0.204/회 | **82% 저렴** |
| **Seedance** | ~$0.26/영상 | $0.222/회 | **15% 저렴** |
| **Wan 2.5** | $0.05/초 (5초 = $0.25) | $0.05/회 | **80% 저렴** |
| **Wan 2.6** | 유사한 가격 | $0.07/회 | 경쟁력 있음 |
| **Veo 3** | $0.40/초 (8초 = $3.20) | TBD | 곧 출시 |
| **Vidu Q3-Pro** | — | $0.06/회 | Atlas 독점 |
| **Vidu Q3-Turbo** | — | $0.034/회 | Atlas 독점 |

> 💡 Atlas Cloud는 모든 주요 비디오 모델에서 **최저가**를 제공합니다. fal.ai에서 전환하여 비디오 생성 비용을 최대 **82%** 절약하세요.

---

## 📚 공식 리소스

### 모델 가중치 & 다운로드

| 리소스 | 링크 | 참고 |
|-------|------|------|
| Hugging Face — Wan-AI | [huggingface.co/Wan-AI](https://huggingface.co/Wan-AI) | 전체 모델 가중치 |
| ModelScope — Wan | [modelscope.cn/Wan-Video](https://modelscope.cn/organization/Wan-Video) | 대체 다운로드 (아시아에서 더 빠름) |
| Wan 2.6 T2V 14B | [HF 링크](https://huggingface.co/Wan-AI/Wan2.6-T2V-14B) | 최신 텍스트→비디오 |
| Wan 2.6 I2V 14B | [HF 링크](https://huggingface.co/Wan-AI/Wan2.6-I2V-14B) | 최신 이미지→비디오 |
| Wan 2.1 T2V 1.3B | [HF 링크](https://huggingface.co/Wan-AI/Wan2.1-T2V-1.3B) | 경량 버전, 소비자용 GPU |

### 논문 & 연구

| 논문 | 링크 | 설명 |
|------|------|------|
| Wan 2.1 기술 보고서 | [arXiv](https://arxiv.org/abs/2503.20314) | 아키텍처 & 학습 세부사항 |
| VBench 리더보드 | [vbench.org](https://vbench.org) | 벤치마크 랭킹 |

### 공식 GitHub 저장소

| 저장소 | 설명 |
|-------|------|
| [Wan-Video/Wan2.6](https://github.com/Wan-Video/Wan2.6) | Wan 2.6 공식 코드 |
| [Wan-Video/Wan2.1](https://github.com/Wan-Video/Wan2.1) | Wan 2.1 공식 코드 |

---

## 🌐 커뮤니티 & 에코시스템

### ComfyUI 확장

| 확장 | 설명 | 스타 |
|------|------|------|
| [ComfyUI-Wan](https://github.com/Wan-Video/ComfyUI-Wan) | 공식 Wan ComfyUI 노드 | ⭐ |
| [ComfyUI-WanVideoWrapper](https://github.com/kijai/ComfyUI-WanVideoWrapper) | 커뮤니티 래퍼 (추가 기능 포함) | ⭐ |

### LoRA 모델 & 파인튜닝

| 리소스 | 설명 |
|-------|------|
| [Civitai — Wan LoRAs](https://civitai.com/models?tags=wan) | 커뮤니티 학습 LoRA 모델 |
| [Wan LoRA 학습 가이드](https://github.com/Wan-Video/Wan2.1/blob/main/docs/lora.md) | 공식 파인튜닝 문서 |

### 커뮤니티 허브

| 플랫폼 | 링크 |
|-------|------|
| Reddit — r/WanVideo | [reddit.com/r/WanVideo](https://reddit.com/r/WanVideo) |
| Discord — Wan 커뮤니티 | 커뮤니티 Discord 서버 |
| Twitter/X — #WanVideo | [#WanVideo 검색](https://twitter.com/search?q=%23WanVideo) |

### 튜토리얼 & 가이드

| 제목 | 유형 | 링크 |
|------|------|------|
| Wan 2.6 완전 가이드 | 영상 | YouTube |
| ComfyUI + Wan 워크플로우 | 글 | 블로그 |
| Wan LoRA 학습 튜토리얼 | 영상 | YouTube |
| Wan vs Kling vs Sora 비교 | 글 | 블로그 |

---

## ❓ FAQ

<details>
<summary><b>Wan AI 비디오 모델이란 무엇인가요?</b></summary>

Wan은 알리바바의 오픈소스 비디오 생성 모델 시리즈입니다. 확산 트랜스포머 아키텍처를 사용하며, 15억 개의 비디오와 100억 개의 이미지로 학습되었습니다. Wan 2.1 모델은 **VBench 리더보드에서 1위**를 달성했으며, 86.22%의 점수로 Sora(84.28%)와 Luma(83.61%)를 능가했습니다. 최신 버전은 **Wan 2.6**으로, 네이티브 오디오 동기화와 함께 최대 15초의 멀티샷 1080p 비디오 생성을 지원합니다.

</details>

<details>
<summary><b>Wan을 로컬에서 실행하려면 어떻게 하나요?</b></summary>

다음 방법으로 Wan을 로컬에서 실행할 수 있습니다:
1. **ComfyUI** — Wan ComfyUI 노드를 설치하고 모델 가중치를 다운로드
2. **Hugging Face Diffusers** — Python에서 `WanPipeline` 클래스 사용
3. **Docker** — 제공된 Dockerfile로 배포

**1.3B 모델은 8.19GB VRAM만 필요**하여 RTX 3060 같은 소비자용 GPU에서도 접근 가능합니다. 14B 모델은 24GB 이상의 VRAM(RTX 4090 또는 A100)이 필요합니다.

자세한 단계는 [로컬 배포 가이드](#-로컬-배포-가이드)를 참조하세요.

</details>

<details>
<summary><b>Wan vs Seedance vs Kling — 어떤 것이 더 나은가요?</b></summary>

| 기능 | Wan 2.6 | Seedance | Kling |
|------|---------|----------|-------|
| 오픈소스 | ✅ | ❌ | ❌ |
| 최대 길이 | 15초 | 10초 | 10초 |
| 오디오 | ✅ | ❌ | ❌ |
| 멀티샷 | ✅ | ❌ | ❌ |
| NSFW | ✅ (Spicy) | ❌ | ❌ |
| 로컬 배포 | ✅ | ❌ | ❌ |
| API 가격 | $0.03부터 | $0.20 이상 | $0.30 이상 |

**Wan의 강점:** 오픈소스 유연성, 가격, NSFW 지원, 로컬 배포, 풍부한 기능. Seedance와 Kling은 특정 사용 사례에서 모션 품질이 다를 수 있지만, Wan의 오픈소스 특성과 빠른 발전으로 장기적으로 최선의 선택입니다.

</details>

<details>
<summary><b>Wan 2.6에 가장 좋은 GPU는 무엇인가요?</b></summary>

| GPU | VRAM | 실행 가능 | 성능 |
|-----|------|---------|------|
| RTX 3060 12GB | 12GB | ✅ (1.3B만) | 기본 |
| RTX 3090 | 24GB | ✅ (14B 최적화 필요) | 양호 |
| RTX 4090 | 24GB | ✅ (14B 풀 스피드) | 우수 |
| A100 40GB | 40GB | ✅ (모든 모델, 배치) | 전문가 |
| A100 80GB | 80GB | ✅ (모든 모델, 고배치) | 엔터프라이즈 |

**예산 추천:** 로컬 배포에는 RTX 4090, 또는 하드웨어에 투자하고 싶지 않다면 [Atlas Cloud API](https://www.atlascloud.ai?ref=JPM683)를 비디오당 $0.03부터 이용하세요.

</details>

<details>
<summary><b>무검열 Wan 모델이 있나요?</b></summary>

**네!** **Wan 2.2 Spicy** 🌶️는 무검열/NSFW 변형으로, 제한 없는 크리에이티브 콘텐츠 생성이 가능합니다. 다음에서 이용 가능합니다:

- **Atlas Cloud API** 단 **$0.03/회** — 시중에서 가장 저렴한 무검열 비디오 생성 API
- 모델: `alibaba/wan-2.2-spicy/image-to-video` 및 `alibaba/wan-2.2-spicy/image-to-video-lora` (LoRA 지원)

[Atlas Cloud에서 Wan 2.2 Spicy 사용해보기 →](https://www.atlascloud.ai?ref=JPM683)

</details>

<details>
<summary><b>API를 통한 Wan 비디오 생성 비용은 얼마인가요?</b></summary>

Atlas Cloud는 가장 합리적인 Wan API 가격을 제공합니다:
- **Wan 2.2 Spicy (NSFW):** $0.03/회
- **Wan 2.6 T2V (1080p, 15초):** $0.07/회 (70% 할인)
- **Wan 2.5 변형:** 더 낮은 가격
- 첫 충전 시 **25% 보너스** (최대 $100)

Sora($0.50+/비디오)나 Runway($0.50+/비디오)와 비교해보세요. [시작하기 →](https://www.atlascloud.ai?ref=JPM683)

</details>

<details>
<summary><b>Wan 2.6 R2V란 무엇인가요?</b></summary>

**Wan 2.6 R2V (레퍼런스→비디오)**는 캐릭터 참조 비디오를 업로드하여 해당 인물의 **외모와 음성** 모두를 캡처하는 독특한 기능입니다. 모델은 동일한 캐릭터가 새로운 장면에 등장하는 비디오를 생성하며, 아이덴티티 일관성을 유지합니다. 가상 아바타, 맞춤형 콘텐츠, 캐릭터 중심 내러티브 제작에 최적입니다.

</details>

<details>
<summary><b>Wan 2.7은 언제 출시되나요?</b></summary>

**Wan 2.7**은 현재 개발 중이며 곧 출시될 예정입니다. Atlas Cloud는 Wan 2.7을 API로 제공하는 최초의 플랫폼 중 하나가 될 것입니다. [Atlas Cloud에 가입](https://www.atlascloud.ai?ref=JPM683)하여 Wan 2.7 런칭 시 알림을 받으세요.

</details>

---

## 🌊 Wan 모델로 창작 시작하기

<div align="center">

**Wan Spicy $0.03/비디오부터 Wan 2.6 $0.07까지 — 가장 합리적인 AI 비디오 생성 API.**

| | |
|---|---|
| ✅ **무검열** | Wan 2.2 Spicy로 무제한 크리에이티비티 |
| ✅ **오픈소스** | 로컬 실행 또는 API 이용 |
| ✅ **Wan 2.7 곧 출시** | Atlas Cloud에서 선행 접근 |
| ✅ **25% 보너스** | 첫 충전 시 (최대 $100 보너스) |
| ✅ **전 모델 지원** | T2V, I2V, V2V, 이미지 편집, 캐릭터 스왑, 애니메이션 |

<br />

[![Atlas Cloud에서 Wan 사용해보기](https://img.shields.io/badge/👉%20Atlas%20Cloud에서%20Wan%20사용해보기-blue?style=for-the-badge&logo=cloud&logoColor=white)](https://www.atlascloud.ai?ref=JPM683)

*GPU도 설정도 필요 없습니다. 프롬프트만 입력하면 비디오가 완성됩니다.*

</div>

---

## ⭐ Star 히스토리

<div align="center">

이 리소스가 유용했다면 Star를 눌러주세요! 다른 사람들이 Wan 에코시스템을 발견하는 데 도움이 됩니다.

[![Star History Chart](https://api.star-history.com/svg?repos=your-org/awesome-wan-video&type=Date)](https://star-history.com/#your-org/awesome-wan-video&Date)

</div>

---

## 🤝 기여하기

기여를 환영합니다! PR을 제출하기 전에 [기여 가이드라인](CONTRIBUTING.md)을 읽어주세요.

### 기여 방법

1. 이 저장소를 Fork
2. 기능 브랜치 생성: `git checkout -b add-new-resource`
3. 적절한 섹션에 리소스 추가
4. 변경사항 커밋: `git commit -m 'Add new resource'`
5. 브랜치에 푸시: `git push origin add-new-resource`
6. Pull Request 제출

### 찾고 있는 것들

- 새로운 Wan 모델 도구, 확장, 통합
- 커뮤니티 튜토리얼 및 가이드
- LoRA 모델 및 파인튜닝 리소스
- 샘플 출력이 포함된 프롬프트 예시
- 벤치마크 결과 및 비교
- 다른 언어로의 번역

---

## 📄 라이선스

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

이 프로젝트는 [MIT 라이선스](LICENSE)로 제공됩니다.

---

<div align="center">

**🌊 Wan — AI 비디오 생성을 모든 사람에게 개방적이고 접근 가능하게 🌊**

오픈소스 커뮤니티가 ❤️ 를 담아 제작

[⬆ 맨 위로 돌아가기](#-awesome-wan-비디오-생성)

</div>
