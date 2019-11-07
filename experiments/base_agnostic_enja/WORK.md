# 11/07
## data preprocessing
### agnostic data
    *  data is exsists in data/
    * clone data (OpenSub2016, OntoNotes)
    * tokenize ja with mecab
    * lowerize en file
    *  apply BPE with 32K voc
### aware data
    * 連続する二つの文をつなげる
    * ほんとはdocの切れ目で切りたいけど、切れ目がわからない、(調べる )
    * agnosticでbpeしたものを、連続2文でくっつける 
    * <eos>でconca

### cnn data
    * 前データで14K
    * 連続するに文をつなげる
    * nanの場合はどうしよう
        * nanはremoveして、その後の文を、連続として扱う方向性
    * とりあえず、para-dataにするところまではできた。


# TODO
* NLTKなら使えそう
* OpenSubの方の、英語もtokenize .moses?
