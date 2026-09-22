# Course 07 Practical Notebook - Accelerate Your Model

This 60-minute practical explores how **model size and precision affect the memory needed to run a language model**.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aims-ai-research-foundations/Pretoria-workshop/blob/main/course-labs/day5/Course_07_Notebook.ipynb)

You will work with **Gemma 3** models to:

1. **Estimate** model memory from parameter count and precision.
2. **Predict** which configurations fit within a 4 GB memory budget.
3. **Apply** INT8 and INT4 quantisation.
4. **Measure** memory use (peak VRAM) and inference speed.
5. **Compare** response quality by inspecting model outputs.
6. **Make a final deployment decision based on your measurements.**

## Before you begin

### 1. Open the notebook in Google Colab

Open the notebook in [Google Colab](https://colab.research.google.com/github/aims-ai-research-foundations/Pretoria-workshop/blob/main/course-labs/day5/Course_07_Notebook.ipynb) and save your own copy:

**File → Save a copy in Drive**

### 2. Turn on a T4 GPU

In Google Colab, go to:

**Runtime → Change runtime type → T4 GPU → Save**

The notebook includes a cell to check that your GPU is ready.

### 3. Set up Hugging Face access

The Gemma models require access through [Hugging Face](https://huggingface.co/).

1. Go to [Hugging Face Access Tokens](https://huggingface.co/settings/tokens) and create a token with **Read** access.
2. Copy the token and add it to **Colab → Secrets** with the name `HF_TOKEN`.
3. Open the [Gemma 3 1B](https://huggingface.co/google/gemma-3-1b-it) model page and accept the terms of use.
4. Open the [Gemma 3 4B](https://huggingface.co/google/gemma-3-4b-it) model page and accept the terms of use.

## Notebook structure

The notebook follows three main phases:

1. **Measure**: Estimate how much memory a model needs and compare your estimate with what happens when you load it.

2. **Optimize**: Use quantization and a smaller model to reduce memory requirements.

3. **Evaluate**: Compare the different model options and decide which one you would use when memory is limited.

## Completing the notebook

Complete the **TODO** cells as you work through the notebook.

A hidden **Solutions** section is provided at the end so you can check your answers after attempting the exercises.

> Don't forget to have fun! 🚀🇬🇭