# research about universal sentence encoder

## subjective

  restore training process of USE for chn sentence encoding


## existing model problem (tested with tensorflow-hub sample code)

  the pre-trained model does not working for chn chars for similarity test


## approaches

  + transformer
    - time/memory complexity O(n^2)
  + deep averaging network (DAN)
    - time/memory complexity O(n)


## Future work

  + first try with DAN method
    - refer to paper (http://www.aclweb.org/anthology/P15-1162)                  
      - https://github.com/miyyer/dan *** <-- I am here ***
    - ~~check tensorflor-hub fine-tuning~~ (since its only one softmax on top of original model, wont help anything)     
    https://github.com/helloeve/universal-sentence-encoder-fine-tune     
