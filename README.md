# Principled Comparisons for End-to-End Speech Recognition: Attention vs Hybrid at the 1000-hour Scale 

This repository lists the experiment implementations for the Matched Encoder and Equal Data comparisons of HMM/DNN and Attention-based ASR systems, and provides a full pairwise analysis PDF (the article includes the interesting parts of the table)


## Pairwise analysis table

See the file full-pairwise-analysis.pdf in this repository.

## Librispeech

The Librispeech experiments are implemented in the same repository.
To run, simply use the corresponding run.sh script.

[Link](https://github.com/aalto-speech/sb-libri-hmmdnn)

These experiments were run on the Aalto University Triton cluster.
Neural network training and inference was run on Nvidia V100 32GB GPUs.

## Finnish Parliament Train20

Since this data was used for the first phase of model development, the experiments have scattered over many repositories.
If there is a particular model you wish to replicate, and are not sure how to run it, please contact us, e.g. through an Issue or by email.
If you wish to simply see an example of the implementations for this paper, we suggest looking at Librispeech or Combined Finnish, as they are more compact examples.

The HMM/GMM implementation and the data preparation is in this repository:
[Link](https://github.com/aalto-speech/fin-parl-models). See the run.sh script.

The HMM/DNN implementations in SpeechBrain are here:
[Link](https://github.com/aalto-speech/sb-fin-parl-2015-2020-kevat). The preparations are done with scripts in local/ and the network training is done by running the different Python training scripts. For decoding, see local/chain-decode.sh

The AED implementations use this repository:
[Link](https://github.com/aalto-speech/sb-2015-2020-kevat_e2e). The preparation is done with scripts in local/ and the network training and decoding uses the different Python scripts. Note that the neural language models are also implemented here.

These experiments were run on the Aalto University Triton cluster.
Neural network training and inference was run on Nvidia V100 32GB GPUs.

## Combined Finnish

Both HMM/DNN systems and AED models are implemented in the same repository.
To run, simply use the corresponding run.sh scripts.

[Link](https://github.com/aalto-speech/fin-parl-lahjoita-puhetta-s5)

These experiments were run on the CSC (IT Center for Science, Finland) Puhti cluster.
Neural network training and inference was run on Nvidia V100 32GB GPUs.


## Analysis code

The analysis was initially performed interactively, using the Notebook in the following repository. The connected data (system text outputs and reference text) is currently not included in the repository, as the files are too large, but the data can be provided - contact us via email.

[Link](https://github.com/aalto-speech/attn-hmm-jrnl-analysis-notebook)

Later, as it became more clear what values we wanted to compute, we implemented scripts in the Librispeech repository under `local/make-analysis-line.py`, `local/rare_word_errors.py` and `local/make-edit-streak-figure.py` to compute the same analysis as above - you can find implementations
[there](https://github.com/aalto-speech/sb-libri-hmmdnn).




