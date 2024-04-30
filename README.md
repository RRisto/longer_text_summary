# (Longer) Estonian text summarization

Project to test different transformer-based models for (longer - up to 2048 tokens input) Estonian text summarization.


Models  tested:

- MBart
- MT5
- mLongT5

Methods for making models smaller/accepting longer context window:
- model embedding layers reduction -  keeping only tokens which are present in training data
- using [LSG Attention](https://github.com/ccdv-ai/convert_checkpoint_to_lsg)
- in some cases quantization

Datasets used for experimenting:

- [Estonian Parliament stenograms summaries](https://huggingface.co/datasets/rristo/et_parliament_stenos_summary)
- [TalTechNLP/samsum_ee](https://huggingface.co/datasets/TalTechNLP/samsum_ee)
- [TalTechNLP/LongSumEt](https://huggingface.co/datasets/TalTechNLP/LongSumEt)

Best model trained on [Estonian Parliament stenograms summaries](https://huggingface.co/datasets/rristo/et_parliament_stenos_summary) is available [here](https://huggingface.co/rristo/mlong-t5-tglobal-base-et-riigikogu-summary)

