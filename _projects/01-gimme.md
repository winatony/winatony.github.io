---
layout: project
title: "GIMME: Graph inference for Microbial Metabolism Exploration"
description: Characterizing auxiliary metabolic genes in the human virome
img: /assets/img/GIMME_logo.png
category: Knowledge Representation and Reasoning
importance: 1
tags:
  - Deep Learning
  - Environmental Microbiology
  - Generative AI
  - Graph Inference
---

## Knowledge Graphs in Biology

Knowledge graphs (KGs) project biological entities as nodes and associations as relationships, forming a network that constrains reasoning. This is a particularly effective way of representing biological information, because biology information and structure is often complex and heirarchical. Graph neural networks (GNNs) are algorithms designed to allow learning over graphs, merging the strengths of machine learning for pattern identification, and the relational structure of graph databases. 

Random-Barcode Transposon Sequencing (RB-TnSeq) is an efficient method for high throughput, genome-wide fitness screening, where a pool of single gene knockout mutants can be distributed to laboratory plates containing different carbon, nitrogen, and stress sources. The resulting differential between a control condition and the experimental wells is known as the fitness delta, and is a relative measure of the gene knockout effect on organismal fitness. RB-TnSeq data is sparse, with a few gene knockouts producing large deleterious effects and many producing far more subtle effects, making it hard to infer metabolic significance for cryptic genes which do not have strong deleterious effects in any given condition.

### The Challenge

By projecting RB-TnSeq data as a knowledge graph, where the gene - fitness effect - experiment triple is connected to a large context network of biological information (gene effect, protein sequence) represented in different forms (natural language, embeddings, floating point numbers, etc.) as well as experimental context (experiment metadata, media concentration, chemical make up). Can these concepts and entities, alongside subtle patterns in fitness experiments, provide a rich substrate for the development of advanced graph models which can reason over these relationships and answer questions like:

- **Graph inference for fitness effect prediction in new organisms** What is the predicted effect of knocking out gene A in an organism we do not have data for (but do have data for other microbes)
- **KGs as World Models** Can large language models identify gaps in knowledge based on the structure of the graph? Can they see inconsistencies and testable patterns we cannot?

### Our Contribution

We are funded to build a KG and train a GNN predict **gene fitness** in Pseudomonas Putida from RB-TnSeq data. This database could be used to predict gene fitness profiles in new bacteria, and can be reasoned over to identify testable hypotheses for further reserach.

*More details on this project coming soon!*

### Related Publications

This work is part of PNNL's Predictive Phenomics Initiative (PPI).
