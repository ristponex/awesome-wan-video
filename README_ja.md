<!-- markdownlint-disable MD033 MD041 -->

<div align="center">

# 🌊 Awesome Wan 動画生成

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Stars](https://img.shields.io/github/stars/your-org/awesome-wan-video?style=social)](https://github.com/your-org/awesome-wan-video)
[![VBench #1](https://img.shields.io/badge/VBench-No.1%20(86.22%25)-gold?style=flat-square&logo=data:image/svg+xml;base64,PHN2Zy8+)](https://vbench.org)
[![Downloads](https://img.shields.io/badge/ダウンロード-2.2M+-blue?style=flat-square&logo=huggingface)](https://huggingface.co/Wan-AI)
[![Wan 2.6](https://img.shields.io/badge/最新版-Wan%202.6-ff6b35?style=flat-square)](https://github.com/Wan-Video/Wan2.6)

**Alibaba Wan 動画生成モデルの完全リソースガイド**

*世界1位のオープンソースAI動画生成モデル — 厳選されたツール、プロンプト、ガイド、リソース集。*

[English](./README.md) | [简体中文](./README_zh-CN.md) | [日本語](./README_ja.md) | [한국어](./README_ko.md)

---

🚀 **API経由でWan動画を生成 — 1リクエスト$0.03から** 🚀

[![Atlas Cloudで試す](https://img.shields.io/badge/今すぐ試す-Atlas%20Cloud-blue?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?ref=JPM683)

*初回チャージで25%ボーナス（最大$100）• 無検閲Wan Spicy対応 • Wan 2.7近日公開！*

---

</div>

> 🔒 **エンタープライズグレードのセキュリティ** — Atlas Cloud は **SOC I & II 認証取得** | **HIPAA 準拠** | 米国企業、99.9% 稼働率 SLA 保証。

> 🎨 **NSFW ホワイトリスト更新** — Seedance と Kling に加えて、**Vidu シリーズ**（Q3-Pro、Q3-Turbo）も Atlas Cloud の検閲なしコンテンツ生成ホワイトリストに追加されました。

## 📑 目次

- [Wanモデルについて](#-wanモデルについて)
- [モデル比較](#-モデル比較)
- [クイックスタート](#-クイックスタート)
- [プロンプトコレクション](#-プロンプトコレクション)
- [ローカルデプロイガイド](#-ローカルデプロイガイド)
- [プロンプトエンジニアリング](#-プロンプトエンジニアリング)
- [API料金比較](#-api料金比較)
- [公式リソース](#-公式リソース)
- [コミュニティとエコシステム](#-コミュニティとエコシステム)
- [FAQ](#-faq)
- [Star履歴](#-star履歴)
- [コントリビューション](#-コントリビューション)
- [ライセンス](#-ライセンス)

---

## 🌊 Wanモデルについて

**Wan**はAlibabaが開発したオープンソースの動画生成モデルシリーズです。デビューから現在の**VBenchリーダーボード1位**まで、Wanはオープンソース動画AIの限界を押し広げ続けています。

### なぜWanなのか？

- **🏆 VBenchチャンピオン** — Wan 2.1はVBenchで**86.22%**のスコアを達成し、Sora（84.28%）、Luma（83.61%）を含む全モデルを上回る
- **🔓 完全オープンソース** — Sora、Kling、Runwayとは異なり、Wanモデルは完全にオープンソースでHugging Faceからウェイトをダウンロード可能
- **💻 コンシューマーGPU対応** — 1.3Bバージョンは**8.19GB VRAM**のみで動作、RTX 3060一枚で実行可能
- **📊 大規模トレーニングデータ** — **15億本の動画** + **100億枚の画像**で学習
- **🔥 220万以上のダウンロード** — Hugging FaceとModelScopeでグローバルAIコミュニティに検証済み
- **🎬 無検閲オプション** — Wan 2.2 Spicyで無制限のクリエイティブ表現が可能

### モデルファミリーツリー

```
Wan 1.0 (2024 Q3)
  └── Wan 2.1 (2024 Q4) — VBench 1位、14B & 1.3B
       └── Wan 2.2 (2025 Q1) — 品質向上、Spicyバリアント 🌶️
            ├── Wan 2.2 Spicy — NSFW/無検閲生成
            └── Wan 2.5 (2025 Q2) — オーディオ同期、1080p、10秒
                 └── Wan 2.6 (2025 Q3) — マルチショット、15秒、キャラクター安定性
                      └── Wan 2.7 (近日公開！) — 🔜 Atlas Cloudで先行提供
```

### クローズドソースモデルとの主な違い

| 機能 | Wan 2.6 | Sora | Kling | Runway Gen-3 |
|------|---------|------|-------|---------------|
| オープンソース | ✅ | ❌ | ❌ | ❌ |
| ローカルデプロイ | ✅ | ❌ | ❌ | ❌ |
| 最大解像度 | 1920×1080 | 1920×1080 | 1920×1080 | 1920×1080 |
| 最大長さ | 15秒 | 20秒 | 10秒 | 10秒 |
| ネイティブオーディオ | ✅ | ✅ | ❌ | ❌ |
| マルチショット | ✅ | ❌ | ❌ | ❌ |
| NSFWサポート | ✅ (Spicy) | ❌ | ❌ | ❌ |
| 動画あたりの価格 | $0.03から | $0.50以上 | $0.30以上 | $0.50以上 |
| コンシューマーGPU | ✅ (1.3B) | N/A | N/A | N/A |
| ファインチューニング | ✅ LoRA | ❌ | ❌ | ❌ |

---

## 📊 モデル比較

| バージョン | パラメータ | 解像度 | 長さ | オーディオ | マルチショット | オープンソース | NSFW | API価格 |
|-----------|-----------|--------|------|-----------|---------------|---------------|------|---------|
| **Wan 2.6** | 14B | 1080p | 最大15秒 | ✅ | ✅ | ✅ | ❌ | $0.07 |
| **Wan 2.5** | 14B | 1080p | 最大10秒 | ✅ | ❌ | ✅ | ❌ | より安い |
| **Wan 2.2 Spicy** 🌶️ | 14B | 720p | 最大8秒 | ❌ | ❌ | ✅ | ✅ | **$0.03** |
| **Wan 2.2** | 14B / 1.3B | 720p | 最大5秒 | ❌ | ❌ | ✅ | ❌ | — |
| **Wan 2.1** | 14B / 1.3B | 720p | 最大5秒 | ❌ | ❌ | ✅ | ❌ | — |

### Atlas Cloudで利用可能なモデル

| モデル | タイプ | 価格 | ハイライト |
|--------|------|------|-----------|
| Wan 2.6 T2V | テキスト→動画 | $0.07/回（70%オフ） | 5/10/15秒、最大1920×1080、マルチショット、オーディオ |
| Wan 2.6 I2V | 画像→動画 | 利用可能 | 高忠実度画像アニメーション |
| Wan 2.6 I2V Flash | 画像→動画 | より高速で安い | 速度最適化バリアント |
| Wan 2.6 V2V | 動画→動画 | 利用可能 | スタイル変換＆編集 |
| Wan 2.6 画像編集 | 画像編集 | 利用可能 | AI画像編集 |
| Wan 2.6 T2I | テキスト→画像 | 利用可能 | 高品質画像生成 |
| Wan 2.5 T2V | テキスト→動画 | 利用可能 | 安定した動画生成 |
| Wan 2.5 I2V | 画像→動画 | 利用可能 | 安定した画像アニメーション |
| Wan 2.5 Fast | テキスト→動画 | 利用可能 | 速度最適化版 |
| Wan 2.2 Spicy I2V 🌶️ | 画像→動画 | **$0.03/回** | 無検閲生成 |
| Wan 2.2 Spicy I2V LoRA | 画像→動画 | 利用可能 | LoRAファインチューニング対応 |
| Wan 2.2 キャラクタースワップ | 動画エフェクト | 利用可能 | animate-mixフェイススワップ |
| Wan 2.2 画像→アニメーション | アニメーション | 利用可能 | animate-moveモーション転送 |
| Van 2.6 / 2.5 | 最適化版 | 利用可能 | Atlas Cloud最適化バリアント |

> 🎁 **新規ユーザー特典：** 初回チャージで25%ボーナス（最大$100ボーナス）。[今すぐ登録 →](https://www.atlascloud.ai?ref=JPM683)

---

## 🚀 クイックスタート

### オプション1：API（Atlas Cloud）— 最速

<details>
<summary><b>cURL例 — Wan 2.6 テキスト→動画</b></summary>

```bash
# Wan 2.6 テキストから動画生成 API呼び出し
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
<summary><b>cURL例 — Wan 2.2 Spicy（無検閲）</b></summary>

```bash
# Wan 2.2 Spicy 無検閲画像から動画 API呼び出し — わずか$0.03/回
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
<summary><b>Python例 — 完全パイプライン</b></summary>

```python
"""
Wan 動画生成完全サンプル
Wan 2.6 T2V、I2V、Wan 2.2 Spicyをサポート
"""
import requests
import time

# Atlas Cloud API設定
API_KEY = "YOUR_API_KEY"
BASE_URL = "https://api.atlascloud.ai/v1"

def generate_video(prompt: str, model: str = "wan-2.6-t2v", **kwargs) -> str:
    """
    Wanモデルで動画を生成する

    引数:
        prompt: 動画の説明テキスト
        model: モデル名、デフォルトはWan 2.6
        **kwargs: duration、resolutionなどの追加パラメータ
    戻り値:
        動画ダウンロードURL
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

    # 生成タスクを送信
    response = requests.post(f"{BASE_URL}/video/generate", json=payload, headers=headers)
    task_id = response.json()["task_id"]

    # 結果をポーリング
    while True:
        status = requests.get(f"{BASE_URL}/video/status/{task_id}", headers=headers)
        result = status.json()

        if result["status"] == "completed":
            return result["video_url"]
        elif result["status"] == "failed":
            raise Exception(f"生成失敗: {result.get('error', '不明なエラー')}")

        time.sleep(2)  # 2秒ごとにステータス確認

# ====== 使用例 ======

# 例1: Wan 2.6 テキストから動画（マルチショット+オーディオ対応）
video_url = generate_video(
    prompt="A chef preparing sushi in a traditional Japanese kitchen, warm lighting, close-up shots",
    model="wan-2.6-t2v",
    duration=10,
    resolution="1920x1080",
    audio=True
)
print(f"動画生成完了: {video_url}")

# 例2: Wan 2.2 Spicy 無検閲生成（わずか$0.03）
spicy_url = generate_video(
    prompt="Artistic figure study, classical painting style, natural movement",
    model="alibaba/wan-2.2-spicy/image-to-video"
)
print(f"Spicy動画生成完了: {spicy_url}")
```

</details>

### オプション2：ローカルデプロイ（ComfyUI）

```bash
# 1. ComfyUIをインストール
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 2. 依存関係をインストール
pip install -r requirements.txt

# 3. Wan 2.6モデルウェイトをダウンロード
# Hugging Faceからダウンロード（約28GBのディスク容量が必要）
huggingface-cli download Wan-AI/Wan2.6-T2V-14B --local-dir models/wan2.6/

# 4. Wan ComfyUIノードをインストール
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
pip install -r ComfyUI-Wan/requirements.txt

# 5. ComfyUIを起動
cd ..
python main.py --listen 0.0.0.0 --port 8188
```

### オプション3：Hugging Face Pipeline

```python
"""
Hugging Face Diffusersライブラリを使用してWan 2.1をローカルで実行
NVIDIA GPU搭載環境向け
"""
from diffusers import WanPipeline
import torch

# モデルをロード（1.3Bバージョンは8.19GB VRAMのみ必要）
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16  # FP16を使用してVRAMを節約
)
pipe = pipe.to("cuda")

# 動画を生成
video = pipe(
    prompt="A golden retriever playing in autumn leaves, slow motion, warm sunlight",
    num_frames=81,        # 約5秒の動画
    height=480,
    width=720,
    guidance_scale=7.5
).frames[0]

# 動画を保存
from diffusers.utils import export_to_video
export_to_video(video, "output.mp4", fps=16)
print("動画をoutput.mp4に保存しました")
```

### オプション4：Dockerデプロイ

```dockerfile
# Wan 2.6 Dockerデプロイ設定
FROM nvidia/cuda:12.1-runtime-ubuntu22.04

# システム依存関係をインストール
RUN apt-get update && apt-get install -y \
    python3 python3-pip git wget \
    && rm -rf /var/lib/apt/lists/*

# Python依存関係をインストール
RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu121
RUN pip3 install diffusers transformers accelerate safetensors

# Wanモデルをダウンロード
RUN huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B --local-dir /models/wan

# 推論スクリプトをコピー
COPY inference.py /app/inference.py

WORKDIR /app
CMD ["python3", "inference.py"]
```

```bash
# Dockerコンテナをビルドして実行
docker build -t wan-video .
docker run --gpus all -p 8080:8080 wan-video
```

---

## 🎨 プロンプトコレクション

> 30以上の厳選プロンプト、Wanモデルに最適化済み。各プロンプトに完全なテキスト、推奨モデル、設定、ティップスを含む。

### 🎬 シネマティック＆映画

<details>
<summary><b>1. 壮大な山岳風景</b></summary>

- **プロンプト：** `Sweeping aerial shot over snow-capped mountains at golden hour, dramatic clouds casting long shadows across alpine valleys, a winding river reflecting the amber sky, cinematic camera movement slowly pushing forward, volumetric lighting, 8K film grain`
- **モデル：** Wan 2.6 T2V
- **長さ：** 15秒
- **解像度：** 1920×1080
- **ティップス：** マルチショットを有効にするとよりダイナミックなシーケンスに。オーディオを追加すると環境音（風の音）が付きます。

</details>

<details>
<summary><b>2. 都市のナイトチェイス</b></summary>

- **プロンプト：** `Tracking shot through neon-lit Tokyo streets at night, rain-soaked asphalt reflecting pink and blue neon signs, a figure in a dark coat running through crowds, handheld camera shake, Blade Runner aesthetic, moody atmosphere, cinematic color grading`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** ネガティブプロンプト"blurry, low quality, static"を使用するとよりシャープな動きに。

</details>

<details>
<summary><b>3. 歴史的バトルシーン</b></summary>

- **プロンプト：** `Wide establishing shot of a medieval battlefield at dawn, thousands of soldiers in formation, banners waving in the wind, mist rolling across the field, dramatic orchestral music feel, Lord of the Rings inspired cinematography, epic scale, film grain`
- **モデル：** Wan 2.6 T2V
- **長さ：** 15秒
- **解像度：** 1920×1080
- **ティップス：** マルチショットモードはこのシーンで特に優れており、ワイドとクローズアップのカット切り替えが可能。

</details>

<details>
<summary><b>4. 水中ドキュメンタリー</b></summary>

- **プロンプト：** `Slow underwater tracking shot through a vibrant coral reef, tropical fish swimming in formation, sunbeams penetrating the crystal-clear blue water, a sea turtle gliding gracefully through the frame, National Geographic style, 4K clarity`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** "smooth camera movement, steady"を追加して水中のブレ artifacts を回避。

</details>

<details>
<summary><b>5. フィルム・ノワール探偵</b></summary>

- **プロンプト：** `Close-up of a detective in a dimly lit office, cigarette smoke curling through a single shaft of light from venetian blinds, black and white film noir style, slow camera dolly in, dramatic shadows, 1940s aesthetic, grain texture`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1280×720
- **ティップス：** "black and white, monochrome"を明示的に指定すると一貫したノワールルックに。

</details>

### 🌶️ NSFW / クリエイティブフリーダム（Wan 2.2 Spicy）

<details>
<summary><b>6. 古典的人体研究</b></summary>

- **プロンプト：** `Renaissance-style figure study, soft diffused lighting on skin, classical painting composition, marble sculpture coming to life with subtle breathing movement, warm golden tones, museum gallery setting, artistic and elegant`
- **モデル：** Wan 2.2 Spicy I2V
- **価格：** $0.03/回
- **ティップス：** 古典画作や彫刻の参考画像と組み合わせると最高の結果に。

</details>

<details>
<summary><b>7. アバンギャルドファッション</b></summary>

- **プロンプト：** `High fashion editorial, model in sheer flowing fabric, dramatic wind effect, stark white studio lighting, Helmut Newton inspired, bold poses transitioning fluidly, haute couture, magazine quality`
- **モデル：** Wan 2.2 Spicy I2V
- **価格：** $0.03/回
- **ティップス：** LoRAバリアントを使用すると複数の生成で一貫したスタイルを維持。

</details>

<details>
<summary><b>8. アーティスティックボディムーブメント</b></summary>

- **プロンプト：** `Contemporary dance performance, fluid body movement, dramatic stage lighting, dancer's silhouette against colored backdrop, artistic expression through motion, modern ballet, intimate camera angles, professional choreography`
- **モデル：** Wan 2.2 Spicy I2V
- **価格：** $0.03/回
- **ティップス：** 画像→動画モードが最適 — ダンサーの参考画像を提供してください。

</details>

<details>
<summary><b>9. 神話シーン</b></summary>

- **プロンプト：** `Birth of Venus reimagined, goddess emerging from ocean waves, flowing golden hair, seashells and foam, Pre-Raphaelite painting style, ethereal glow, mythological beauty, Botticelli inspired but cinematic`
- **モデル：** Wan 2.2 Spicy I2V
- **価格：** $0.03/回
- **ティップス：** 古典美術の参考画像との相性が抜群。

</details>

<details>
<summary><b>10. サイバーパンクキャラクター</b></summary>

- **プロンプト：** `Cyberpunk character in revealing neon-lit outfit, holographic tattoos glowing on skin, futuristic nightclub setting, pulsing LED lights, confident walking motion, sci-fi fashion, Blade Runner 2049 aesthetic`
- **モデル：** Wan 2.2 Spicy I2V LoRA
- **価格：** $0.03/回
- **ティップス：** LoRAを使用すると異なるシーンでキャラクターの外観を一貫して維持。

</details>

### 📦 プロダクト＆コマーシャル

<details>
<summary><b>11. 高級腕時計ショーケース</b></summary>

- **プロンプト：** `Macro close-up of a luxury watch rotating on a black velvet surface, golden light reflections dancing on polished metal, mechanical movement visible through transparent caseback, premium product photography, smooth 360-degree rotation`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** ゆっくりとしたコントロールされた回転が最適。"studio lighting, product photography"を追加してコマーシャル品質に。

</details>

<details>
<summary><b>12. フードCM — コーヒー注ぎ</b></summary>

- **プロンプト：** `Slow motion pour of steaming espresso into a white ceramic cup, rich crema forming on surface, steam rising in soft morning light, rustic wooden table, out-of-focus bakery background, food photography, warm color palette, 120fps slow motion feel`
- **モデル：** Wan 2.6 T2V
- **長さ：** 5秒
- **解像度：** 1920×1080
- **ティップス：** 短い長さで高いディテールがフードコンテンツに最適。

</details>

<details>
<summary><b>13. スニーカー製品発表</b></summary>

- **プロンプト：** `Dynamic sneaker reveal, shoe floating and rotating in mid-air against gradient background, particles and light streaks surrounding the product, dramatic lighting transitions, Nike commercial style, clean product visualization`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** マルチショットで同じ製品を異なる角度から撮影。

</details>

<details>
<summary><b>14. 香水CM — エーテリアル</b></summary>

- **プロンプト：** `Glass perfume bottle on a reflective surface, golden liquid catching light, slow motion flower petals falling around it, soft bokeh background, luxury brand commercial aesthetic, Chanel No.5 inspired visual, elegant and sophisticated`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** "glass reflections, caustics, luxury"を追加してプレミアム感を演出。

</details>

<details>
<summary><b>15. テック製品アンボクシング</b></summary>

- **プロンプト：** `Cinematic unboxing of a sleek smartphone, hands slowly lifting the lid of a minimalist white box, device rising with a subtle glow, holographic interface appearing above the screen, Apple keynote style presentation, clean and modern`
- **モデル：** Wan 2.6 I2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** I2Vモードで実際の製品画像を使用するとブランドの正確性が向上。

</details>

### 🎨 アニメーション＆カートゥーン

<details>
<summary><b>16. アニメ桜シーン</b></summary>

- **プロンプト：** `Anime style, a young girl standing under a blooming cherry blossom tree, pink petals falling in slow motion, gentle breeze moving her hair and school uniform, soft watercolor background, Studio Ghibli aesthetic, warm spring lighting`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1280×720
- **ティップス：** "anime, cel-shaded, 2D animation"を追加すると一貫したアニメスタイルに。

</details>

<details>
<summary><b>17. ピクセルアートアドベンチャー</b></summary>

- **プロンプト：** `Retro pixel art game scene, 16-bit hero character walking through a mystical forest, glowing mushrooms, floating fireflies, parallax scrolling background layers, SNES-era RPG aesthetic, vibrant pixel colors`
- **モデル：** Wan 2.5 T2V
- **長さ：** 5秒
- **解像度：** 1280×720
- **ティップス：** 低い解像度がレトロピクセルアート感を向上させます。

</details>

<details>
<summary><b>18. 3Dカートゥーンキャラクター</b></summary>

- **プロンプト：** `Pixar-style 3D animated character, a small robot with big expressive eyes discovering a flower in a post-apocalyptic landscape, WALL-E inspired, smooth character animation, subsurface scattering on plastic materials, Pixar render quality`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** Wan 2.6は3Dアニメーションスタイルの処理が非常に優れています。

</details>

<details>
<summary><b>19. コミックブックアクション</b></summary>

- **プロンプト：** `Marvel comic book style action sequence, superhero landing pose with impact shockwave, bold ink outlines, halftone dot shading, dynamic camera angle from below, speech bubble appearing, vibrant primary colors, Jack Kirby inspired`
- **モデル：** Wan 2.6 T2V
- **長さ：** 5秒
- **解像度：** 1280×720
- **ティップス：** 短くパワフルなアクションがコミックスタイルに最適。

</details>

<details>
<summary><b>20. 水彩絵本</b></summary>

- **プロンプト：** `Watercolor illustration coming to life, a fox and rabbit having a tea party in an enchanted forest clearing, soft paint bleeding effects, storybook page turning animation, children's book illustration style, gentle pastel colors, whimsical`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1280×720
- **ティップス：** "watercolor, illustration, painted"キーワードがアーティスティックスタイルの維持に役立ちます。

</details>

### 🔄 キャラクタースワップ（Wan 2.2 animate-mix）

<details>
<summary><b>21. セレブリティインプレッション</b></summary>

- **プロンプト：** `Professional business presentation, confident speaker at a podium, formal attire, corporate event, smooth gestures and natural speech patterns`
- **モデル：** Wan 2.2 キャラクタースワップ（animate-mix）
- **ティップス：** プレゼンテーションのソース動画とターゲットの顔画像をアップロード。正面向きで照明の良い顔が最適。

</details>

<details>
<summary><b>22. 歴史人物の復活</b></summary>

- **プロンプト：** `Historical documentary narration, period-appropriate setting, speaking directly to camera, educational content`
- **モデル：** Wan 2.2 キャラクタースワップ（animate-mix）
- **ティップス：** 鮮明で高解像度の参考写真で最良の結果に。ソースとターゲット間の照明を一貫させてください。

</details>

<details>
<summary><b>23. ミュージックビデオフェイススワップ</b></summary>

- **プロンプト：** `Music performance, singer on stage, dynamic lighting, emotional expression, concert atmosphere`
- **モデル：** Wan 2.2 キャラクタースワップ（animate-mix）
- **ティップス：** 顔のトラッキングが安定しているミュージックビデオに最適。極端な頭の回転は避けてください。

</details>

### 🏃 モーション転送（Wan 2.2 animate-move）

<details>
<summary><b>24. ダンス振り付け転送</b></summary>

- **プロンプト：** `Professional dance routine, hip-hop choreography, studio setting, full body visible, clean background`
- **モデル：** Wan 2.2 画像→アニメーション（animate-move）
- **ティップス：** ダンス動画をモーションソースとして、キャラクター画像をアップロード。クリーンな背景の全身ショットが最適。

</details>

<details>
<summary><b>25. カートゥーンキャラクターアニメーション</b></summary>

- **プロンプト：** `Animated character performing complex movements, cartoon style, expressive body language`
- **モデル：** Wan 2.2 画像→アニメーション（animate-move）
- **ティップス：** 実際の人物のモーション動画を使用して、2Dまたは3Dキャラクター画像をアニメーション化。

</details>

<details>
<summary><b>26. ブランドマスコットアニメーション</b></summary>

- **プロンプト：** `Brand mascot performing fun actions, waving, jumping, dancing, engaging personality`
- **モデル：** Wan 2.2 画像→アニメーション（animate-move）
- **ティップス：** 静的なブランドマスコットに自然な動きを与えるのに最適。

</details>

### 🌐 その他＆アドバンスト

<details>
<summary><b>27. タイムラプスシティ</b></summary>

- **プロンプト：** `Hyper-lapse of a modern city skyline from day to night, clouds racing across the sky, lights gradually turning on in skyscrapers, traffic becoming streams of light, star trails appearing, 24-hour cycle compressed into seconds, urban time-lapse`
- **モデル：** Wan 2.6 T2V
- **長さ：** 15秒
- **解像度：** 1920×1080
- **ティップス：** 15秒の長さは昼夜のトランジションに最適。

</details>

<details>
<summary><b>28. 自然マクロ — 蝶の羽化</b></summary>

- **プロンプト：** `Extreme macro shot of a monarch butterfly emerging from chrysalis, iridescent wing scales unfolding in slow motion, morning dew drops on wings, shallow depth of field, nature documentary quality, BBC Earth style`
- **モデル：** Wan 2.6 T2V
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** ゆっくりとした精密な動きのマクロ被写体が素晴らしい結果を生みます。

</details>

<details>
<summary><b>29. SFスペースステーション</b></summary>

- **プロンプト：** `Exterior shot of a massive space station orbiting Earth, ISS-inspired design but futuristic, solar panels rotating to track the sun, a shuttle approaching for docking, Earth's blue glow illuminating the structure, Interstellar cinematography`
- **モデル：** Wan 2.6 T2V
- **長さ：** 15秒
- **解像度：** 1920×1080
- **ティップス：** オーディオを追加して没入感のある宇宙の雰囲気に。マルチショットで内部/外部の切り替え。

</details>

<details>
<summary><b>30. 抽象フルイドアート</b></summary>

- **プロンプト：** `Abstract fluid art in motion, vibrant acrylic paint pouring and mixing, golden veins forming between color pools, Kandinsky meets Jackson Pollock, mesmerizing organic patterns, satisfying ASMR-like visual, overhead camera view`
- **モデル：** Wan 2.5 T2V
- **長さ：** 10秒
- **解像度：** 1280×720
- **ティップス：** 抽象コンテンツはエラー許容度が高く、常に美しい結果を生成します。

</details>

<details>
<summary><b>31. Wan 2.6 R2V — キャラクターリファレンス</b></summary>

- **プロンプト：** `キャラクターのリファレンス動画をアップロード（外観+声をキャプチャ）し、新しいシーンで生成：未来都市を歩く、ホログラフィックディスプレイとインタラクト、外観と声の特徴を完全に維持`
- **モデル：** Wan 2.6 R2V（リファレンスから動画）
- **長さ：** 10秒
- **解像度：** 1920×1080
- **ティップス：** Wan 2.6 R2Vはリファレンス動画からキャラクターのアイデンティティ（外観+声）を維持。3-5秒のリファレンスクリップで最良の結果に。

</details>

<details>
<summary><b>32. マルチショットナラティブ</b></summary>

- **プロンプト：** `Shot 1: Wide establishing shot of a cozy café on a rainy Parisian street. Shot 2: Close-up of hands wrapping around a steaming coffee cup. Shot 3: Looking out the window as rain streams down the glass. Shot 4: Slow zoom out revealing the full café scene with warm interior lighting.`
- **モデル：** Wan 2.6 T2V（マルチショット）
- **長さ：** 15秒
- **解像度：** 1920×1080
- **ティップス：** "Shot N:"プレフィックスでシーンを分けてマルチショット機能を使用。Wan 2.6がショット間のスムーズなトランジションを作成。

</details>

---

## 🖥️ ローカルデプロイガイド

### ハードウェア要件

| コンポーネント | Wan 2.6 (14B) | Wan 2.1 (14B) | Wan 2.1 (1.3B) |
|------------|---------------|---------------|-----------------|
| **GPU VRAM** | 24GB以上 | 24GB以上 | **8.19GB** |
| **推奨GPU** | RTX 4090 / A100 | RTX 4090 / A100 | RTX 3060 12GB |
| **システムRAM** | 32GB以上 | 32GB以上 | 16GB |
| **ディスク容量** | 約56GB | 約28GB | 約5GB |
| **OS** | Linux / Windows | Linux / Windows | Linux / Windows |
| **CUDA** | 12.1以上 | 11.8以上 | 11.8以上 |

### ComfyUIセットアップ（ステップバイステップ）

```bash
# ======== ステップ1：ComfyUIをインストール ========
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI

# 仮想環境を作成（推奨）
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# PyTorchをインストール（CUDA 12.1）
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# ComfyUIの依存関係をインストール
pip install -r requirements.txt

# ======== ステップ2：Wanノードをインストール ========
cd custom_nodes
git clone https://github.com/Wan-Video/ComfyUI-Wan.git
cd ComfyUI-Wan
pip install -r requirements.txt
cd ../..

# ======== ステップ3：モデルをダウンロード ========
# オプションA：フル14Bモデル（推奨、ただし24GB以上のVRAMが必要）
huggingface-cli download Wan-AI/Wan2.6-T2V-14B \
    --local-dir models/wan2.6-14b/

# オプションB：軽量1.3Bモデル（8.19GB VRAMのみ必要）
huggingface-cli download Wan-AI/Wan2.1-T2V-1.3B \
    --local-dir models/wan2.1-1.3b/

# ======== ステップ4：ComfyUIを起動 ========
python main.py --listen 0.0.0.0 --port 8188

# ブラウザで http://localhost:8188 を開く
# Wanワークフローノードをインポートして使用
```

### VRAMメモリ最適化ティップス

```python
"""
VRAM最適化テクニック、コンシューマーGPUでWanモデルを実行するのに役立つ
"""
import torch
from diffusers import WanPipeline

# テクニック1: 半精度浮動小数点を使用（約50%のVRAMを節約）
pipe = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-14B",
    torch_dtype=torch.float16
)

# テクニック2: アテンションスライシングを有効化（VRAMピーク値を大幅に削減）
pipe.enable_attention_slicing(slice_size="auto")

# テクニック3: VAEスライシングを有効化（段階的に動画フレームをデコード）
pipe.enable_vae_slicing()

# テクニック4: CPUオフロードを有効化（非アクティブモジュールを自動的にCPUに移動）
pipe.enable_model_cpu_offload()

# テクニック5: xformersで高速化（xformersの追加インストールが必要）
# pip install xformers
pipe.enable_xformers_memory_efficient_attention()

# テクニック6: 解像度とフレーム数を下げる
video = pipe(
    prompt="Your prompt here",
    num_frames=49,       # フレーム数を減らす（49フレーム ≈ 3秒）
    height=480,          # 解像度を下げる
    width=720,
    guidance_scale=7.5
).frames[0]

# テクニック7: 14Bの代わりに1.3Bモデルを使用
# 1.3Bモデルは8.19GB VRAMのみで、品質も優れている
pipe_light = WanPipeline.from_pretrained(
    "Wan-AI/Wan2.1-T2V-1.3B",
    torch_dtype=torch.float16
).to("cuda")
```

---

## ✍️ プロンプトエンジニアリング

### Wan専用の効果的なキーワード

| カテゴリ | 効果的なキーワード |
|---------|-------------------|
| **画質** | `8K, cinematic, film grain, high detail, professional, masterpiece` |
| **カメラ** | `tracking shot, dolly zoom, aerial shot, close-up, macro, wide angle` |
| **ライティング** | `golden hour, volumetric lighting, rim lighting, neon glow, soft diffused` |
| **モーション** | `slow motion, time-lapse, smooth pan, gentle movement, dynamic action` |
| **スタイル** | `photorealistic, anime, watercolor, oil painting, cyberpunk, noir` |
| **ムード** | `dramatic, ethereal, cozy, epic, melancholic, whimsical` |

### ネガティブプロンプト戦略

```
# 推奨汎用ネガティブプロンプト
blurry, low quality, distorted, deformed, ugly, bad anatomy,
watermark, text overlay, logo, pixelated, noise, artifacts,
oversaturated, underexposed, static image, no movement,
extra fingers, missing limbs, unnatural proportions
```

### マルチショットテクニック（Wan 2.6）

```
# マルチショットナラティブテンプレート
Shot 1: [ワイド/確立ショット] - 環境とコンテキストでシーンを設定
Shot 2: [ミディアム] - 被写体またはキャラクターを紹介
Shot 3: [クローズアップ] - 感情的なディテールまたはキーアクション
Shot 4: [ワイド/プルバック] - 解決またはリビール

# 例：コーヒー広告マルチショット
Shot 1: 日の出時のコロンビアコーヒー農園の空撮、朝霧。
Shot 2: 熟したコーヒーチェリーを摘む農家の手。
Shot 3: 焙煎されるコーヒー豆の極端なクローズアップ、オイルが輝く。
Shot 4: モダンなカフェでの淹れたてコーヒーから立ち昇る湯気。
```

### オーディオ生成コントロール（Wan 2.6）

Wan 2.6はネイティブオーディオ同期をサポート。ベストプラクティス：

- **環境音**は視覚コンテンツに基づいて自動生成
- プロンプトにオーディオ手がかりを追加：`"birds chirping"`、`"rain on window"`、`"crowd cheering"`
- より長い長さ（10-15秒）でオーディオ品質が向上
- API呼び出しで`audio: true`を使用してオーディオ生成を有効化

### 解像度 vs 速度のトレードオフ

| 解像度 | VRAM使用量 | 生成時間 | 最適用途 |
|--------|-----------|---------|---------|
| 1920×1080 | 約24GB | 約3-5分 | 最終プロダクション |
| 1280×720 | 約16GB | 約1-3分 | ドラフト＆テスト |
| 854×480 | 約10GB | 約30-60秒 | ラピッドプロトタイピング |
| 640×360 | 約8GB | 約15-30秒 | クイックプレビュー |

---

## 💰 API料金比較

| プロバイダー | Wan 2.6 T2V | Wan 2.5 T2V | Wan Spicy 🌶️ | 主な機能 |
|------------|-------------|-------------|---------------|---------|
| **Atlas Cloud** ⭐ | **$0.07/回**（70%オフ） | より安い | **$0.03/回** | ✅ 全モデル、NSFW、LoRA、V2V、マルチショット |
| Alibaba Cloud | $0.10以上 | $0.08以上 | N/A | ⚠️ リージョン制限、NSFWなし |
| Replicate | $0.15以上 | $0.12以上 | 限定 | 基本APIのみ |
| セルフホスト | GPU時間コスト | GPU時間コスト | GPU時間コスト | ✅ 完全制御、❌ メンテナンス負担 |

### コスト分析例

| ユースケース | モデル | 月間生成数 | Atlas Cloudコスト | セルフホスト（A100） |
|------------|------|----------|-----------------|---------------------|
| SNSクリエイター | Wan 2.6 T2V | 500本 | **$35/月** | 約$500/月 |
| NSFWアートクリエイター | Wan Spicy | 1,000本 | **$30/月** | 約$500/月 |
| コマーシャル制作 | Wan 2.6 T2V | 100本 | **$7/月** | 約$500/月 |
| ホビイスト | Wan 2.5 T2V | 50本 | **$5未満/月** | 約$500/月 |

> 💡 **プロのティップス：** [Atlas Cloudに登録](https://www.atlascloud.ai?ref=JPM683)すると初回チャージで**25%ボーナス**（最大$100ボーナス）。$100+$25ボーナスで最大1,785本のWan Spicy動画またはWan 2.6動画を生成！

### Atlas Cloud vs fal.ai 料金比較

| モデル | fal.ai 料金 | Atlas Cloud 料金 | 節約額 |
|:------|:------------|:-----------------|:---------|
| **Kling** | $0.224/秒 (5秒 = $1.12) | $0.204/回 | **82%安い** |
| **Seedance** | ~$0.26/動画 | $0.222/回 | **15%安い** |
| **Wan 2.5** | $0.05/秒 (5秒 = $0.25) | $0.05/回 | **80%安い** |
| **Wan 2.6** | 同等の価格 | $0.07/回 | 競争力あり |
| **Veo 3** | $0.40/秒 (8秒 = $3.20) | TBD | 近日公開 |
| **Vidu Q3-Pro** | — | $0.06/回 | Atlas限定 |
| **Vidu Q3-Turbo** | — | $0.034/回 | Atlas限定 |

> 💡 Atlas Cloudは全ての主要動画モデルで**最安値**を提供しています。fal.aiから乗り換えて、動画生成コストを最大**82%**節約しましょう。

---

## 📚 公式リソース

### モデルウェイト＆ダウンロード

| リソース | リンク | 備考 |
|---------|------|------|
| Hugging Face — Wan-AI | [huggingface.co/Wan-AI](https://huggingface.co/Wan-AI) | 全モデルウェイト |
| ModelScope — Wan | [modelscope.cn/Wan-Video](https://modelscope.cn/organization/Wan-Video) | 代替ダウンロード（アジアから高速） |
| Wan 2.6 T2V 14B | [HFリンク](https://huggingface.co/Wan-AI/Wan2.6-T2V-14B) | 最新テキスト→動画 |
| Wan 2.6 I2V 14B | [HFリンク](https://huggingface.co/Wan-AI/Wan2.6-I2V-14B) | 最新画像→動画 |
| Wan 2.1 T2V 1.3B | [HFリンク](https://huggingface.co/Wan-AI/Wan2.1-T2V-1.3B) | 軽量版、コンシューマーGPU |

### 論文＆リサーチ

| 論文 | リンク | 説明 |
|------|------|------|
| Wan 2.1技術レポート | [arXiv](https://arxiv.org/abs/2503.20314) | アーキテクチャ＆トレーニング詳細 |
| VBenchリーダーボード | [vbench.org](https://vbench.org) | ベンチマークランキング |

### 公式GitHubリポジトリ

| リポジトリ | 説明 |
|-----------|------|
| [Wan-Video/Wan2.6](https://github.com/Wan-Video/Wan2.6) | Wan 2.6公式コード |
| [Wan-Video/Wan2.1](https://github.com/Wan-Video/Wan2.1) | Wan 2.1公式コード |

---

## 🌐 コミュニティとエコシステム

### ComfyUI拡張

| 拡張 | 説明 | スター |
|------|------|------|
| [ComfyUI-Wan](https://github.com/Wan-Video/ComfyUI-Wan) | 公式Wan ComfyUIノード | ⭐ |
| [ComfyUI-WanVideoWrapper](https://github.com/kijai/ComfyUI-WanVideoWrapper) | コミュニティラッパー（追加機能付き） | ⭐ |

### LoRAモデル＆ファインチューニング

| リソース | 説明 |
|---------|------|
| [Civitai — Wan LoRAs](https://civitai.com/models?tags=wan) | コミュニティトレーニング済みLoRAモデル |
| [Wan LoRAトレーニングガイド](https://github.com/Wan-Video/Wan2.1/blob/main/docs/lora.md) | 公式ファインチューニングドキュメント |

### コミュニティハブ

| プラットフォーム | リンク |
|---------------|------|
| Reddit — r/WanVideo | [reddit.com/r/WanVideo](https://reddit.com/r/WanVideo) |
| Discord — Wanコミュニティ | コミュニティDiscordサーバー |
| Twitter/X — #WanVideo | [#WanVideoを検索](https://twitter.com/search?q=%23WanVideo) |

### チュートリアル＆ガイド

| タイトル | タイプ | リンク |
|---------|------|------|
| Wan 2.6完全ガイド | 動画 | YouTube |
| ComfyUI + Wanワークフロー | 記事 | ブログ |
| Wan LoRAトレーニングチュートリアル | 動画 | YouTube |
| Wan vs Kling vs Sora比較 | 記事 | ブログ |

---

## ❓ FAQ

<details>
<summary><b>Wan AI動画モデルとは何ですか？</b></summary>

WanはAlibabaのオープンソース動画生成モデルシリーズです。拡散Transformerアーキテクチャを使用し、15億本の動画と100億枚の画像で学習しています。Wan 2.1モデルは**VBenchリーダーボードで1位**を達成し、スコアは86.22%で、Sora（84.28%）とLuma（83.61%）を上回りました。最新版は**Wan 2.6**で、ネイティブオーディオ同期付きの最大15秒のマルチショット1080p動画生成をサポートしています。

</details>

<details>
<summary><b>Wanをローカルで実行するには？</b></summary>

以下の方法でWanをローカル実行できます：
1. **ComfyUI** — Wan ComfyUIノードをインストールしてモデルウェイトをダウンロード
2. **Hugging Face Diffusers** — Pythonで`WanPipeline`クラスを使用
3. **Docker** — 提供されているDockerfileでデプロイ

**1.3Bモデルは8.19GB VRAMのみ**で動作し、RTX 3060のようなコンシューマーGPUでアクセス可能です。14Bモデルは24GB以上のVRAM（RTX 4090またはA100）が必要です。

詳しい手順は[ローカルデプロイガイド](#-ローカルデプロイガイド)をご覧ください。

</details>

<details>
<summary><b>Wan vs Seedance vs Kling — どれが優れていますか？</b></summary>

| 機能 | Wan 2.6 | Seedance | Kling |
|------|---------|----------|-------|
| オープンソース | ✅ | ❌ | ❌ |
| 最大長さ | 15秒 | 10秒 | 10秒 |
| オーディオ | ✅ | ❌ | ❌ |
| マルチショット | ✅ | ❌ | ❌ |
| NSFW | ✅ (Spicy) | ❌ | ❌ |
| ローカルデプロイ | ✅ | ❌ | ❌ |
| API価格 | $0.03から | $0.20以上 | $0.30以上 |

**Wanの優位点：** オープンソースの柔軟性、価格、NSFWサポート、ローカルデプロイ、機能の豊富さ。SeedanceやKlingは特定のユースケースでモーション品質が異なる場合がありますが、Wanのオープンソース性と迅速な進化により、長期的な最良の選択です。

</details>

<details>
<summary><b>Wan 2.6に最適なGPUは？</b></summary>

| GPU | VRAM | 実行可能 | パフォーマンス |
|-----|------|---------|-------------|
| RTX 3060 12GB | 12GB | ✅（1.3Bのみ） | ベーシック |
| RTX 3090 | 24GB | ✅（14B最適化付き） | 良好 |
| RTX 4090 | 24GB | ✅（14Bフルスピード） | 優秀 |
| A100 40GB | 40GB | ✅（全モデル、バッチ） | プロフェッショナル |
| A100 80GB | 80GB | ✅（全モデル、高バッチ） | エンタープライズ |

**予算の推奨：** ローカルデプロイにはRTX 4090、またはハードウェアに投資したくない場合は[Atlas Cloud API](https://www.atlascloud.ai?ref=JPM683)を$0.03/動画から利用。

</details>

<details>
<summary><b>無検閲のWanモデルはありますか？</b></summary>

**はい！** **Wan 2.2 Spicy** 🌶️は無検閲/NSFWバリアントで、無制限のクリエイティブコンテンツ生成が可能です。以下から利用できます：

- **Atlas Cloud API** わずか**$0.03/回** — 市場で最も安い無検閲動画生成API
- モデル：`alibaba/wan-2.2-spicy/image-to-video`と`alibaba/wan-2.2-spicy/image-to-video-lora`（LoRAサポート付き）

[Atlas CloudでWan 2.2 Spicyを試す →](https://www.atlascloud.ai?ref=JPM683)

</details>

<details>
<summary><b>API経由のWan動画生成のコストは？</b></summary>

Atlas Cloudは最もリーズナブルなWan API価格を提供：
- **Wan 2.2 Spicy（NSFW）：** $0.03/回
- **Wan 2.6 T2V（1080p、15秒）：** $0.07/回（70%割引）
- **Wan 2.5バリアント：** さらに低価格
- 初回チャージで**25%ボーナス**（最大$100）

Sora（$0.50以上/動画）やRunway（$0.50以上/動画）と比較してください。[始める →](https://www.atlascloud.ai?ref=JPM683)

</details>

<details>
<summary><b>Wan 2.6 R2Vとは？</b></summary>

**Wan 2.6 R2V（リファレンスから動画）** はユニークな機能で、キャラクターのリファレンス動画をアップロードして、その人物の**外観と声**の両方をキャプチャできます。モデルは同じキャラクターが新しいシーンに登場する動画を生成し、アイデンティティの一貫性を維持します。バーチャルアバター、パーソナライズコンテンツ、キャラクター主導のナラティブの作成に最適です。

</details>

<details>
<summary><b>Wan 2.7はいつリリースされますか？</b></summary>

**Wan 2.7**は現在開発中で、近日公開予定です。Atlas CloudはWan 2.7をAPIで提供する最初のプラットフォームの1つになります。[Atlas Cloudに登録](https://www.atlascloud.ai?ref=JPM683)して、Wan 2.7ローンチ時に通知を受け取りましょう。

</details>

---

## 🌊 Wanモデルでクリエイション開始

<div align="center">

**Wan Spicy $0.03/動画からWan 2.6 $0.07まで — 最もリーズナブルなAI動画生成API。**

| | |
|---|---|
| ✅ **無検閲** | Wan 2.2 Spicyで無制限のクリエイティビティ |
| ✅ **オープンソース** | ローカル実行またはAPI利用 |
| ✅ **Wan 2.7近日公開** | Atlas Cloudで先行アクセス |
| ✅ **25%ボーナス** | 初回チャージ時（最大$100ボーナス） |
| ✅ **全モデル対応** | T2V、I2V、V2V、画像編集、キャラスワップ、アニメーション |

<br />

[![Atlas CloudでWanを試す](https://img.shields.io/badge/👉%20Atlas%20Cloudで%20Wanを試す-blue?style=for-the-badge&logo=cloud&logoColor=white)](https://www.atlascloud.ai?ref=JPM683)

*GPUもセットアップも不要。プロンプトを入力するだけで動画が完成。*

</div>

---

## ⭐ Star履歴

<div align="center">

このリソースが役に立ったら、ぜひStarをお願いします！他の人がWanエコシステムを発見する手助けになります。

[![Star History Chart](https://api.star-history.com/svg?repos=your-org/awesome-wan-video&type=Date)](https://star-history.com/#your-org/awesome-wan-video&Date)

</div>

---

## 🤝 コントリビューション

コントリビューション歓迎！PRを提出する前に[コントリビューションガイドライン](CONTRIBUTING.md)をお読みください。

### コントリビューション方法

1. このリポジトリをFork
2. フィーチャーブランチを作成：`git checkout -b add-new-resource`
3. 適切なセクションにリソースを追加
4. 変更をコミット：`git commit -m 'Add new resource'`
5. ブランチにプッシュ：`git push origin add-new-resource`
6. Pull Requestを提出

### 求めているもの

- 新しいWanモデルツール、拡張、統合
- コミュニティチュートリアルとガイド
- LoRAモデルとファインチューニングリソース
- サンプル出力付きプロンプト例
- ベンチマーク結果と比較
- 他の言語への翻訳

---

## 📄 ライセンス

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

本プロジェクトは[MITライセンス](LICENSE)で提供されています。

---

<div align="center">

**🌊 Wan — AI動画生成をすべての人にオープンでアクセシブルに 🌊**

オープンソースコミュニティが ❤️ を込めて制作

[⬆ トップに戻る](#-awesome-wan-動画生成)

</div>
