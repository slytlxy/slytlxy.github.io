# Play around with Tensor2tensor

procedure followed:    
https://github.com/tensorflow/tensor2tensor

## About tensor2tensor

**Self-attention network**:    
From my rough understanding: refer to a current word, a self attention network would know which other words in the whole sequence it should focus on in order to make decision.    
Self attention learning model surpasses (lstm) rnn & cnn since it runs much faster for natral language problems.

## Play with built-in translation model en-ch

**model name**: translate_enzh_wmt32k (en-ch translation model)    
**batch size**: 2048    
**gpu**: 4x Tesla K40m

+ data generation with t2t-datagen
    - takes 66 mins to generate data OTZ
+ training process
    - costs 70-100s for every 100 steps
    - updates model & saves checkpoints for every 1000 steps
    - takes 18k steps for loss to drop down below 1

## What's next
time to grab some test data and play with testing process
