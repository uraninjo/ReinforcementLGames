# ReinforcementLGames

I built a model that plays cartpole and space invaders using reinforcement learning. I trained cartpole 5k,7k,10k times. For better results you may want to train it more and more.

Also, some of the games can be trained by simply changing the name of the game...

There are two errors if you want to try it out in your computer.


## 1. AttributeError: module 'gym' has no attribute 'make' 
```
!pip install gym[atari]
!pip install gym[all]
```
Then restart kernel


## 2. AttributeError: 'Sequential' object has no attribute '_compile_time_distribution_strategy'
![1](https://user-images.githubusercontent.com/74925286/151668584-bf71c9d4-dd4c-48bd-b581-778b3d91c30c.png)

Go to marked directory, mine is
c:\Users\mehmu\PycharmProjects\github repo\ReinforcementLGames\gymgames\lib\site-packages\keras\engine\training_v1.py


Change this line same as second screenshoot

![Ekran görüntüsü 2022-01-29 175131](https://user-images.githubusercontent.com/74925286/151668602-7687021e-c337-4732-b265-1f097b3e8ac1.png)

![Ekran görüntüsü 2022-01-29 175201](https://user-images.githubusercontent.com/74925286/151668605-744d9856-85d8-4454-8a57-df5ada675c44.png)


## 3. TypeError: Argument `fetch` = <tf.Variable 'dense/kernel:0' shape=(4, 24) dtype=float32> has invalid type "ResourceVariable" must be a string or Tensor. (Can not convert a ResourceVariable into a Tensor or Operation.)

Before creating the model use
```
del model
```

