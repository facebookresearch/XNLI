# XNLI: The Cross-Lingual NLI Corpus
XNLI is an evaluation corpus for language transfer and cross-lingual sentence classification in 15 languages.

**New:** [Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md#models) uses XNLI to evaluate the quality of the cross-lingual representations.

## Introduction
Many NLP systems (e.g. sentiment analysis, topic classification, feed ranking) rely on training data in one high-resource language, but cannot be directly used to make predictions for other languages at test time.
This problem happens in almost any industrial application that involves cross-lingual data.

Machine translation can be used to translate any sample into the high-resource language to alleviate this issue.
However, having an MT system in every direction is costly and may not the best solution for cross-lingual classification.
Cross-lingual encoders are a cheaper and more elegant alternative.

**To evaluate such cross-lingual sentence understanding methods, we built XNLI, an extension of the
[SNLI](https://nlp.stanford.edu/projects/snli/)/[MultiNLI](https://www.nyu.edu/projects/bowman/multinli/) corpus in 15 languages.**
XNLI raises the following research question: how can we make predictions in any language at test time, when we only have English training data for that task?

While industrial applications may not include NLI in their routine tasks, we believe that NLI is a good testbed for evaluating cross-lingual
sentence representations, and that better approaches for XNLI will result in [better XLU methods](https://github.com/google-research/bert/blob/master/multilingual.md#results).

## The XNLI corpus
The Cross-lingual Natural Language Inference (XNLI) corpus is a crowd-sourced collection of *5,000 test and 2,500 dev pairs for the MultiNLI corpus*.
The pairs are annotated with textual entailment and translated into 14 languages: *French, Spanish, German, Greek, Bulgarian,
Russian, Turkish, Arabic, Vietnamese, Thai, Chinese, Hindi, Swahili and Urdu*. This results in 112.5k annotated pairs.
Each premise can be associated with the corresponding hypothesis in the 15 languages, summing up to more than 1.5M combinations.

![Examples](https://dl.fbaipublicfiles.com/XNLI/xnli_examples.png)

## Download
XNLI is distributed in a single ZIP file containing the corpus as both JSON lines (jsonl) and tab-separated text (txt). The English training data can be found on the [MultiNLI website](https://www.nyu.edu/projects/bowman/multinli/).

Download: [XNLI 1.0](https://dl.fbaipublicfiles.com/XNLI/XNLI-1.0.zip) (17MB, ZIP)

XNLI can also be used as a 15way parallel corpus of 10,000 sentences, for building or evaluating Machine Translation systems. XNLI provides additional open parallel data for low-resource languages such as Swahili or Urdu.

Download [XNLI-15way](https://dl.fbaipublicfiles.com/XNLI/XNLI-15way.zip) (12MB, ZIP)

## Useful XLU resources
Parallel data for aligning sentence encoders: [OPUS: the open parallel corpus](http://opus.nlpl.eu/)

Monolingual word embeddings in 157 languages: [fastText CommonCrawl vectors](https://github.com/facebookresearch/fastText/blob/master/docs/crawl-vectors.md)

Aligning word embeddings: [MUSE](https://github.com/facebookresearch/MUSE)


## Data description paper and citation

A description of the data can be found [here](https://arxiv.org/abs/1809.05053) or in the corpus package zip. If you use the corpus in an academic paper, please consider citing:

```
@InProceedings{conneau2018xnli,
  author = "Conneau, Alexis
        and Rinott, Ruty
        and Lample, Guillaume
        and Williams, Adina
        and Bowman, Samuel R.
        and Schwenk, Holger
        and Stoyanov, Veselin",
  title = "XNLI: Evaluating Cross-lingual Sentence Representations",
  booktitle = "Proceedings of the 2018 Conference on Empirical Methods
               in Natural Language Processing",
  year = "2018",
  publisher = "Association for Computational Linguistics",
  location = "Brussels, Belgium",
}
```

## Baselines and MT data
The [XNLI paper](https://arxiv.org/abs/1809.05053) presents several baselines for language adaptation.

We also release the machine translated data for reproducing the TRANSLATE-TRAIN and TRANSLATE-TEST:

Download: [XNLI-MT 1.0](https://dl.fbaipublicfiles.com/XNLI/XNLI-MT-1.0.zip) (445MB, ZIP)

## License
XNLI is licensed under the license found in the LICENSE file. See details in the [XNLI paper](https://arxiv.org/abs/1809.05053).
