# Semver for machine learning models (WIP)
> A proposal for applying [semver](https://semver.org/) to machine learning models.

## Introduction
Semantic versioning is a popular and widely used standard for versioning software that handles the issues of breaking changes with regard to external APIs very well. In the field of data science, software engineering approaches are increasingly important, especially where machine learning (ML) models are productionised. For most tasks in deployment of machine learning software, the concepts from "traditional" software engineering translate well to the ML field. In other tasks, specialised approaches are needed, e.g. version control for data such as [DVC](https://dvc.org/).

## Motivation
One approach from software engineering that does not translate as well to ML, is semantic versioning. Versioning of machine learning models is often performed, but no agreed standard exists such as semantic versioning. Unfortunately, the existing standard behind semantic versioning cannot be readily applied to ML models, thus the need for a modified standard that takes into account the intricacies of ML models, whilst still offering the benefits of a multi-numbered version string.

## Proposal / specification
It is proposed that the existing format of **vMAJOR.MINOR.PATCH** be utilised, with the following specification:

1. The **MAJOR** version shall denote any of the following changes:
    * A change in the model architecture, including within the hidden layers, even if the input and output data shape / format are unchanged
    * A change in the format of the data e.g. 32-bit float to 8-bit float precision
    * A change in the input or output data shape e.g. [3, 128, 128] to [4. 128, 128]
2. The **MINOR** version
3. The **PATCH** version shall denote changes to trainining data used to train the model, whilst keeping all other aspects of the model constant.

### Compatibility
- As a **MAJOR** version increment can correspond to a change in model architecture, different major versions are not by default interoperable or compatible with one and another. Althought a **MAJOR** increment could also be simply due to updating the model architecture but keeping the same input and output data shape & format, as well being trained on the same data, the mere fact of a change in the model architecture could have more significant effects on the model performance which could make it in compatible with where it is being deployed, without a conscious decision for an update to this version.


## References
- [https://www.bryanwhiting.com/posts/2018-07-02-semantic-versioning-for-data-science-models/](https://www.bryanwhiting.com/posts/2018-07-02-semantic-versioning-for-data-science-models/)
