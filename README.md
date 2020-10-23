# Japanese Medical BERT
Trials of pre-trained BERT models for the medical domain in Japanese.  
The medical corpora are scraped for academic use from [Today's diagnosis and treatment : premium](https://www.igaku-shoin.co.jp/bookDetail.do?book=89056), which consists of 15 digital references for clinicians in Japanese published by [IGAKU-SHOIN Ltd.](https://www.igaku-shoin.co.jp/).  
The general corpora are extracted from a Wikipedia dump file (jawiki-20190901)　on https://dumps.wikimedia.org/jawiki/.

## Our demonstration models  
  * [medBERTjp - MeCab-IPAdic](https://github.com/ou-medinfo/medbertjp/releases/tag/v0.1-mi)
    - pre-trained model following [MeCab-IPAdic-tokenized Japanese BERT model](https://github.com/cl-tohoku/bert-japanese/).
    - tokenizer: [MeCab](https://taku910.github.io/mecab/)
    - [ipadic-py](https://github.com/polm/ipadic-py), or manual install of IPAdic is required.
    - max_seq_length=128
  * [medBERTjp - Unidic-2.3.0] will be uploaded soon.
    - tokenizer: [MeCab](https://taku910.github.io/mecab/)
    - Unidic v2.3.0+2020-10-08 via [unidic-py](https://github.com/polm/unidic-py) is required.
    - max_seq_length=128
  * [medBERTjp - MeCab-IPAdic-NEologd-JMeDic](https://github.com/ou-medinfo/medbertjp/releases/tag/v0.1-minj)
    - tokenizer: [MeCab](https://taku910.github.io/mecab/)
    - install of both [mecab-ipadic-NEologd](https://github.com/neologd/mecab-ipadic-neologd/) and [J-MeDic (MANBYO_201907_Dic-utf8.dic)](http://sociocom.jp/~data/2018-manbyo/) is required.
    - max_seq_length=128
  * [medBERTjp - SentencePiece](https://github.com/ou-medinfo/medbertjp/releases/tag/v0.1-sp)
    - tokenizer: [SentencePiece](https://github.com/google/sentencepiece/)
    - use customized tokenization for the medical domain by SentencePiece following [Sentencepiece Japanese BERT model](https://github.com/yoheikikuta/bert-japanese)
    - max_seq_length=128

## Requirements
For just using the models:  
+ [Transformers](https://github.com/huggingface/transformers/) (>=2.11.0)
+ [fugashi](https://github.com/polm/fugashi), a Cython wrapper for [MeCab](https://taku910.github.io/mecab/)
    - [ipadic](https://github.com/polm/ipadic-py), [unidic-py](https://github.com/polm/unidic-py), [mecab-ipadic-NEologd](https://github.com/neologd/mecab-ipadic-neologd/), and [J-MeDic](http://sociocom.jp/~data/2018-manbyo/): if required.
+ [SentencePiece](https://github.com/google/sentencepiece/) would be automatically installed with the transformers.

## Usage
Please check code examples of [`tokenization_example.ipynb`](./tokenization_example.ipynb), or try to use [`example_google_colab.ipynb`](./example_google_colab.ipynb) on [Google Colab](https://colab.research.google.com/).

## Funding
This work was supported by Council for Science, Technology and Innovation (CSTI), cross-ministerial Strategic Innovation Promotion Program (SIP), "Innovative AI Hospital System" (Funding Agency: National Institute of Biomedical Innovation, Health and Nutrition (NIBIOHN)).

## Licenses
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />The pretrained models are distributed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)</a>.   
They are freely available for academic purpose or individual research, but restricted for commecial use.  


The codes in this repository are licensed under the Apache License, Version2.0.
