# README
## Language Model Sampler
This script is a language model sampler that generates text using various sampling techniques. It uses n-gram models and supports add-one smoothing. 
## The supported sampling methods are:

Greedy
Beam search
Temperature sampling
Top-K sampling
Top-P sampling
### Usage
 First, create the language model using run_match_language_models. This function takes a folder containing a collection of text files in .csv format, one per language. It returns a dictionary containing the n-gram models for each language.

 Define the test_ dictionary, where you can specify various examples with different start tokens, sampling methods, generation lengths, and stop tokens.

 Call generate_string to generate text for each example in the test_ dictionary. This function takes the following parameters:

all_models: The n-gram models created in step 1.
prefix: The start tokens for the generation.
sampling_method: The sampling method to use.
gen_length: The length of the generated text.
stop_token: The token that stops the generation.
num_beams: The number of beams to keep (only relevant for beam search).
add_one: A boolean flag indicating whether to use add-one smoothing.
The generated text for each example will be stored in the generation field of the test_ dictionary. You can print the generated text and analyze the results.

## Dependencies
This script requires the following Python packages:

#### numpy
#### pandas
#### random
Make sure to have them installed before running the script.