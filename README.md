# Optimising Text2Image via Search and Negative Prompts
This repository contains the code and results for the paper titled "Optimising Text2Image Generation via Search and Negative Prompts". The goal of this work is to enhance the text-to-image generation process through optimization techniques involving search and negative prompts.

## Introduction
Text-to-image generation has seen significant advancements in recent years, but improving the quality and relevance of generated images remains a challenging task. This repository presents an approach that leverages search algorithms and negative prompts to optimize the text-to-image generation process.

## Notebooks
### 1. Prompt_Engineering_Notebook.ipynb
This notebook is utilized to execute the optimization process. It involves fetching images from the DiffusionDB database and optimizing their prompts to enhance image generation.

### 2. Save_Form_images.ipynb
The purpose of this notebook is to take the images generated in the previous notebook and produce the images in the format used for human evaluation.

### 3. Generate_Results.ipynb
This notebook processes the outcomes of the optimization process and the generated form images. It calculates the metrics used in the results section of the paper.

### Results
The results obtained from executing the notebooks demonstrate the effectiveness of the proposed approach in improving text-to-image generation quality.

We can observe, for different prompts, how the generation process proposed in our approach improves the adequacy respect the prompt:
| Prompt | Our results | DiffusionDB results |
| :-------- | :--- | :--- |
| `honey label by adolphe mucha` | <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/004_best.png" width="500"> | <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/004_base.png" width="500"> |
| `turn of the century sepia photo of a man waiting at the train station while using an ipad` | <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/005_best.png" width="500">| <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/005_base.png" width="500"> |
| `huge glitter bomb explosion above city` | <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/007_best.png" width="500"> | <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/007_base.png" width="500"> |
| `3 d octane render of a glowing yellow orb with clear wings flying` |<img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/016_best.png" width="500"> | <img src="https://raw.githubusercontent.com/guillermoih/Improving-GenAI-with-negative-prompts/master/results/016_base.png" width="500"> |

The rest of the images are stored in `results/` folder. While `form_imgs/` contains the images used in the human evaluation form.

Results of the research are contained in `Generate_Results.ipynb` notebook.

## Experimental set-up
For our experiments we used Stable Diffusion v2 [implemented by Stability AI](https://huggingface.co/stabilityai/stable-diffusion-2 "Stable Diffusion v2 implementation"), BLIP [implemented by Salesforce](https://huggingface.co/Salesforce/blip-image-captioning-large "BLIP implementation") and all-mpnet-base-v2 [implemented by SBERT]([https://huggingface.co/Salesforce/blip-image-captioning-large](https://huggingface.co/sentence-transformers/all-mpnet-base-v2) "MPNet implementation").

All experiments were conducted on on two 48 GB Nvidia Quadro RTX 8000 GPUs and an Intel Xeon Bronze 3206R CPU @ 1.90GHz.

### Contact
For any questions or feedback regarding this repository, feel free to contact guillermo.iglesias@upm.es .
