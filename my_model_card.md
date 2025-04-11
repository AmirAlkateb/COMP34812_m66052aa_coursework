---
{}
---
language: en
license: cc-by-4.0
tags:
- text-classification
repo: https://github.com/username/project_name

---

# Model Card for m66052aa-track_ED


This is a classification model that was trained to
      detect whether a piece of evidence supports a claim.



### Model Description


This model is based upon a BERT model that was fine-tuned
      on 21K pairs of texts.

- **Developed by:** Amir Alkateb
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** Transformers
- **Finetuned from model [optional]:** bert-base-uncased

### Model Resources


- **Repository:** https://huggingface.co/google-bert/bert-base-uncased
- **Paper or documentation:** https://aclanthology.org/N19-1423.pdf

## Training Details

### Training Data


21K pairs of claims and evidence.

### Training Procedure


#### Training Hyperparameters



      - learning_rate: 2e-05
      - train_batch_size: 16
      - eval_batch_size: 32
      - num_epochs: 3

#### Speeds, Sizes, Times



      - overall training time: 2 hours
      - duration per training epoch: 40 minutes
      - model size: 300MB


#### Testing Data


7k pairs of claims and evidence.

#### Metrics



      - F1-score
      - Accuracy

### Results

The model obtained an F1-score of 74% and an accuracy of 87%.

## Technical Specifications

### Hardware


      - RAM: at least 16 GB
      - Storage: at least 2GB,
      - GPU: T4

### Software


      - Transformers 4.18.0
      - Pytorch 1.11.0+cu113

## Bias, Risks, and Limitations


Any inputs (concatenation of two sequences) longer than
      512 subwords will be truncated by the model.

## Additional Information


The hyperparameters were determined by experimentation
      with different values.

## Use of Generative AI Tools

I used chatgpt to advise me on how to optimise the model for running locally on a macbook pro.