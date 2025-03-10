# HORIZON Clusters `text-classification` 🇪🇺 ⚾👩‍🔬
Building text classifiers for horizon clusters

This repository contains code for developing and implementing HORIZON Clusters classifiers, designed for efficient and accurate classification of STI records in HORIZON Clusters.

Clusters in Hirozn Europe area the following 6 domains
```
1. Health
2. Culture, Creativity and Inclusive Society
3. Civil Security for Society
4. Digital, Industry and Space
5. Climate, Energy and Mobility
6. Food, Bioeconomy, Natural Ressources, Agriculture and Environment
```

## Overview
This repository contains code for developing HORIZON Clusters classifiers. The project involves taxonomy consolidation, prompt engineering, dataset labelling, model training, and evaluation to classify records efficiently and accurately.

## Project Workflow

### 1. Dataset preparation
Sourced from the [SIRIS-Lab/unlabelled-sti-corpus](https://huggingface.co/datasets/SIRIS-Lab/unlabelled-sti-corpus), providing broader coverage of science, technology, and innovation literature globally.

### 2. Pseudolabelling
We employ a battery of methods for pseudolabelling:
1. Sciroshot – A zero-shot classifier for scientific documents.
2. Large Language Models (LLMs) – Multiple LLMs for classification.
3. Project-based Labelling – Using projects labelled with relevant HORIZON areas.

### 3. Label Consolidation
After pseudolabelling, we consolidate the assigned labels to enhance quality and consistency:
- Aggregation & Confidence Scoring: Combine outputs from different methods, assigning confidence scores to each label.
- Conflict Resolution: Resolve inconsistencies using heuristics, majority voting, or confidence-weighted decisions.
- Human Review (Optional): Sampled documents are manually checked to validate and refine labels.

### 4. Fine-Tuning the Classifier
- Model selection
- Training
- Evaluation & iteration

## Contribution Guidelines
We welcome contributions to improve the classifier and expand the dataset. To contribute:

- Create a new branch for your feature.
- Commit changes with clear messages
- Open a pull request for review.

## Environemnt

Create the environment from `environment.yml`
```bash
conda env create -f environment.yml --name horizon-classifiers
```

Export the environment, when we install need dependencies
```bash
conda env export --name horizon-classifiers > environemnt.yml
```

## License

This project is licensed under [Apache Licence](https://github.com/sirisacademic/horizon-clusters-text-classification/blob/main/LICENSE).

