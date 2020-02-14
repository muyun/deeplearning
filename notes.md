### work notes

### deeplearning
 * This is mainly on deeplearning and its applications, especially in NLP and NLU.

 * Workflow to Approach a ML problem -> Prototype
   - what kind of question or goal we wanna answer

   - how to define and measure success -> like using a business metric like increased profit or decreased losses

   -  acquire the data and build a working prototype - a loop [TODO]
      + analyze the mistakes
      + collect more or diff data
      + change the task formulation slightly
   - humans in the loop
      + algotithm might increase response time or reduce cost
      + TODO
   
* From Prototype to Production
  - data analytics teams
  - production teams -> reimplement the solution for robust, scalable system

     + line evaluation
     + online testing using A/B testing [TODO]


#### A Use Case in Intelligent Configurations Design
#####  Descrption 
Online product configurations are prevailing tools in e-commerce industry to elicit customer needs. Yet current online configurations require customers to specify the choices of each product attribute, which poses a great challenge for customers with no background knowledge.

Hence, this project aims to develop a new online product configuration approach which enables customers to configure a product just by specifying their functional requirements, instead of the detailed design parameters.

For example, when users input the keywords like “a large Screen Size laptop“, our approach could map the associated features and and give high quality recommendations <small>(Fig.1: Our approach to predicting the attributes based on the input “A large Screen Size laptop”)<small>.


![Fig.1](https://github.com/muyun/dev.deeplearning/blob/master/nsrc/icon_demo.png) 

##### Solution
We develop tools to extract Amazon user review (laptop) data (suppose these reviews as user inputs). Then we build **Deep learning Models** to do the query-to-attributes mapping [map user inputs (the functional requirements in unstructured query) into product parameters or features (structured attributes)].



##### Presentations from me about deep learning technology and its application

* [Collect data as Dataset](https://docs.google.com/presentation/d/1Y7zrC9QLHHcFlQpn3Yb2_paOgU_xB1B4yJwjM6ah98E/edit?usp=sharing)
* [Algorithm: word embeddings based mapping](https://docs.google.com/presentation/d/1XpAfL3T-A0cxyRjVbmZFE2M8jsFQrwycfGX042OSP18/edit?usp=sharing)
* [Algorithm: Support Vector Machine on word-embedding](https://docs.google.com/presentation/d/1GoGhYoFfq1Ha2MoseFj5KcWrzu0IISQ2/edit#slide=id.p1)
* [Convolutional Neural Network for Sentence Classification](https://docs.google.com/presentation/d/1w8Qw0U5P9FVhO8-4WYMb0-foUYG47CBE/edit#slide=id.p1)
* [The experiments based on Convolutional Neural Network](https://docs.google.com/presentation/d/1JKskq_ufcVFyvbG0yfBc1aRl0PLv39ak/edit#slide=id.p1)
* [Algorithm: Recurrent Neural Network](https://docs.google.com/presentation/d/1UG5GBp7PH-8pOlXFw_jMKGQQpUtEe2xV/edit#slide=id.p1)
* [Algorithm: Long short-term memory Network](https://docs.google.com/presentation/d/1f-5p59g9NrMlYHkhjagAYe7OO-23P-R-/edit#slide=id.p1)
* [Algorithm: Hier-attention Network](https://docs.google.com/presentation/d/1MWM-tzy_I7I-MWqkIF3u9KodEKW3K2Tb/edit#slide=id.p1)
* [Top-N Sort Algorithm](https://docs.google.com/presentation/d/1kpzEqbFUUvQ3dsSITs5C8ifK0VfOyAB0/edit#slide=id.p1)
* [TOP-N Algorithm on word embeddings](https://docs.google.com/presentation/d/1kpzEqbFUUvQ3dsSITs5C8ifK0VfOyAB0/edit#slide=id.p1)


#### Notes on deep learning
 * ch2 
   - 通过**与非门**的组合可以实现计算机 ? [The elements of computing systems](http://www1.idc.ac.il/tecs/plan.html) 
   - 与非门可以使用感知机实现 => 通过感知机的组合可以表示计算机  
   - 
   - 两层感知机就能构建计算机， 因为两层感知机可以表示任意函数   

 * ch3 
   - 神经网络可以**自动地从数据中学习到合适的权重参数** 
   - 激活函数 必须使用 非线性函数 
   - **batch 批处理** 可以缩短处理时间 
     + 因为数值计算的库都能够高效处理大型数组运算的最优化
     + 批处理一次性计算大型数组要比分开速度更快 - **数据传送**成为瓶颈 

 * ch4 
   - 由人来驱动 - 人来设计算法解决问题，
   - 数据驱动 - 机器学习是由机器**从收集到的数据中找出规律** -> 模型/算法 
   - 
   - 选 mini-batch -> 计算mini-batch的损失函数的值 - 梯度 -> 更新参数 <- loop 
   - 从训练数据中随机选出一部分数据 - mini-batch - 目标是减少mini-batch的损失函数的值 
     + 神经网络 **以损失函数为指标** 寻找最优权重参数 
     +  
     + 如果以识别精度作为指标，参数的导数在绝大多数地方都会变成0 
       - 识别精度**对微小的参数变化**基本上没有什么反应， 它的值是不连续，突然地 变化 

   - **梯度法** - 以梯度的信息为线索，决定前进的方向 
   - **学习率** 由人工设定 - 在一次学习中，在多大程度上更新参数 


#### reference




#### 2019-04-10 
* TODO - crawl amazon data from 2016 year 

#### 2019-03-29 
* check the parameters 
  - epoch 
  - batch size 

* running log:
Train on 1075 samples, validate on 269 samples
Epoch 1/9
1075/1075 [==============================] - 4s 4ms/step - loss: 0.7636 - acc: 0.8000 - val_loss: 4.1915 - val_acc: 0.1190
Epoch 2/9
1075/1075 [==============================] - 4s 4ms/step - loss: 0.7202 - acc: 0.8009 - val_loss: 4.0211 - val_acc: 0.1301
Epoch 3/9
1075/1075 [==============================] - 4s 4ms/step - loss: 0.6551 - acc: 0.8437 - val_loss: 4.1592 - val_acc: 0.1450
Epoch 4/9
1075/1075 [==============================] - 4s 4ms/step - loss: 0.5603 - acc: 0.8595 - val_loss: 4.3268 - val_acc: 0.1152
Epoch 5/9
1075/1075 [==============================] - 4s 4ms/step - loss: 0.5028 - acc: 0.8819 - val_loss: 4.4902 - val_acc: 0.1152
Epoch 6/9
1075/1075 [==============================] - 5s 4ms/step - loss: 0.4611 - acc: 0.8856 - val_loss: 4.5951 - val_acc: 0.1078
Epoch 7/9
1075/1075 [==============================] - 5s 4ms/step - loss: 0.4106 - acc: 0.8977 - val_loss: 4.5893 - val_acc: 0.1190
Epoch 8/9
1075/1075 [==============================] - 5s 4ms/step - loss: 0.4193 - acc: 0.8940 - val_loss: 4.6872 - val_acc: 0.1264
Epoch 9/9
1075/1075 [==============================] - 5s 4ms/step - loss: 0.4081 - acc: 0.9005 - val_loss: 4.6695 - val_acc: 0.1227

y_proba:  [[ 2 58 26 ... 44 56 42]
 [34  4 12 ... 40 48 22]
 [58 26 19 ... 44 56 42]
 ...
 [33 43 34 ... 37 36  5]
 [ 2 58 25 ...  9 56 42]
 [10 25  8 ... 11  9 22]]
precision:
0.359375
0.3098958333333333
0.2864583333333333
0.2604166666666667
0.24479166666666666
recall:
0.3645833333333333
0.5885416666666666
0.6822916666666666
0.7552083333333334
0.8020833333333334

#### 2019-01-11 
  * TODO
     - Feedforward neural network and backprop
     - Computation graphs and modules
     - Autograd in ML


#### 2019-01-10 
  * todo
    - using the labeld data
    - improve the precisions based on range inds
    - GAN

  * how to improve performances in machine learning
    - add more data 
    - model complexity -> too complex or not enough
    - feature space -> right set of features - the scale of features or more new features
    - change the model -> model is in general not a good fit for the use case

  * biase-variance tradeoff ?
    - todo 

  
  * system
    - jug to manage computations to use multiple cores or multiple machines
    - AWS E2
    - StarCluster

#### 2019-01-03 
 * metrics - Discounted cumulative gain in information retrieval

#### Notes on deep learning
 * ch2 
   - 通过**与非门**的组合可以实现计算机 ? [The elements of computing systems](http://www1.idc.ac.il/tecs/plan.html) 
   - 与非门可以使用感知机实现 => 通过感知机的组合可以表示计算机  
   - 
   - 两层感知机就能构建计算机， 因为两层感知机可以表示任意函数   

 * ch3 
   - 神经网络可以**自动地从数据中学习到合适的权重参数** 
   - 激活函数 必须使用 非线性函数 
   - **batch 批处理** 可以缩短处理时间 
     + 因为数值计算的库都能够高效处理大型数组运算的最优化
     + 批处理一次性计算大型数组要比分开速度更快 - 数据传送成为瓶颈 

 * ch4 
   - 由人来驱动 - 人来设计算法解决问题，
   - 数据驱动 - 机器学习是由机器**从收集到的数据中找出规律** ->算法 
   - 
   - 选 mini-batch -> 计算mini-batch的损失函数的值 - 梯度 -> 更新参数 <- loop 
   - 从训练数据中随机选出一部分数据 - mini-batch - 目标是减少mini-batch的损失函数的值 
     + 神经网络 **以损失函数为指标** 寻找最优权重参数 
   - 
   - 以识别精度作为指标，参数的导数在绝大多数地方都会变成0
     + 识别精度**对微小的参数变化**基本上没有什么反应， 它的值是不连续，突然地 变化 

   - **梯度法** - 以梯度的信息为线索，决定前进的方向 
   - **学习率** 由人工设定 - 在一次学习中，在多大程度上更新参数 


#### 2018-12-18 
 * top-N alg
   - top-N multi-classifier

#### 2018-11-01 
 * todo 
   - RNN-LSTM ?
 * 

#### 2018-10-11 
 * summary
  - 
 * todo 
  - pre-processing 
  - 

#### 2018-10-08 
 * summary
  - flipkart
  Num of brands in Flipkart: %d: 408
  Num of reviews: %d: 32434 - 32k
  Num of words: %d: 1171703 - 1.17M

  - HP
  Num of brands in HP: %d: 59
  Num of reviews: %d: 950 - 1k
  Num of words: %d: 78173 - 18k

#### 2018-10-05
 * flipkart
  - 408 brands

#### data 
 * HP
  - class="bv-content-container"

#### 2018-09-07 
 * ch6 
  - 最优化 -> 神经网络学习的目的是找到使损失函数的值尽可能小的参数 

  - 权重的初始值 - 权值衰减 -> 减少权重参数的值可以抑制过拟合的发生  ？

  - 


 * more correct labels,  lower metrics 

 * experiments on cpu 

1. Shape of data tensor: (7227, 108)
[[   0    0   10    0]
 [   0   26   12    1]
 [   3    3 1207   20]
 [   0    0   41  122]]
0.9377162629757786
             precision    recall  f1-score   support

          0       0.00      0.00      0.00        10
          1       0.90      0.67      0.76        39
          2       0.95      0.98      0.96      1233
          3       0.85      0.75      0.80       163

avg / total       0.93      0.94      0.93      1445


2. Classify ...
[[   0    0   10    0    0]
 [   0   28   10    1    0]
 [   1   13 1200   16    3]
 [   0    0   39  124    0]
 [   0    0    0    0    0]]
0.9356401384083045
/usr/local/tensorflow/lib/python3.6/site-packages/sklearn/metrics/classification.py:1137: UndefinedMetricWarning: Recall and F-score are ill-defined and being set to 0.0 in labels with no true samples.
  'recall', 'true', average, warn_for)
             precision    recall  f1-score   support

          0       0.00      0.00      0.00        10
          1       0.68      0.72      0.70        39
          2       0.95      0.97      0.96      1233
          3       0.88      0.76      0.82       163
          4       0.00      0.00      0.00         0

avg / total       0.93      0.94      0.93      1445


#### 2018-09-07 

##### ch5 
 * deep learning
   random mini-batch -> W's gradients -> update W -> repeat


 * why to use loss function in deep learning ? 
   - 

 * backward alg could compute gradients effectively 
   - 数值微分耗时 -> 确认BP的实现是否正确 

 * TODO - the code



#### 2018-08-30 
a fast pc -> 2.16 GHz Intel Celeron -> latop


#### 2018-08-24 
  * modify the classifier

  * remove Punctuation 
    - todo: stemming
    - -> acc: 0.4738 - precision: 0.2292 - recall: 0.0311
      -> acc: 0.4743 - precision: 0.2507 - recall: 0.0301


#### 2018-08-22 
 * re-code SWEM-max 
   - L patch ?

 * re-code SWEM-aver + SWEM-conct 
 *  

#### 2018-08-15 
 * SWEM alg improvements

#### 2018-08-06
 * some about SWEM

 * need to learn PyTorch on fast.ai


 * Some on Keras
   - 符号计算 - 计算图
   - Model - 
   - batch - batch_size -> mini-batch gradient descent 
   - epochs


#### 2018-08-03
  * use Pandas lib for data

  * todo
    - PyTorch


#### 2018-08-01
  * research
    - 学会找出研究人员和论文的基本出发点 - motivation

  * Pandas

  * todo:
    - Latex
    - data Visualisation


#### 2018-07-18 
 * result

Found 838332 reviews.
Found 21616 unique tokens.
Shape of data tensor: (838332, 300)
Shape of label tensor: (838332, 6)

SWEM-aver:

Layer (type)                 Output Shape              Param #
=================================================================
input_1 (InputLayer)         (None, 300)               0
_________________________________________________________________
embedding_1 (Embedding)      (None, 300, 100)          2000000
_________________________________________________________________
lambda_1 (Lambda)            (None, 100)               0
_________________________________________________________________
dense_1 (Dense)              (None, 6)                 606
=================================================================
Total params: 2,000,606
Trainable params: 606
Non-trainable params: 2,000,000
_________________________________________________________________
None
Train on 528149 samples, validate on 58684 samples


#### 2018-07-17 
 * work harder

 * problem fix:
  - export LD_LIBRARY_PATH=LD_LIBRARY_PATH:/usr/local/cuda-9.0/lib64/
 

#### 2018-07-13  
 * 精力问题 

#### 2018-07-12  
 * 

#### 2018-07-11
 * notes on the server
   - source /usr/local/tensorflow/bin/activate
   - GPU: export CUDA_VISIBLE_DEVICES=0
   - check gpu process : nvidiva-smi


#### 2018-07-09 
 * reproduce the paper



#### 2018-05-31
  * read the paper - "predicting latent structured intents from shopping queries"     - MLP
    - LSTM/RNN
    - CNN
    
  * claw the review data - "small" subsets  
  * run basic word2vec on TF  

#### 2018-05-30
  * word embedding
    + data normalization  
      - lemmatization and word stem ?  
      
    + document vectorization  
      - count vectorizer and TF-IDF vectorizer  
      - word2vec <- could care about the order (word context) -> semantic  
        -> we get the similar vectors for the words  
        
    + 


#### 2018-05-29
  * setup google cloud <http://cs231n.github.io/gce-tutorial/>
  
  * NN algorithms
  
  * the server: 10.237.4.253 raymond/raymond

#### meetup with Dr. Wang on 28/05/2018
* about tensorflow [1]:
    + Setup the env about python and tensorflow
    + now a simple tensorflow could be run in locally -> see the github [4] 
    
    + plan (todo):
        - run a basic mode like linear regression in tensorflow
        - then run word2vec in tensorflow, or try to run it on server
    
* about word embedding [2][3]:
    +  the basic applied machine learning knowledge:  like loss functions, bag of words, features, bag of vectors 
       - if there is something wrong, if we could know the principle/theory, we could know the reason and correct it quickly
 
    + plan (todo):
       - know more about ML, especially deep learning (like word embedding part) based on the reference 2 and 3

* Others
   + the github for the code
   + the fixed meetting time


#### 2018-05-24
  * setup the env on python and tensorflow on mac
  * TODO: 
    - setup the env on windows


#### virtualenvwrapper -> export WORKON_HOME=$HOME/.env

  * For some project 
> cd dev.dplearning  

  * create an env 
> <del>mkvirtualenv tfenv -> including the Python executable files, and a copy of the pip lib  </del>  
> python3 -m venv ~/.env/isightenv 
> 
  * use the env
> workon tfenv  -> using the virtual env  
> pip install * 

  * deactivate 
> deactivate -> deactivate the env  
> rmvirtualenv venv

> 
> pip freeze > requirements.txt 

> pip install -r requirements.txt

#### reference
* [Pipenv & Virtual Environments](http://docs.python-guide.org/en/latest/dev/virtualenvs/#lower-level-virtualenv)
