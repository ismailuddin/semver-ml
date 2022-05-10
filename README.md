# Semver for machine learning models (WIP)
> A proposal for applying [semver](https://semver.org/) to machine learning models.

## Introduction
Semantic versioning is a popular and widely used standard for versioning software that handles the issues of breaking changes with regard to external APIs very well. In the field of data science, software engineering approaches are increasingly important, especially where machine learning (ML) models are productionised. For most tasks in deployment of machine learning software, the concepts from "traditional" software engineering translate well to the ML field. In other tasks, specialised approaches are needed, e.g. version control for data such as [DVC](https://dvc.org/).

## Motivation
One approach from software engineering that does not translate as well to ML, is semantic versioning. Versioning of machine learning models is often performed, but no agreed standard exists such as semantic versioning. Unfortunately, the existing standard behind semantic versioning cannot be readily applied to ML models, thus the need for a modified standard that takes into account the intricacies of ML models, whilst still offering the benefits of a multi-numbered version string.

## Proposal
It is proposed that the existing...


## References
- [https://www.bryanwhiting.com/posts/2018-07-02-semantic-versioning-for-data-science-models/](https://www.bryanwhiting.com/posts/2018-07-02-semantic-versioning-for-data-science-models/)
