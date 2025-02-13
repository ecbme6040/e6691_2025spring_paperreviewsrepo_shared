# DistillBERT Prompt Injection Detector 

@author Jack Bosco (jab2516)

We pull an off-the-shelf pretrained DistilBERT 87M (https://huggingface.co/distilbert/distilbert-base-uncased) model from HuggingFace. 
After testing on the public prompt injection dataset (https://huggingface.co/datasets/Bogdan01m/Catch_the_prompt_injection_or_jailbreak_or_benign),
we finetune using qLoRA adaptors (https://doi.org/10.48550/arXiv.2305.14314) and demonstrate significant improvement in accuracy over just 4 epochs.

### Discussion

This is an anecdotal experiment demonstrating the practicality of hyper-parameter efficient LLMs for specific taks. 
Larger models and heavier adaptor sets will likely improve on our preliminary results.
Regardless, we show it is possible to solve non-trivial language modeling tasks by classifying prompts specifically intended to trick an LLM with fine-tuned DistilBERT.

### Other Reading
1. original BERT paper: https://doi.org/10.48550/arXiv.2305.14314
2. DistilBERT paper: https://doi.org/10.48550/arXiv.1910.01108
3. Overview on Parameter-Efficient Fine-Tuning: https://doi.org/10.48550/arXiv.2403.14608
