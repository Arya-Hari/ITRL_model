---
license: apache-2.0
base_model: Salesforce/codet5-base
tags:
- generated_from_keras_callback
model-index:
- name: ITRLTrained
  results: []
---

<!-- This model card has been generated automatically according to the information Keras had access to. You should
probably proofread and complete it, then remove this comment. -->

# ITRLTrained

This model is a fine-tuned version of [Salesforce/codet5-base](https://huggingface.co/Salesforce/codet5-base) on [ITRLDataset](https://huggingface.co/datasets/AshArya/ITRLDataset)


## Model description

The model is a fine-tuned version of the CodeT5-base model by Salesforce. It has been fine-tuned on a custom dataset with over 1200 entries.

## Intended uses & limitations

Its intended use is to act as a text-to-code generator. The Natural Language (NL) input is in the form of algorithmic statements and the model generates 1-2 lines of Python code corresponding to the input.

## Training and evaluation data

[AshArya/ITRLDataset](https://huggingface.co/datasets/AshArya/ITRLDataset)

## Training procedure

Fine-tuning of [Salesforce/codet5-base](https://huggingface.co/Salesforce/codet5-base) using PyTorch and Transformers with custom training arguments and a custom training loop.

### Training hyperparameters

The following hyperparameters were used during training:
- optimizer: XLA
- training_precision: float32

### Training results

The model achieves high accuracy during human evaluation. It achieves a ROUGE-L score of 0.359662899235267 and a chrF score of 9.637061227631952 after the fine-tuning. The original model achieves a score of 0.06735368389780155 and 3.021597905833814 respectively. 

### Framework versions

- Transformers 4.35.2
- TensorFlow 2.14.0
- Tokenizers 0.15.0
