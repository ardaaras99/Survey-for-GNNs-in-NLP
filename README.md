# Main Papers of GNNs in the NLP domain and Interesting Implementations of GNNs in the other Fields.
*Contributed by Arda Can Aras.*
## Preliminary Definitions
- **Transductive**: You have a single graph (like Cora) you split some nodes (and not graphs) into train/val/test training sets. While you're training you'll be using only the labels from your training nodes. During the forward prop, by the nature of how spatial GNNs work, you'll be aggregating the feature vectors from your neighbors and some of them may belong to val or even test sets! The main point is - you ARE NOT using their label information but you ARE using the structural information and their features.

- **Inductive**: You have a set of training graphs, a separate set of val graphs and of course a separate set of test graphs. Generally aim is to learn generalizable transformations of embeddings instead of having direct matrix multiplications like in [GCNConv](https://arxiv.org/abs/1609.02907). 
- **Heterogeneous Graph**: Graphs that can be directed or can include different type of nodes like in [TextGCN](https://arxiv.org/abs/1809.05679).

Note: For more comprehensive and general GNNs implementation in several different fields, please check this [GitHub repo](https://github.com/ardaaras99/GNNPapers#survey-papers).
## [Content](#content)

<table>
<tr><td colspan="2"><a href="#survey-papers">1. Survey</a></td></tr> 
<tr><td colspan="2"><a href="#models">2. Models</a></td></tr>
<tr>
    <td>&ensp;<a href="#basic-models">2.1 Basic Models</a></td>
    <td>&ensp;<a href="#graph-types">2.2 Graph Types</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#pooling-methods">2.3 Pooling Methods</a></td>
    <td>&ensp;<a href="#analysis">2.4 Analysis</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#efficiency">2.5 Efficiency</a></td>
    <td>&ensp;<a href="#explainability">2.6 Explainability</a></td>
</tr>
<tr><td colspan="2"><a href="#natural-language-processing">3. Natural Language Processing</a></td></tr> 
<tr>
    <td>&ensp;<a href="#text-classification">3.1 Text Classification</a></td>
    <td>&ensp;<a href="#question-answering">3.2 Question Answering</a></td>
</tr> 
</table>

## [Survey Papers](#content)
1. **Graph Neural Networks for Natural Language Processing: A Survey** . [paper](https://arxiv.org/abs/2106.06090)

    *Lingfei Wu, Yu Chen, Kai Shen, Xiaojie Guo, Hanning Gao, Shucheng Li, Jian Pei, Bo Long* 

    
## [Models](#content)   
### [Basic Models](#content)
The following models are not inherently designed to tackle problems in NLP domain. However, they are easily
applicable and their implementations are available at [PyG](https://pytorch-geometric.readthedocs.io/en/latest/notes/cheatsheet.html) (PyTorch Geometric) website.

1. **Semi-Supervised Classification with Graph Convolutional Networks** *Thomas N. Kipf, Max Welling*. [paper](https://arxiv.org/abs/1609.02907) (GCNConv)
   
    - Short Model Description (SMD): Basic aggregation of neighbor nodes with transductive manner. Simple matrix multiplication is possible due to its nature.
<br><br>

1. **Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering**  *Michaël Defferrard, Xavier Bresson, Pierre Vandergheynst.* [paper](https://arxiv.org/abs/1606.09375) (ChebConv)
   
    - SMD: 
<br><br>

1. **Inductive Representation Learning on Large Graphs** *William L. Hamilton, Rex Ying, Jure Leskovec.* [paper](https://arxiv.org/abs/1706.02216)
   
   - SMD: Trying to learn generalizable aggregation functions in an inductive manner. 3 main approaches tried for aggregation in paper (sum,pool,lstm).
<br><br>

1. **Weisfeiler and Leman Go Neural: Higher-order Graph Neural Networks** *Christopher Morris, Martin Ritzert, Matthias Fey, William L. Hamilton, Jan Eric Lenssen, Gaurav Rattan, Martin Grohe.* [paper](https://arxiv.org/abs/1810.02244)
   
   - SMD: 
<br><br>

1. **Gated Graph Sequence Neural Networks** *Yujia Li, Daniel Tarlow, Marc Brockschmidt, Richard Zemel* [paper](https://arxiv.org/abs/1511.05493)
   
   - SMD: 
<br><br>

1. **Residual Gated Graph ConvNets** *Xavier Bresson, Thomas Laurent* [paper](https://arxiv.org/abs/1711.07553)
   
   - SMD: 
<br><br>

1. **Graph Attention Networks** *Petar Veličković, Guillem Cucurull, Arantxa Casanova, Adriana Romero, Pietro Liò, Yoshua Bengio* [paper](https://arxiv.org/abs/1710.10903)
   
   - SMD: 
<br><br>

1. **How Attentive are Graph Attention Networks?** *Shaked Brody, Uri Alon, Eran Yahav* [paper](https://arxiv.org/abs/2105.14491)
   
   - SMD: 
<br><br>

1. **Masked Label Prediction: Unified Message Passing Model for Semi-Supervised Classification** *Yunsheng Shi, Zhengjie Huang, Shikun Feng, Hui Zhong, Wenjin Wang, Yu Sun* [paper](https://arxiv.org/abs/2009.03509)
   
   - SMD: 
<br><br>

1. **Attention-based Graph Neural Network for Semi-supervised Learning** *Kiran K. Thekumparampil, Chong Wang, Sewoong Oh, Li-Jia Li* [paper](https://arxiv.org/abs/1803.03735)
   
   - SMD: 
<br><br>

<details><summary> more </summary> 

1. **** ** [paper]()
   
   - SMD: 
<br><br>

1. **** ** [paper]()
   
   - SMD: 
<br><br>

1. **** ** [paper]()
   
   - SMD: 
<br><br>

1. **** ** [paper]()
   
   - SMD: 
<br><br>

1. **** ** [paper]()
   
   - SMD: 
<br><br>

1. **** ** [paper]()
   
   - SMD: 
<br><br>

1. **** ** [paper]()
   
   - SMD: 
<br><br>

</details>



## [Natural Language Processing ](#content)

### [Text Classification ](#content)

#### Datasets & Bench Marks
1. [Text Classification](https://paperswithcode.com/task/text-classification)
1. [Text Classification on 20NEWS](https://paperswithcode.com/sota/text-classification-on-20news)
1. [Text Classification on R8](https://paperswithcode.com/sota/text-classification-on-r8)
1. [Text Classification on MR](https://paperswithcode.com/sota/text-classification-on-mr)
1. [Text Classification on R52](https://paperswithcode.com/sota/text-classification-on-r52)
1. [Text Classification on Ohsumed](https://paperswithcode.com/sota/text-classification-on-ohsumed)
#### Papers
The following papers are from the GNN field only. However, there are some datasets that GNNs are dominated by other algorithms. It is possible to include GNNs in those algorithms and get better combinations.
1. **Graph Convolutional Networks for Text Classification**  *Liang Yao, Chengsheng Mao, Yuan Luo.* [paper](https://arxiv.org/abs/1809.05679) (TextGCN)
   
    - SMD: GCN implementation with Adjacency matrix entries are predefined with TF-IDF and PPMI scores. No solution provided for iterartive updates for newly incoming data. Transductive approach.
    - Future Work:
<br><br>

1. **BertGCN: Transductive Text Classification by Combining GCN and BERT**  *Yuxiao Lin, Yuxian Meng, Xiaofei Sun, Qinghong Han, Kun Kuang, Jiwei Li, Fei Wu.* [paper](https://arxiv.org/abs/2105.05727) (BertGCN,RobertaGCN)
   
    - SMD: BertGCN constructs a heterogeneous graph over the dataset and represents initial document as nodes using BERT representations. Jointly trains BERT and GCN modules. Learns representation for both training adata and unlabeled test data. Finally, BERT and GCN results are interpolated with trainable trade-off coefficient to obtain final representation. Transductive approach. 
    - Future Work: In this work, they only use document statistics to build the graph, which might be sub-optimal compared to models that are able to automatically construct edges between nodes. We leave this in future work.
<br><br>

1. **Every Document Owns Its Structure: Inductive Text Classification via Graph Neural Networks**  *Yufeng Zhang, Xueli Yu, Zeyu Cui, Shu Wu, Zhongzhen Wen, Liang Wang.* [paper](https://arxiv.org/abs/2004.13826) (TextING)
   
    - SMD:
    - Future Work: 
<br><br>

1. **Simple Spectral Graph Convolution**  *Hao Zhu, Piotr Koniusz.* [paper](https://openreview.net/forum?id=CYO5T-YjWZV) (SSGC)
   
    - SMD:
    - Future Work: 
<br><br>

1. ****  *.* [paper]() ()
   
    - SMD:
    - Future Work: 
<br><br>

1. ****  *.* [paper]() ()
   
    - SMD:
    - Future Work: 
<br><br>

1. ****  *.* [paper]() ()
   
    - SMD:
    - Future Work: 
<br><br>

1. ****  *.* [paper]() ()
   
    - SMD:
    - Future Work: 
<br><br>

1. ****  *.* [paper]() ()
   
    - SMD:
    - Future Work: 
<br><br>

1. ****  *.* [paper]() ()
   
    - SMD:
    - Future Work: 
<br><br>

### [Question Answering](#content)

