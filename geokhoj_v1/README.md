# GEOKhoj v1

## Table of Contents

- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks](#supported-tasks-and-leaderboards)
  - [Languages](#languages)
- [Dataset Structure](#dataset-structure)
  - [Data Fields](#data-instances)
  - [Data Splits](#data-instances)
- [Additional Information](#additional-information)
  - [Motivation](#motivation)
  - [Licensing Information](#licensing-information)
  - [References](#references)


## Dataset Description

### Dataset Summary

Metadata has been extracted for samples from Microarray, Transcriptomics and Single cell experiments which are available on the GEO (Gene Expression Omnibus) database (GEO is a public functional genomics data repository supporting MIAME-compliant data submissions).
This dataset contains metadata for 30,000 samples with their respective labels (control/perturbed), which were labelled using the information available in the metadata.

What are control/perturbation samples? 
Control samples are samples whose composition, source  and type are well known. These samples are compared against perturbed samples which are altered (or perturbed) using environmental stimuli, drug inhibition, gene knockdown etc.


### Supported Tasks 

- `text-classification`: The dataset can be used to train a text classification model which can classify samples as control or perturbation

### Languages

The text in the dataset is in English

## Dataset Structure

### Data Fields

Each column corresponds to the following fields:

- `sample_id`: a `string` for unique identification. (This is the unique accession number(GSMXX) associated with a sample record on GEO)
- `label`: a classification label, with possible values including `Control` (0), `Perturbation` (1)
- `text`: a `string` feature.

### Data Splits

| name  |train|test|
|-------|----:|---:|
|default|25000|5000|


## Additional Information

### Motivation

With clean and curated metadata for public omics data, people have been able to study drug repurposing, suggest novel drugs for many diseases and explain mechanisms for many approved drugs. In the past, this has been done at a small scale by manually curating public data. But if we want to curate the millions of datasets available publicly we need classifiers trained on high-quality data to curate datasets at scale. GEOKhoj v1 has a large sample of high-quality annotations for public data from GEO with which we can train said classifiers for curation at scale. With this curated dataset we can enable researchers to generate gene signatures at scale which can be used to repurpose a drug, understand mechanism of a drug, understand a disease and explore normal biological mechanisms. 

### Licensing Information

https://creativecommons.org/licenses/by-nc/4.0/
