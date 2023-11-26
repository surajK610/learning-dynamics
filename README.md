# transformer-curvature

If running this code in the Oscar (SLURM), first run `./scripts/env_setup.sh` to generate the virtual environment. Running `source ./scripts/load_env.sh` loads necessary modules and the virtual environment.

## Dataset Creation/Experiment Running

To run experiments, please specify parameters and make changes in the `*.yaml` files in `configs/` and then run the python script with the dataset name. 
To run batches of experiments, please modifyl `pipeline.sh` or `slurm_pipeline.sh` if you have a slurm environment.

```bash
# Sets up folders.
setup.sh 

# Create dataset.
sbatch configs/datasets/pipeline.sh
sbatch configs/experiments/pipeline.sh
```

| Model                       | CoNLL2003 NER | CoNLL2003 CPOS | CoNLL2003 FPOS | OntoNotes NER | en_ewt-ud DEP | en_ewt-ud CPOS | en_ewt-ud FPOS | ptb_3 DEPTH | ptb_3 DISTANCE |
|-----------------------------|---------------|----------------|----------------|---------------|---------------|----------------|----------------|-------------|----------------|
| bert-base-cased (Layer 7)   |     0.96      |   0.87         |      0.88      |    0.96      |     0.85      |         0.95     |        .95      |(0.8776, 0.8585)|(0.8015, 0.8342)|
