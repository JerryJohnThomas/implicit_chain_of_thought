# Understandings 


## data 

1345 * 8193 || 84434  +  013450(8,57,790) + 0097884(85,65,894) + 00039261 #### 8,56,87,212

each number is reversed 
5431 * 3918

5431 * 8 = 43448
5431 * 1 * 10 = 54310
5431 * 9 * 100 = 48879 00 

this is how its added up

## important insights
* src_autoencoder is not even used anywhere
* only src is used 


## architecture - teacher 

* path - `src\models\teacher.py`
* we are literally only using 3 blocks along the diagonal in a 3*3 hidden states only that is concerning ...
* diagonal had the best results out of the 3

### Initial
* base_model - GPT2
* tokenizer 
* In summary, the Teacher model is a wrapper around a GPT-2 language model. It initializes the GPT-2 model, a layer normalization module, and a tokenizer.

### compute_positions_to_extract_per_layer
* 

### extract_states

* Find the boundaries between input and CoT, and CoT and output
* [input] first_sep_position [CoT] second_position [output] eos
* we find the seperation points
* generate the hidden states from GPT2
* first_sep_positions = get_sep_position(input_ids, self.tokenizer.eos_token_id, skip=0)
    * this is just find positions of || and #
* 
* 
* 

## scripts

* script1 
`python src\train_teacher.py --train_path data\4_by_4_mult\train.txt  --val_path data\4_by_4_mult\valid.txt --save_model train_models\4_by_4_mult\gpt2\teacher\`



## install
gpu -
`pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121`

took 1 hour to make it to 148/25250
and 1%





