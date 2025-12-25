

<div align="center">
<h1>LSA-DETR: Lightweight Spectral-Attentive Detection Transformer for UAV Small Objects</h1>
<div>




# The core innovation points of the paper

1.We propose LSA-DETR, a lightweight and robust UAV small-object detection framework that effectively addresses weak feature representation and scale variation.

2.We design LFRNet, enhanced with Compact Feature Refinement Blocks (CFRBs), to improve feature quality while reducing computational cost through decoupled convolution and adaptive feature reweighting.

3.We introduce SGE, integrating the Frequency Enhanced Feature Aggregation (FEFA) module to enhance frequency-domain cues and multi-scale fusion, improving small-object detail extraction. 

4.We propose AESIoU Loss, which incorporates a dynamic asymmetric extension mechanism and an angular direction penalty mechanism to improve localization precision and robustness.



# TODO List
- [x] Figure of results
- [ ] Code and datasets
- [ ] Release Code
- [ ] Inference code and checkpoint



# Overall architecture of the LSA-DETR

<img src="fig\fig2.png" alt="fig2"  />





# Core Module Description

<img src="Fig\Fig3.png" alt="fig3"  />

**The architecture of the proposed CFRB module**.



<img src="Fig\Fig4.png" alt="fig4"  />

 **Structure of the DSBlock module.**



<img src="Fig\Fig5.png" alt="fig5"  />

 **Structure of the FEFA module.**



# Result

<img src="Fig\Fig9.png" alt="fig9"  />

 **Visualized detection results on the Visdrone-2019-DET dataset using our proposed LSA-DETR and state-of-the-art methods. Blue dashed circles highlight missed detections (false negatives), while dashed red circles indicate false positives.**





<img src="Fig\Fig10.png" alt="fig10"  />

 **Heatmap comparison on the Visdrone-2019-DET dataset. From top to bottom: dense urban scene, sparse roadside with occlusion, large scale variation, low-light condition, and motion blur. LSA-DETR shows more accurate and robust activation on small and medium objects across challenging scenarios.**



<img src="Fig\Fig11.png" alt="fig11"  />

 **Comparison of dark environment detection results on the Visdrone-2019-DET dataset. Under challenging low-light conditions, LSA-DETR better preserves small-object responses and achieves more reliable localization than competing detectors.**



<img src="Fig\Fig12.png" alt="fig12"  />

 **Comparison of dark environment detection results on the Visdrone-2019-DET dataset. Under challenging low-light conditions, LSA-DETR better preserves small-object responsesandachievesmorereliablelocalizationthancompetingdetectors.**
