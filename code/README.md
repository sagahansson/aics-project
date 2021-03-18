# Code

The code in the submodule [hate speech detection](https://github.com/sagahansson/hate-speech-detection/tree/ffb0970eb5e207d7e8d384dc872bc93095a23109) has been updated to enable running from the commandline as follows (with redudant arguments for the purpose of explaining):

`$ python train.py 100 -HS 50 -E 100 -BS 25 -B 0 -T 0 --img 1 --txt 1 --lr 0.001 --cpt False --dev 0` 

where `100` is the name of the file (the only positional argument, all others have default values), 
`-HS 50` is the hidden size of the perceptron (default: 20), 
`-E 100` is the number of epochs to train for (default: 40),
`-BS 25` is the batch size (default: 50),
`-B 0` is whether or not to use balanced data (either 0 : no, or 1 : yes; default: 1),
`-T 0` is whether or not to test (either 0 : no, only train, or 1 : yes, only test; default: 0),
`--img 1` is whether or not to use the image representation (either 0 : no, or 1 : yes; default: 1), 
`--txt 1` is whether or not to use the text representation (either 0 : no, or 1 : yes; default: 1), 
`--lr 0.001` is the learning rate of the model (default: 0.001),
`--cpt False` is whether or not to start from checkpoint (either True or False; default: False),
`--dev 0` is the cuda device to run the model on (either 0, 1, 2 or 3 (at some point we had 4 GPUs); default: 1).