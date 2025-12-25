<div align="center">
<h1>LSA-DETR: Lightweight Spectral-Attentive Detection Transformer for UAV Small Objects</h1>
</div>




# The core innovation points of the paper

1. We propose LSA-DETR, a lightweight and robust UAV small-object detection framework that effectively addresses weak feature representation and scale variation.

2. We design LFRNet, enhanced with Compact Feature Refinement Blocks (CFRBs), to improve feature quality while reducing computational cost through decoupled convolution and adaptive feature reweighting.

3. We introduce SGE, integrating the Frequency Enhanced Feature Aggregation (FEFA) module to enhance frequency-domain cues and multi-scale fusion, improving small-object detail extraction. 

4. We propose AESIoU Loss, which incorporates a dynamic asymmetric extension mechanism and an angular direction penalty mechanism to improve localization precision and robustness.



# TODO List
- [x] Figure of results
- [ ] Code and datasets
- [ ] Inference code and checkpoint



# Overall architecture of the LSA-DETR

<img src="fig\fig2.png" alt="fig2"  />
Fig2 ：Overall architecture of the LSA-DETR. The input image is encoded by LFRNet into multi-scale feature maps, where shallow features {S2, S3} are enhanced by the FEFA module and deep features {S4, S5} are fused through a sequence of upsampling and downsampling operations. The fused features are passed to the query selection module for informative query generation, and the decoder produces final classifications and bounding boxes.




# Core Module Description

<img src="fig\fig3.png" alt="fig3"  />

Fig3 : The architecture of the proposed CFRB module.



<img src="fig\fig4.png" alt="fig4"  />

Fig4 : Structure of the DSBlock module.



<img src="fig\fig5.png" alt="fig5"  />

Fig5 : Structure of the FEFA module.



# Result

<img src="fig\fig9.png" alt="fig9"  />

 Fig9 : Visualized detection results on the Visdrone-2019-DET dataset using our proposed LSA-DETR and state-of-the-art methods. Blue dashed circles highlight missed detections (false negatives), while dashed red circles indicate false positives. 



<img src="fig\fig10.png" alt="fig10"  />

Fig10 : Heatmap comparison on the Visdrone-2019-DET dataset. From top to bottom: dense urban scene, sparse roadside with occlusion, large scale variation, low-light condition, and motion blur. LSA-DETR shows more accurate and robust activation on small and medium objects across challenging scenarios.



<img src="fig\fig11.png" alt="fig11"  />

Fig11 : Comparison of dark environment detection results on the Visdrone-2019-DET dataset. Under challenging low-light conditions, LSA-DETR better preserves small-object responses and achieves more reliable localization than competing detectors.



<img src="fig\fig12.png" alt="fig12"  />

Fig12 : Comparison of real-world UAV detection results. Detection results are obtained from images captured by a UAV in real deployment scenarios involving partial occlusions, complex backgrounds, and significant scale variations.
