# NLG-diversity
Script to measure the diversity of NLG output.

## Requirements
- Python 3
- nltk 3.4.5

## Setup
This script requires the Punkt tokenizers from the NLTK.
You can obtain them by running `python get_started.py`,
or by starting up Python and running the following code:

```python
import nltk
nltk.download('punkt')
```

## Usage
For basic use with English data, please run `python diversity.py your_file.txt`. Other options are provided when you run `python diversity.py -h`:

```
usage: diversity.py [-h] [--language LANGUAGE] [--msttr_window MSTTR_WINDOW]
                    [--punctuation] [--output_vocab] [--case_sensitive]
                    [--repeat_MSTTR] [--num_repeats NUM_REPEATS]
                    filename

Script to compute diversity statistics for NLG output.

positional arguments:
  filename              File you want to analyse

optional arguments:
  -h, --help            show this help message and exit
  --language LANGUAGE   Any language that has a model in
                        nltk_data/tokenizers/punkt.
  --msttr_window MSTTR_WINDOW
                        Window size to compute the mean-segmental type-token
                        ratio.
  --punctuation         Include punctuation in the statistics.
  --output_vocab        Include vocabulary in the results file.
  --case_sensitive      Make the analysis case sensitive?
  --repeat_MSTTR        Carry out repeated MSTTR?
  --num_repeats NUM_REPEATS
                        Number of times to carry out repeated MSTTR.
```
## Supported languages
In principle, any language for which you have a Punkt tokenizer model. Here's a list of the languages supported by the NLTK out of the box:

* czech
* danish
* dutch
* english
* estonian
* finnish
* french
* german
* greek
* italian
* norwegian
* polish
* portuguese
* russian
* slovene
* spanish
* swedish
* turkish
