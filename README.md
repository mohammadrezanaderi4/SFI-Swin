# SFI-Swin: Symmetric Face Inpainting with Swin Transformer by Distinctly Learning Face Components Distributions
Official implementation

by MohammadReza Naderi
, MohammadHossein Givkashi 
, Nader Karimi
, Shahram Shirani
, Shadrokh Samavi

[[arXiv](https://arxiv.org/abs/2301.03130)]
 


<p align="center">
  <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/GIF_final1.gif" width="90%"/>
</p>
<br>
<br>
<br>

## Blockdiagram


<div  align="center"> 
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/block%20diagram.png" width="90%">
</div>
<p align="center" "font-size:14px;">
Block diagram of our proposed method.
</p>

<br>
<br>
<br>

## FID and LPIPS comparison

<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Table1.PNG" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>
<br>
<br>
<br>
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Fig2.png" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>

<br>
<br>
<br>

## SCS comparison
what is symmetry concentration score (SCS)?
<br>
Symmetry concentration Score is a newly introduce metric which expailed compeletly in the paper to measure the symmerty of the repaired faces base on the concentration of the inpaintor.  
How to calculate it?
<br>
First, we mask an eye and a K×K patch of the face, and reconstruct the missing eye and the K×K patch. Then the absolute difference between the image with inpainted eye with the image with a missing K×K patch and the missing eye is computed. The difference shows the effect of that K×K patch on inpainting result of the missing eye. The effect of all K×K patches is computed and shown as a heatmap. The face borders are also depicted to investigate the impact of each part of the face on inpainting the missed eye.
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Fig4.png" width="90%">
</div>

</p>
<br>
<br>
<br>
<p align="center" "font-size:14px;">
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Table2.PNG" width="90%">
</div>
<p align="center" "font-size:14px;">
</p>
<br>
<br>
<br>
<div  align="center">
    <img src="https://github.com/mohammadrezanaderi4/SFI-Swin/blob/main/Fig5.png" width="90%">
</div>
<p align="center" "font-size:14px;">
Block diagram of our proposed method.
</p>

## Implementations
* Coming Soon ...

## Acknowledgments
* lama [CSAILVision](https://github.com/CSAILVision/semantic-segmentation-pytorch).
* Swin-Unet [CSAILVision](https://github.com/CSAILVision/semantic-segmentation-pytorch).
* Segmentation code and models if form [CSAILVision](https://github.com/CSAILVision/semantic-segmentation-pytorch).
* LPIPS metric is from [richzhang](https://github.com/richzhang/PerceptualSimilarity)
* SSIM is from [Po-Hsun-Su](https://github.com/Po-Hsun-Su/pytorch-ssim)
* FID is from [mseitzer](https://github.com/mseitzer/pytorch-fid)

## Citation
If you found this code helpful, please consider citing: 
```
@article{naderi2023sfi-swin,
  title={SFI-Swin: Symmetric Face Inpainting with Swin Transformer by Distinctly Learning Face Components Distributions},
  author={Naderi, MohammadReza and Givkashi, MohammadHossein and Karimi, Nader and Shirani, Shahram and Samavi, Shadrokh},
  journal={arXiv preprint arXiv:2301.03130},
  year={2023}
}
```

