# Chroma-Modular-WF

Chroma is a new 8.9B parameter model, still being developed, based on Flux.1 Schnell.
It’s fully Apache 2.0 licensed, ensuring that anyone can use, modify, and build on top of it.
![Chroma Modular WF](https://www.tenofas.ai/wp-content/uploads/2025/07/f0da47b4b4f3b76f756640bbb9451350.png)
Like my other workflows, this will let you work with:
- txt2img or img2img,
-Detail-Daemon,
-Inpaint,
-HiRes-Fix,
-Ultimate SD Upscale,
-FaceDetailer.

The model is still being trained, so there are many updated versions (latest today, June 8th, is the v35). Here are all the versions: https://huggingface.co/lodestones/Chroma/tree/main

In brief, this model is:
    Training on a 5M dataset, curated from 20M samples including anime, furry, artistic stuff, and photos.
    Fully uncensored, reintroducing missing anatomical concepts.
    Built as a reliable open-source option for those who need it.

Being based on Flux.1 Schnell, it should run on low-Vram GPUs, so you can use it locally very easily.

You will need one of the t5xxl text encoder model files that you can find in: this repo, fp16 is recommended, if you don’t have that much memory fp8_scaled are recommended. Put it in the ComfyUI/models/text_encoders/ folder. The VAE is the same as FLUX or HiDream, so you should already have it.

Important: You must load an image (any image) in the Load Image node (at the left of the Prompts nodes) before running the workflow; otherwise, the workflow will give you an error. You must do this the first time you use the workflow only, and you must do it even if you are not planning to use that image for img2img or inpaint.
