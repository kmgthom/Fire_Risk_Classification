# Fire_Risk_Classification
In recent decades wildfires have become increasingly destructive natural disasters that have resulted in massive property damage, injuries, and fatalities. These disasters have also wreaked havoc on forest ecosystems. To mitigate these consequences, it is imperative to prevent wildfires. One key step in preventing wildfires is to identify wildfire hazards and risks as much as possible. This allows for the proper responses to be taken to reduce these risks. Fire risk assessments are time-consuming processes that require both the identification and evaluation of the potential risks. While methods using satellite data such as surface temperature, moisture levels, and other geoscientific data exist, these still require specialized knowledge. Introducing remote sensing imagery and satellite imagery into the field can help in mapping geographical features to these measurements and reduce the specialized knowledge bottleneck.

This analysis seeks to examine whether remote sensing imagery can be used to classify land areas into fire risk levels. The FireRisk dataset, a collection of remote sensing imagery of different classifications of wildfire risks, was used for the analysis. In this work, the FireRisk dataset was used to construct CNNS to classify images into 7 fire risk levels. The dataset itself was highly imbalanced, with a bias toward very low fire risk and non-burnable areas. Three baseline models were built and compared, with the best performing baseline model being advanced for additional fine tuning. The best performing baseline model used a ResNet50 backbone, pre-trained on the ImageNet dataset. After selecting the backbone, a new model was constructed to improve on the baseline model. Once the architecture was finalized, the model’s hyperparameters were tuned to further improve performance.
The analysis concludes that it may be possible to use remote sensing imagery to assess areas for fire risk. However, due to the imbalanced nature of the dataset, the model was not effective at detecting risks. Rather, it was highly effective at identifying non-burnable areas, water, or very low risk fire areas. Additional testing with a more balanced dataset may provide better results and increase the potential use of the model. The final model achieved a validation accuracy of 60.13%. After further examination of the F1 scores, this accuracy was found to be due to the high bias towards non-burnable, water, or very low fire risk classes. The model struggled to correctly identify low to very high-level fire risks. Overall, the use of remote sensing imagery for fire risk assessment may have some potential. However, relying only on remote sensing imagery may not be the most successful of methods on its own. Instead, it could help to augment other methods rather than stand on its own.

### Data Source
@misc{shen2023fireriskremotesensingdataset,

title={FireRisk: A Remote Sensing Dataset for Fire Risk Assessment with Benchmarks Using Supervised and Self-supervised Learning}, 

author={Shuchang Shen and Sachith Seneviratne and Xinye Wanyan and Michael Kirley},
      
      year={2023},
      
      eprint={2303.07035},
      
      archivePrefix={arXiv},
      
      primaryClass={cs.CV},
      
      url={https://arxiv.org/abs/2303.07035}, 
}
