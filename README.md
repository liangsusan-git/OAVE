<div align="center">

<h2>Language-Guided Joint Audio-Visual Editing via One-Shot Adaptation</h2>

<a href='https://arxiv.org/abs/2410.07463'><img src='https://img.shields.io/badge/ArXiv-2410.07463-red'></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href='https://liangsusan-git.github.io/project/avedit/'><img src='https://img.shields.io/badge/Project-Page-Green'></a>


_**[Susan Liang](https://liangsusan-git.github.io/), [Chao Huang](https://wikichao.github.io/), [Yapeng Tian](https://www.yapengtian.com/), [Anurag Kumar](https://anuragkr90.github.io/), [Chenliang Xu](https://www.cs.rochester.edu/~cxu22/)**_

</div>

### Abstract

<b>TL; DR: We achieve joint audio-visual editing under language guidance.</b>

> In this paper, we introduce a novel task called language-guided joint audio-visual editing. Given an audio and image pair of a sounding event, this task aims at generating new audio-visual content by editing the given sounding event conditioned on the language guidance. For instance, we can alter the background environment of a sounding object while keeping its appearance unchanged, or we can add new sounds contextualized to the visual content. To address this task, we propose a new diffusion-based framework for joint audio-visual editing and introduce two key ideas. Firstly, we propose a one-shot adaptation approach to tailor generative diffusion models for audio-visual content editing. With as few as one audio-visual sample, we jointly transfer the audio and vision diffusion models to the target domain. After fine-tuning, our model enables consistent generation of this audio-visual sample. Secondly, we introduce a cross-modal semantic enhancement approach. We observe that when using language as content editing guidance, the vision branch may overlook editing requirements. This phenomenon, termed catastrophic neglect, hampers audio-visual alignment during content editing. We therefore enhance semantic consistency between language and vision to mitigate this issue. Extensive experiments validate the effectiveness of our method in language-based audio-visual editing and highlight its superiority over several baseline approaches.

### OAVE Dataset
We provide the One-Shot Audio-Visual Editing (OAVE) Dataset in this repository. The OAVE dataset consists of 44 distinct sounding events for benchmarking purposes, encompassing animals, vehicles, tools, natural phenomena, musical instruments, and human speech. We collect data from the MUSIC, AVSpeech, and VGGSound datasets. The figure below presents some examples from the OVAE dataset.
![dataset](./dataset.png)

Due to copyright restrictions, we only provide access to the processed data. By using this data, you agree to comply with all copyright and licensing terms associated with the MUSIC, AVSpeech, and VGGSound datasets.

The data is organized with the following directory structure.
```
.
├── accordion
│   ├── audio.wav
│   ├── frames_00001.png
│   ├── frames_00002.png
│   ├── frames_00003.png
│   ├── frames_00004.png
│   ├── frames_00005.png
│   ├── frames_00006.png
│   ├── frames_00007.png
│   ├── frames_00008.png
│   ├── frames_00009.png
│   └── frames_00010.png
├── acoustic_guitar
├── bagpipe
├── ...
```
For each sounding object, we provide
* `audio.wav`: one 10-second audio clip.
* `frames_*.png`: ten video frames sampled at 1 fps.
The audio-visual sample is used for model finetuning and evaluation. 

### Citation
```bib
@article{liang2024avedit,
  title={Language-Guided Joint Audio-Visual Editing via One-Shot Adaptation},
  author={Liang, Susan and Huang, Chao and Tian, Yapeng and Kumar, Anurag and Xu, Chenliang},
  journal={arXiv preprint arXiv:2410.07463},
  year={2024}
}
```

### Acknowledgment
This dataset is based on [MUSIC](https://github.com/roudimit/MUSIC_dataset),  [AVSpeech](https://looking-to-listen.github.io/avspeech/), and [VGGSound](https://www.robots.ox.ac.uk/~vgg/data/vggsound/) datasets. We thank the authors for sharing their datasets. If you use our dataset, please also consider citing their nice works.

### Contact
If you have any comments or questions, feel free to contact [Susan Liang](mailto:sliang22@ur.rochester.edu) and [Chao Huang](mailto:chuang65@ur.rochester.edu).
