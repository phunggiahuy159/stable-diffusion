# Kohya GUI - Runpod Only

This guide helps you run [Kohya's Stable Diffusion trainers](https://github.com/kohya-ss/sd-scripts) on [Runpod.io](https://www.runpod.io) using a simple and fast setup.

> ✅ **Runpod-Only** instructions  
> ⚠️ Local and Docker setups are not covered here

---

## 🚀 Quick Start (Pre-built Template)

The fastest way to launch Kohya GUI on Runpod:

1. Click this Runpod template:  
   👉 [Launch Kohya GUI on Runpod](https://runpod.io/gsc?template=ya6013lj5a&ref=w18gds2n)

2. Choose your GPU (e.g. A100, H100, 3090).
3. Click **Deploy**.
4. Wait for the pod to start.
5. Access the GUI via the exposed port (default: `7860`).

---

## 🛠 Manual Installation on Runpod

If you prefer not to use the template:

1. Start a **PyTorch 2.2.0** Runpod container.
2. Open a terminal and run, download your model if you want, for example:

   ```bash
   cd /workspace
   git clone --recursive https://github.com/bmaltais/kohya_ss.git
   wget -O Realistic_sdxl.safetensors "https://huggingface.co/SG161222/RealVisXL_V5.0/resolve/main/RealVisXL_V5.0_fp16.safetensors?download=true"
   cd kohya_ss
   ./setup-runpod.sh
   ./gui.sh --share --headless
3. Open GUI and started training
### recommend flow
Follow this workflow to effectively train using Kohya GUI:
1.Caption Your Images
   Navigate to the Utilities tab.
   Use the auto-captioning tool to label your training images.
2.Prepare Dataset via LoRA Tab
   Go to the LoRA tab.
   Organize and configure your dataset for training.
3.Set Training Parameters
   In the same LoRA tab:
   Set Max Steps to 2600
   Set LoRA Rank to 128
   Leave other hyperparameters at their default values for best compatibility.
4.Start Training
Once everything is set, click Start Training and monitor the progress.

