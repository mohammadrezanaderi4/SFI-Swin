# SFI-Swin: Symmetric Face Inpainting with Swin Transformer by Distinctly Learning Face Components Distributions
Official Pytorch implementation

by MohammadReza Naderi
, MohammadHossein Givkashi 
, Nader Karimi
, Shahram Shirani
, Shadrokh Samavi

[[arXiv](https://arxiv.org/abs/2301.03130)]
 
## Implementations
* Coming Soon ...
---
<p align="center">
  <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/GIF_final1.gif" width="90%"/>
</p>
<br>

## Blockdiagram
What is the general explainations of the proposed method?
<br>
First, the generator takes the masked image as input and attempts to inpaint it. Then the inpainted image is fed to the patch discriminator to check the overall reality of the patches. Meanwhile, the inpainted image is also fed into a semantic segmentation network to separate the semantic parts of the face, such as eyes, and ears. (The architecture of these six semantic discriminators is the same). In the next step, six distinct discriminators calculate the total realness of each semantic part of the face. Then, the generator parameters will be updated based on these seven discriminators and the pixel-wise loss gradient signals, which are backpropagated to the generator.

<div  align="center"> 
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/block%20diagram.png" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>

## FID and LPIPS comparison

<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Table1.PNG" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>

<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Fig2.png" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>

## SCS comparison
what is symmetry concentration score (SCS)?
<br>
Symmetry concentration Score is a newly introduce metric which explained compeletly in the paper to measure the symmerty of the repaired faces base on the concentration of the inpaintor.  
How to calculate it?
<br>
First, we mask an eye and a K×K patch of the face, and reconstruct the missing eye and the K×K patch. Then the absolute difference between the image with inpainted eye with the image with a missing K×K patch and the missing eye is computed. The difference shows the effect of that K×K patch on inpainting result of the missing eye. The effect of all K×K patches is computed and shown as a heatmap. The face borders are also depicted to investigate the impact of each part of the face on inpainting the missed eye.
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Fig4.png" width="90%">
</div>

</p>
<p align="center" "font-size:14px;">
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Table2.PNG" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Fig5.png" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>


## Acknowledgments
* [lama](https://github.com/saic-mdal/lama).
* [Swin-Unet](https://github.com/HuCaoFighting/Swin-Unet).
* Segmentation code and models if form [CSAILVision](https://github.com/CSAILVision/semantic-segmentation-pytorch).
* LPIPS metric is from [richzhang](https://github.com/richzhang/PerceptualSimilarity)
* FID is from [mseitzer](https://github.com/mseitzer/pytorch-fid)

## Citation
If you found this code helpful, please consider citing: 
```
@article{naderi2023sfi,
  title={SFI-Swin: Symmetric Face Inpainting with Swin Transformer by Distinctly Learning Face Components Distributions},
  author={Naderi, MohammadReza and Givkashi, MohammadHossein and Karimi, Nader and Shirani, Shahram and Samavi, Shadrokh},
  journal={arXiv preprint arXiv:2301.03130},
  year={2023}
}
```

