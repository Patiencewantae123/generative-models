# Generative Models by Stability AI
![sample1](assets/000.jpg)

## 🗞️ News

### **July 24, 2024**
- 🚀 **[Stable Video 4D (SV4D)](https://huggingface.co/stabilityai/sv4d)**: A video-to-4D diffusion model for novel-view video synthesis.
  - **Quickstart**: Run `python scripts/sampling/simple_video_sample_4d.py --input_path assets/sv4d_videos/test_video1.mp4 --output_folder outputs/sv4d`.
  - **Technical Details**:
    - Trained to generate 40 frames at 576x576 resolution.
    - Run demo locally with `python -m scripts.demo.gradio_app_sv4d`.
  - **Resources**: [Project page](https://sv4d.github.io), [Technical report](https://sv4d.github.io/static/sv4d_technical_report.pdf), [Video summary](https://www.youtube.com/watch?v=RBP8vdAWTgk).
  
  ![tile](assets/sv4d.gif)

### **March 18, 2024**
- 🎥 **[SV3D](https://huggingface.co/stabilityai/sv3d)**: An image-to-video model for multi-view synthesis.
  - **Run a demo** with `streamlit run scripts/demo/video_sampling.py`.
  - **Models**:
    - **SV3D_u**: Generates orbital videos from single images.
    - **SV3D_p**: Allows for camera path specification for 3D video.
  - **Documentation**: [Project page](https://sv3d.github.io), [Tech report](https://sv3d.github.io/static/paper.pdf), [Video summary](https://youtu.be/Zqw4-1LcfWg).

  ![tile](assets/sv3d.gif)

### **November 30, 2023**
- 🌟 Released **[SD-Turbo](https://huggingface.co/stabilityai/sd-turbo)**.

### **November 28, 2023**
- ⚡ **SDXL-Turbo**: A fast, high-quality text-to-image model.
  - **Installation**: `pip install streamlit-keyup`.
  - **Demo**: Run `streamlit run scripts/demo/turbo.py`.
  - **[Technical Report](https://stability.ai/research/adversarial-diffusion-distillation)**.
  - ![tile](assets/turbo_tile.png)

### **November 21, 2023**
- 🎬 **Stable Video Diffusion (SVD)** for image-to-video generation.
  - **Model Details**:
    - **SVD**: Generates 14 frames at 576x1024 resolution.
    - **SVD-XT**: Finetuned for 25 frames.
  - **Run Locally**: `python -m scripts.demo.gradio_app`.
  - **Demos**: `scripts/demo/video_sampling.py` and `scripts/sampling/simple_video_sample.py`.
  - **[Technical Report](https://stability.ai/research/stable-video-diffusion-scaling-latent-video-diffusion-models-to-large-datasets)**.
  - ![tile](assets/tile.gif)

### **July 26, 2023**
- 🌐 Released **SDXL-base-1.0** and **SDXL-refiner-1.0** models under the `CreativeML Open RAIL++-M` license.

![sample2](assets/001_with_eval.png)

### **July 4, 2023**
- 📄 Technical report for **SDXL** available [here](https://arxiv.org/abs/2307.01952).

### **June 22, 2023**
- 🌱 Released two new diffusion models:
  - **SDXL-base-0.9**: Trained with various aspect ratios and resolution 1024².
  - **SDXL-refiner-0.9**: Denoises data with small noise levels for image-to-image use only.

---

## 🔧 Installation Guide

### Step 1: Clone the Repository
```shell
git clone https://github.com/Stability-AI/generative-models.git
cd generative-models
```

### Step 2: Set Up Virtual Environment
**Note**: Tested with `python3.10`.

```shell
# Create virtual environment
python3 -m venv .pt2
source .pt2/bin/activate
pip3 install -r requirements/pt2.txt
```

### Step 3: Install `sgm`
```shell
pip3 install .
```

### Step 4: Install `sdata` for Training
```shell
pip3 install -e git+https://github.com/Stability-AI/datapipelines.git@main#egg=sdata
```

---

## 📦 Packaging

- **Build Wheel**:
```shell
pip install hatch
hatch build -t wheel
```

- **Install Wheel**:
```shell
pip install dist/*.whl
```

---

## 🤖 Inference

**Streamlit Demo**: `scripts/demo/sampling.py`.

**Supported Models**:
- [SDXL-base-1.0](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0)
- [SDXL-refiner-1.0](https://huggingface.co/stabilityai/stable-diffusion-xl-refiner-1.0)

**Weights** available under the `CreativeML Open RAIL++-M` license.

---

## 🛡️ Invisible Watermark Detection

Run detection with:

```bash
python -m venv .detect
source .detect/bin/activate

pip install "numpy>=1.17" "PyWavelets>=1.1.1" "opencv-python>=4.1.0.25"
pip install --no-deps invisible-watermark
```

**Test Commands**:
```bash
python scripts/demo/detect.py <your filename>
python scripts/demo/detect.py <filename 1> <filename 2> ... <filename n>
python scripts/demo/detect.py <your folder name>/*
```

---

## 🏋️ Training

Training configurations are available in `configs/example_training`. Start training with:

```shell
python main.py...
```

---

### Enhancements Added:
- **Icons** for visual engagement.
- **Bold headers** for improved section visibility.
- **Consistent layout** for easier navigation.
- **Shortened key instructions** with emphasis on main points.

Let me know if you need further tweaks!
