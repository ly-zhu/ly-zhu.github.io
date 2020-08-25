---
title: Predicting Gene Expression Levels from Histone Modification Signals with Convolutional Recurrent Neural Networks
layout: default1
---

[[Paper]](https://link.springer.com/chapter/10.1007/978-981-10-5122-7_139) | [[Code]](https://github.com/ly-zhu/CRNN-gene-expression-with-histone-modifications)
<!-- [[Code **Coming soon.**]](https://github.com/ly-zhu/cof-net) -->

# Abstract
In this paper we study how a Convolutional Recurrent Neural Network performs for predicting the gene expression levels from histone modification signals. Moreover, we consider two simplified variants of the Convolutional Recurrent Neural Network: Convolutional Neural Network and Recurrent Neural Network. The performance of the methods is evaluated with histone modification signal and gene expression data derived from Roadmap Epigenomics Mapping Consortium database, and compared against the state of the art method: the DeepChrome. It is shown that the proposed models give a statistically significant improvement over the baseline.

## Architecture
<!-- ![](cof-net/figures/cof.png?raw=true | width=500) -->
<img src="crnn/figures/crnn.png" width="800"/>

The architecture of the proposed CRNN model is composed of six layers: two convolutional layers followed by one LSTM layer, two dense layers and one output layer. The first two convolutional layers map the input gene sequences from a 100 × 5 matrix into 32 feature maps with the size of 3×3 filters and a stride of 3. Before feeding the output of the convolutional layers into the recurrent layer, the feature maps were concatenated along histone axis in order to intensify the effects of histone modifications while keeping the bin axis unchanged. In the LSTM layer with 32 nodes, dropout operations are applied to the input gates and recurrent connections for alleviating overfitting. After that, there are two fully connected layers with 100 and 20 nodes respectively. We adopt the Rectified Linear Unit (RELU) activation function and dropout regularizer to each layer, and sigmoid operator to the output layer for the final binary prediction.



<!--
## Paper
<blockquote class="embedly-card"><h4><a href="https://arxiv.org/abs/2006.03028">Visually Guided Sound Source Separation using Cascaded Opponent Filter Network</a></h4><p>The objective of this paper is to recover the original component signals from a mixture audio with the aid of visual cues of the sound sources.</p></blockquote>
<script async src="//cdn.embedly.com/widgets/platform.js" charset="UTF-8"></script>
-->

<!-- 
## Code 
**Coming soon.**
-->

<!--<iframe width="360" height="315" src="https://arxiv.org/abs/2006.03028"></iframe> -->

## Citation
```bibtex 
@incollection{zhu2017predicting,
  title={Predicting Gene Expression Levels from Histone Modification Signals with Convolutional Recurrent Neural Networks},
  author={Zhu, Lingyu and Kesseli, Juha and Nykter, Matti and Huttunen, Heikki},
  booktitle={EMBEC \& NBC 2017},
  pages={555--558},
  year={2017},
  publisher={Springer}
}
```

<img src="images/logo_tau.png" width="288">
<!-- ![Octocat](images/logo_tau.png?raw=true | width=288) -->
