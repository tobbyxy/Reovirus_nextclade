# Avian Reovirus Nextclade Datasets

This repository contains Nextclade datasets for all 10 segments of Avian Reovirus (ARV), enabling phylogenetic analysis and genotype classification of reovirus sequences.

## Dataset Attributes

| Attribute            | Value                                    |
| -------------------- | ---------------------------------------- |
| name                 | Constellation-based classification of avian reovirus in turkeys reveals shared virus origins among different meat-type farms, Hseuh et al., 2025 Vet Microbiol  |
| refName              | PV406034                              |
| refAccession         | PV406034.1                             |
| refProtein           | PV406034.1                             |

## Scope of this Dataset

This dataset is based on [Hseuh et al., 2025](https://doi.org/10.3389/fvets.2025.1648247) for defining reovirus genotypes.

## Available Datasets

This repository contains separate datasets for each of the 10 ARV segments:

### L Segments (Large)
- **L1**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/L1_dataset)
- **L2**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/L2_dataset)
- **L3**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/L3_dataset)

### M Segments (Medium)
- **M1**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/M1_dataset)
- **M2**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/M2_dataset)
- **M3**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/M3_dataset)

### S Segments (Small)
- **S1**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/S1_dataset)
- **S2**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/S2_dataset)
- **S3**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/S3_dataset)
- **S4**: [Nextclade Web Link](https://master.clades.nextstrain.org/?dataset-url=gh:tobbyxy/Reovirus_nextclade@main@/datasets/S4_dataset)

## Usage

### Using Nextclade Web

Click on any of the links above to load the dataset directly in Nextclade Web. Once loaded:
1. Upload your sequences (FASTA format) or click "Load example" to test with example sequences
2. Click "Run" to perform the analysis
3. View alignment, phylogenetic placement, mutations, and quality control metrics

### Using Nextclade CLI

```bash
# Install Nextclade (if not already installed)
# See: https://docs.nextstrain.org/projects/nextclade/en/stable/user/nextclade-cli.html

# Run analysis for L1 segment
nextclade run \
  your_sequences.fasta \
  --input-dataset datasets/L1_dataset \
  --output-all output/

# Or use directly from GitHub
nextclade dataset get \
  --name 'avian-reovirus/L1' \
  --output-dir 'data/avian-reovirus-L1'
```

## Dataset Structure

Each segment dataset contains:
- **Reference sequence** (FASTA format): Segment-specific reference genome
- **Genome annotation** (GFF3 format): Gene/protein annotations for translation
- **Phylogenetic tree** (Auspice JSON format): Reference tree with representative sequences
- **Configuration file** (pathogen.json): Nextclade-specific settings and QC parameters
- **Example sequences** (sequences.fasta): Sample sequences for testing
- **Documentation** (README.md, CHANGELOG.md): Dataset-specific information

## Segmented Virus Analysis

As a segmented virus, each ARV segment evolves independently and should be analyzed separately:
- Use the appropriate segment dataset for your sequences
- Analyze all 10 segments separately for complete genome characterization
- Compare phylogenetic placement across segments to identify reassortment events

## Citation

If you use these datasets in your research, please cite:

Hseuh et al. (2025). Constellation-based classification of avian reovirus in turkeys reveals shared virus origins among different meat-type farms. *Frontiers in Veterinary Science*. https://doi.org/10.3389/fvets.2025.1648247

## Authors and Contacts

**Maintainer**: [Tobi Aminu](mailto:osaminu@iastate.edu?subject=[Nextclade]%20ReovirusNomenclature)

For questions regarding the dataset, please contact the corresponding author of [Hseuh et al., 2025](https://doi.org/10.3389/fvets.2025.1648247).

## Contributing

Issues and suggestions for improvements are welcome. Please open an issue on this repository or contact the maintainer.

## License

These datasets are provided for research and educational purposes. Please refer to the original publication for data usage terms.

## Acknowledgments

- Dataset created using [Nextstrain](https://nextstrain.org/) and [Nextclade](https://clades.nextstrain.org/)
- Based on the dataset creation guide: https://github.com/nextstrain/nextclade_data/blob/master/docs/dataset-creation-guide.md
