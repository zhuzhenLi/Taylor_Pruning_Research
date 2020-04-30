
### This repository is the further research studies of Taylor Pruning based on: https://github.com/NVlabs/Taylor_pruning

---

### Adjustments: 
* Minor changes are made on the original code in order to succefully run the Taylor pruning. (commented)

* Also, because of the huge size limitation of Imagenet as the dataset, this Taylor Pruning has chosen CIFAR10 as data set. 

* Due to the limittaion of GPU memory, batch size = 128 is used here. 


### Experiments are conducted on a Titan Machine :
1. resnet50
* log files are located at :

``` 
https://github.com/zhuzhenLi/Taylor_Pruning_Research/tree/master/runs/resnet50/resnet50_prune72
``` 

2. googlenet 
* log files are located at :
``` 
https://github.com/zhuzhenLi/Taylor_Pruning_Research/tree/master/runs/googlenet
``` 

3. inception_v3 (not successfully run yet)
  * Trying to run: 
  
  ``` 
  python3 main.py --name=runs/inception_v3/ --dataset=CIFAR10 --lr=0.001 --lr-decay-every=5 \
  --momentum=0.9 --epochs=30 --batch-size=128 --pruning=True --seed=0 --model=inception_v3 \
  --mgpu=False --group_wd_coeff=1e-8 --wd=0.0 --tensorboard=True  --pruning-method=22 \
  --data=/data/cifar-10-batches-py/ --no_grad_clip=True 
  ```

  Will have error:  
  ``` 
  ImportError:  /usr/lib/x86_64-linux-gnu/libstdc++.so.6: version `GLIBCXX_3.4.22' not found  
  ``` 
  Needs to resolve




