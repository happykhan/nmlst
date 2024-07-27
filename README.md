# nmlt  

## Overview

nmlst is a powerful and efficient bioinformatics tool designed to perform Multi-Locus Sequence Typing (MLST) using the popular Minimap2 alignment software. MLST is a technique used to characterize bacterial species by analyzing the sequences of internal fragments of multiple housekeeping genes. nmlst leverages the speed and accuracy of Minimap2 to align sequences and assign MLST types, making it an invaluable tool for microbial genomics research.

## Features

- **Fast and Accurate Alignment:** Utilizes Minimap2 for rapid and precise sequence alignment.
- **Automated MLST Assignment:** Automatically assigns MLST types based on the aligned sequences.
- **Customizable Gene Schemes:** Supports various MLST schemes and allows users to input custom gene sets.
- **Comprehensive Output:** Generates detailed reports with MLST types, allele sequences, and alignment statistics.
- **User-friendly Interface:** Command-line interface designed for ease of use by researchers and bioinformaticians.

## Installation

### Prerequisites

Before installing , ensure that you have the following dependencies installed:

- Python 3.6 or higher
- Minimap2
- Biopython

### Installing nmlst

You can install nmlst using pip:

```bash
pip install nmlst
```

Alternatively, you can clone the repository and install it manually:

```bash
git clone https://github.com/yourusername/nmlst.git
cd nmlst
pip install .
```

## Usage

nmlst is designed to be simple and intuitive to use. The following example demonstrates how to run nmlst on a set of input sequences.

### Basic Usage

```bash
nmlst -i input_sequences.fasta -o output_directory -d mlst_database -m minimap2_path
```

### Command-line Options

- `-i, --input`: Path to the input FASTA file containing the sequences to be typed.
- `-o, --output`: Directory where the output files will be saved.
- `-d, --database`: Path to the MLST database containing allele sequences and profiles.
- `-m, --minimap2`: Path to the Minimap2 executable.
- `-s, --scheme`: (Optional) Name of the MLST scheme to use (default: `scheme1`).
- `-t, --threads`: (Optional) Number of threads to use for alignment (default: 1).

### Example

```bash
nmlst -i samples.fasta -o results -d /path/to/mlst_db -m /usr/local/bin/minimap2 -s scheme1 -t 4
```

## Output

nmlst generates several output files in the specified output directory:

- `mlst_results.txt`: A summary file containing the MLST type assignments for each input sequence.
- `alleles.fasta`: FASTA file of the allele sequences for each housekeeping gene.
- `alignment_stats.txt`: Detailed statistics of the alignment process, including coverage and identity percentages.

## Contributing

We welcome contributions from the community! If you would like to contribute to nmlst, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with clear and concise messages.
4. Push your changes to your fork.
5. Submit a pull request to the main repository.

## License

nmlst is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

nmlst uses the following open-source tools and libraries:

- [Minimap2](https://github.com/lh3/minimap2): A versatile sequence alignment program.
- [Biopython](https://biopython.org/): A collection of tools for biological computation.

## Contact

For any questions or issues, please open an issue on GitHub or contact us at [your-email@example.com](mailto:your-email@example.com).

---

Thank you for using nmlst! We hope this tool accelerates your microbial genomics research and provides valuable insights into your data.
