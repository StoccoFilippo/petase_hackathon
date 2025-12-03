# Experimental assay datasets for benchmarking zero-shot models

In this folder you'll find 4 different csv files with columns: 

- `mutated_sequence`: the sequence to score 
- Experimental assay measurement: `Activity_cutinases`, `Activity_proteingym`, `Expression`, `Stability`. Depending on which dataset you are using. 

To use the notebook and calculate the spearman correlation between your predicted results and the ground truth: 

1. Download the .csv you are interested in anc calculate the log likelihoods of the models for the `mutated_sequence`.
2. Create a .csv file with at least 2 columns (mutated_sequence, and the experimental assay measurement you want to check).
3. Change the paths in the notebook and run the spearman correlation. Update the spearman leaderboard in the slack canvas in `#petase-tournament` with your spearman and method of choice. 

## ProteinGym datasets 
The datasets that have been found by searching ProteinGym datasets of enzymes that perform similar reactions to PETase: carboxylesterase-like and hydrolases: 

- `colab_datasets_Activity_proteingym.csv`
- `colab_datasets_Stability.csv`
- `colab_datasets_Expression.csv`

Being a collection of different enzymes, the spearman colab reports also the mean TMscore (`mean_qtmscore_petases`) of the enzymes when compared to Uniprot reviewed PETases (10 proteins) as a way to rank the protein similarity to PETase.

## Cutinases dataset 
Alternatively, we found a [publication](https://www.biorxiv.org/content/10.1101/2024.04.25.591214v1.full.pdf) with a very good dataset of some DMS and chimeras of cutinases and ancestral reconstructions, and some of them are reported to have PETase activity. 

- `colab_datasets_Activity_cutinases`

