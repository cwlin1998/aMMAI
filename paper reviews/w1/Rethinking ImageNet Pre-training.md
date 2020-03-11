# Rethinking ImageNet Pre-training

Kaiming He	Ross Girshick	Piotr Dollár

Facebook AI Research

## Novelties

Since pre-training had been pretty popular in those days and many papers were using this technique, it was the first time that a paper systemmatically discussed whether pre-training is necessary or not.

## Experiments

Compares the accuracy between training from scratch and with pre-training using the same model in many different cases, such as ResNet, keypoint detection, large model, models without BN/GN.

Moreover, compares while using less data such as 35k COCO and 10k COCO.

We can observe that the accuracy of training from scratch are able to catch up the one with pre-training over time from all experiments.

## Conclusions

1. ImageNet pre-training is not necessary as long as we have enough target data (and computation). (10k COCO dataset is enough according to the experiment)
2. ImageNet pre-training is still helpful since it is able to speed up convergence and pre-trained models are widely and freely available today. Therefore, we can easier access to encouraging result.
3. ImageNet pre-training helps less if the target task is more sensitive to localization than classification.

