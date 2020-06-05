---
title: Visually Guided Sound Source Separation using Cascaded Opponent Filter Network
layout: default
---
# Abstract
The objective of this paper is to recover the original component signals from a mixture audio with the aid of visual cues of the sound sources. Such task is usually referred as visually guided sound source separation. The proposed Cascaded Opponent Filter (COF) framework consists of multiple stages, which recursively refine the sound separation based on appearance and motion information. A key element is a novel opponent filter module that identifies and relocates residual components between sound sources. Finally, we propose a Sound Source Location Masking (SSLM) technique, which, together with COF, produces a pixel level mask of the source location. The entire system is trained end-to-end using a large set of unlabelled videos. We compare COF with recent baselines and obtain state-of-the-art performance in three challenging datasets (MUSIC, A-MUSIC, and A-NATURAL). The implementation and pre-trained models will be made publicly available.

## The Architecture of COF-Net
![](cof-net/figures/cof.pdf?raw=true | width=500)
>The overall architecture of the proposed Cascaded Opponent Filter (COF) network. COF operates in multiple stages. The first stage contains three components: 1) a sound network that splits the input spectrogram into a set of feature maps; 2) a vision network that converts the input video sequences into compact representations; and 3) a sound separator that produces spectrograms of the component audios (one per video) based on the outputs of the sound and vision networks. The second stage contains similar sound and vision networks as the first one (internal details may differ). However, instead of the sound separator, the second stage contains a special opponent filter (OF) module, which enhances the separation result by transferring sound components between the sources. The output of the filter is passed to the next stage or used as the final output. The following stages are identical to the second one and, for this reason, we refer our method as cascaded opponent filter (COF) network. The final component audios are produced by applying the inverse STFT to the component spectrograms.

## The Architecture of OF and SSLM
![](cof-net/figures/of_sslm.pdf?raw=true | width=500)
>The Opponent Filter (OF) module identifies and relocates residual components between sound sources based on appearance and motion information. Sound Source Location Masking (SSLM) network identifies a minimum set of input pixels, for which the COF-Net would produce almost identical output as for the entire image.

## Paper
<blockquote class="embedly-card"><h4><a href="https://arxiv.org/abs/2006.03028">Visually Guided Sound Source Separation using Cascaded Opponent Filter Network</a></h4><p>The objective of this paper is to recover the original component signals from a mixture audio with the aid of visual cues of the sound sources.</p></blockquote>

## Code 
**Coming soon.**


<!--<iframe width="360" height="315" src="https://arxiv.org/abs/2006.03028"></iframe> -->
```  
#Citation 
@misc{zhu2020visually,
    title={Visually Guided Sound Source Separation using Cascaded Opponent Filter Network},
    author={Lingyu Zhu and Esa Rahtu},
    year={2020},
    eprint={2006.03028},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
```

<!--<img src="images/logo_tau.png" width="288" height="158"> -->
![Octocat](images/logo_tau.png?raw=true | width=288)
