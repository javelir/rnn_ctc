# rnn_ctc

Recurrent Neural Network with Connectionist Temporal Classifical implemented in Theano. Includes a Toy training example.

## Usage

1) First generate some data using scribe
```sh
python3 scribe.py data.pkl
# Run with no arguments to see full usage
```
    This will output data.pkl

2) Run the actual recurrent neural net with connectionist temporal classification cost function as:
```sh
python3 rnn_ctc data.pkl [nHidden]
```

## Sample Output
```
Input  : 0 2 3 1 0 1 0 2 1 2   
 0¦    ██  ██ ██             ¦  
 1¦     ███  ███  ███        ¦  
 2¦    ████    ████  ████    ¦  
 3¦    █████                 ¦  

Predict: 0 2 3 1 0 1 0 2 1 2   
 0¦    █    ██ █▓            ¦  
 1¦       ██  █    ███       ¦  
 2¦     █       ▒██   ██▓    ¦  
 3¦      █                   ¦  
 4¦████                 ▒████¦  
```

## Credits


* Graves, Alex, et al. ["Connectionist temporal classification: labelling unsegmented sequence data with recurrent neural networks."](http://machinelearning.wustl.edu/mlpapers/paper_files/icml2006_GravesFGS06.pdf) ICML, 2006.

* Theano implementation of CTC by [Shawn Tan](https://github.com/shawntan/rnn-experiment/)
