# Zero-Shot Evaluation of CLIP Models on Compositional Datasets

## Description

This project provides a comprehensive benchmark for evaluating the zero-shot performance of CLIP models on novel compositional concepts.

80 variants of CLIP are tested on procedurally generated datasets combining adjectives and nouns in a compositional manner. Models are evaluated on their ability to generalize to these OOD combinations not seen during pretraining. 

Analysis is provided on how different model capacities, architectures, and pretraining datasets impact zero-shot compositional generalization. Performance is also compared systematically to supervised ImageNet models.

## CLIP Models

The following CLIP models are evaluated:

- ViT-B/32, ViT-B/16, ViT-L/14 pretrained on 400M image-text pairs from web data
- Models pretrained on YFCC15M dataset
- CoCa and CC12M models pretrained on COCO captions
- Models like CLIP-ViT-B-8, CLIP-ViT-L-14

These models vary in:

- Backbone CNN architectures (ResNet, ViT, EfficientNet)
- Model capacities
- Pretraining dataset scale and domain

This tests the effect of these factors on zero-shot generalization.

## Evaluation Datasets  

- **Adjective-Noun Compositions**: All combinations of 20 common adjectives and 20 nouns. (e.g. yellow cat, old book)
- **Noun Compositions**: All pairs of 20 common nouns. (e.g. cat and book) 

Images are generated procedurally or scraped from the web for each composition.

## Evaluation Settings

- **Zero-shot**: Models are evaluated without any fine-tuning on the compositional datasets. 
- **Few-shot**: Models are fine-tuned on a small labeled subset of 5-10 images per class.

## References

- [CLIP](https://arxiv.org/abs/2103.00020)
- [open_clip](https://github.com/mlfoundations/open_clip)
- [timm](https://github.com/rwightman/pytorch-image-models)
