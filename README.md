## Chatbot conversation using LSTM nets

Through the use of Long Short-Term Memory (LSTM) Networks, we aim to model the English language as closely as possible, such that model created is able to generate coherent sequences of words, namely, sentences. To achieve this, every word is transformed into a feature vector, which is used as input. Its corresponding output is the next most probable word to follow. The network will learn these probabilities through the use of a large list of human-generated sentences, more specifically the novel "Twelve Short Mystery Stories” by Sapper (Ronald Standish) <sup>[1](#projgut)</sup>.<br><br>

<center><img src="docs/res/predict.gif" height=230></center>

<br>

## Running the Code

### Dependencies

* `Python 3.6.1`
* `Tensorflow 1.3.0`
* `Keras 2.1.2`
* `matplotlib 2.0.2`
* `numpy 1.12.1`

### Command-line Execution

Directory Path: `/src/scripts/`

* **Train the model**: `python train.py [-h] [-v] [--data DATA] [--epochs EPOCHS] [--temp TEMP] [--slen SLEN] [-win WIN]`

	Optional arguments:

	| | |
	|-------------|--------|
	|`-h`, `--help`|show help message and exit |
	|`-v`, `--version`|show program's version number and exit|
	|`--data DATA`|path to training data (default: `sample_data_short.txt`)|
	|`--epochs EPOCHS`|number of epochs to train for (default: 50)|
	|`--temp TEMP`|select temperature value for prediction diversity (default: 1.0)|
	|`--slen SLEN`|maximum length for a training sequence (default: 15)|
	|`-win WIN`|select sliding window for text iteration and data collection for training (default: 3)|
	
* **Make predictions:** `python predict.py [-h] [-v] [--data DATA] [--seed SEED] [--nwords NWORDS] [--temp TEMP] [--slen SLEN] [-win WIN]`
	
	Optional arguments:
	
	| | |
	|-------------|--------|
	|`-h`, `--help`|show help message and exit |
	|`-v`, `--version`|show program's version number and exit|
	|`--data DATA`|path to training data (default: `sample_data_short.txt`)|
	|`--seed SEED`|provide a word or sentence to seed the program with|
	|`--nwords NWORDS`|number of words to generate (default: 400)|
	|`--temp TEMP`|select temperature value for prediction diversity (default: 1.0)|
	|`--slen SLEN`|maximum length for a training sequence (default: 15)|
	|`-win WIN`|select sliding window for text iteration and data collection for training (default: 3)|
	
	
<br><hr>
<a name="projgut">1</a>: This novel is available on the [Project Gutenberg website](http://gutenberg.ca/index.html).

Thanks colab as life saver !!! :)
