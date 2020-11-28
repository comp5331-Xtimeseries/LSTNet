# LSTNet

### Paper

Modeling Long- and Short-Term Temporal Patterns with Deep Neural Networks.(https://arxiv.org/abs/1703.07015)

This repo is forked from and modified on the authors' repo: https://github.com/laiguokun/LSTNet

### Source file descriptions

`Dataset.py`: API for accessing 5 datasets

`main.py`: training logics for LSTNet

`utils.py`: helper functions to convert data to batches

`models/LSTNet.py`: the architecture of LSTNet

`Optim.py`: learning rate decay logics for SGD  (unchanged from the original authors code)
`
### How to run
Check the `save` folder for the trained models and their configurations

In summary, we ran 
``` 
python main.py --gpu 0 --data exchange_rate --save exchange_rate.pt --hidCNN 50 --hidRNN 50 --L1Loss False --output_fun None
python main.py --gpu 0 --data electricity --save elec.pt --output_fun Linear --horizon 24
python main.py --gpu 0 --data solar --save solar_AL.pt --hidSkip 10 --output_fun Linear
python main.py --gpu 0 --data traffic --save traffic.pt --hidSkip 10
python main.py --gpu 0 --data sp500 --save sp500.pt --window 60 --horizon 6 --skip 20 --CNN_kernel 6 --hidSkip 1
```
Check `main.py` for the usage of the arguments.

### Environment 
Linux

Python 3.6 and PyTorch 1.6.0

