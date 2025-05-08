
This guide helps you run [Kohya's Stable Diffusion trainers](https://github.com/kohya-ss/sd-scripts) on [Runpod.io](https://www.runpod.io) using a simple and fast setup.

> ✅ **Runpod-Only Instructions**  
> ⚠️ Local and Docker setups are not covered

---

## 🚀 Quick Start (Pre-Built Template)

The fastest way to launch Kohya GUI on Runpod:

1. Click the template below:  
   👉 [Launch Kohya GUI on Runpod](https://runpod.io/gsc?template=ya6013lj5a&ref=w18gds2n)
2. Select a GPU (e.g., A100, H100, 3090).
3. Click **Deploy**.
4. Wait for the pod to initialize.
5. Access the GUI via the exposed port (default: `7860`).

---

## 🛠 Manual Installation on Runpod

If you prefer a manual setup:

1. Start a **PyTorch 2.2.0** container on Runpod.
2. Open the terminal and run the following:

   ```bash
   cd /workspace
   git clone --recursive https://github.com/bmaltais/kohya_ss.git
   wget -O Realistic_sdxl.safetensors "https://huggingface.co/SG161222/RealVisXL_V5.0/resolve/main/RealVisXL_V5.0_fp16.safetensors?download=true"
   cd kohya_ss
   ./setup-runpod.sh
   ./gui.sh --share --headless
   ```

3. Access the GUI via the shared link or exposed port.

---

## 📌 Recommended Training Flow for dreambooth lora

Follow this 4-step workflow to train effectively using Kohya GUI:

### 1. Caption Your Images
- Go to the **Utilities** tab.
- Use the auto-captioning tool to label your training images.

### 2. Prepare Dataset (LoRA Tab)
- Switch to the **LoRA** tab.
- Load and organize your training dataset.

### 3. Set Training Parameters
- In the same **LoRA** tab:
  - Modify yours hyperparameters

### 4. Start Training
- Click **Start Training** and monitor progress through the GUI.

---
## for diffuser training, change the path to the data in notebook and directly training 

