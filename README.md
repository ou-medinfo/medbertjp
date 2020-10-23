# Japanese Medical BERT
Trials of pre-trained BERT models for the medical domain in Japanese.

# Our demonstration models  
  * [medBERTjp - MeCab-IPAdic](https://github.com/ou-medinfo/medbertjp/releases/tag/v0.1-mi)
    - pre-trained this model following [the Japanese BERT model](https://github.com/cl-tohoku/bert-japanese/).
    - max_seq_length=128
  * [medBERTjp - MeCab-IPAdic-NEologd-JMeDic](https://github.com/ou-medinfo/medbertjp/releases/tag/v0.1-minj)
    - change dictionaries for MeCab and pre-trained this model.
    - max_seq_length=128
  * [medBERTjp - SentencePiece](https://github.com/ou-medinfo/medbertjp/releases/tag/v0.1-sp)
    - use tokenization by SentencePiece.
    - max_seq_length=128

# Requirements
For just using the models:  
+ [Transformers](https://github.com/huggingface/transformers/) (>=2.11.0)
+ [fugashi](https://github.com/polm/fugashi) with [MeCab](https://taku910.github.io/mecab/)
    - [ipadic](https://github.com/polm/ipadic-py), [mecab-ipadic-NEologd](https://github.com/neologd/mecab-ipadic-neologd/), and [J-MeDic](http://sociocom.jp/~data/2018-manbyo/): if required.
+ [SentencePiece](https://github.com/google/sentencepiece/) would be already installed with the transformers.

# Usage
Please check code examples of [`tokenization_example.ipynb`](./tokenization_example.ipynb).

# Licenses
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />The pretrained models are distributed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)</a>.   
They are freely available for academic purpose or individual research, but restricted for commecial use.  


The codes in this repository are distributed under the MIT License.
