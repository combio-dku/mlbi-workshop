# Machine Learning and Bioinformatics Workshops

Hands-on workshop materials from the Machine Learning and Bioinformatics (MLBI) Lab at Dankook University. The collection covers machine learning, deep learning, biological data analysis, sequencing workflows, and single-cell RNA-seq analysis.

The materials are intended for undergraduate and graduate students and researchers. Workshop guides and notebook explanations are primarily in Korean, with English terminology and selected English sections.

## Workshops

Each workshop page provides prerequisites, an outline, and links to the corresponding notebooks in this repository.

| Workshop | Topics |
| --- | --- |
| [Machine Learning](Workshop/ML_workshop_2603.md) | DataFrames, visualization, statistics, dimensionality reduction, clustering, regression, classification, ROC/AUC, neural networks, CNNs, RNNs, and Transformer-based image reconstruction. Includes Genome-to-Field regression exercises. |
| [Bioinformatics](Workshop/BI_workshop_2602.md) | Whole-exome sequencing and variant analysis; short-read bulk RNA-seq alignment and quantification; PacBio long-read RNA-seq, transcript assembly, and isoform analysis. |
| [Biological Big Data Analysis — KOTHEA](Workshop/BioBigdata_workshop_2607.md) | Python/pandas, statistical analysis, drug-response prediction, cancer classification, neural networks, and molecular representation learning using CCLE/CTRPv2, CancerSEEK, TCGA-BRCA, and QM9 data. |
| [Single-Cell RNA-seq Analysis — KSBi-BIML](Workshop/SCODA_workshop_2509.md) | AnnData and Scanpy, exploration of SCODA results, cell-type annotation, CNV and ploidy, cell–cell interactions, marker discovery, gene set enrichment, and KEGG pathway visualization. |
| [Single-Cell RNA-seq Analysis — LAIDD](Workshop/SCODA_workshop_LAIDD_2507.md) | Scanpy fundamentals, SCODA case studies in breast cancer and ulcerative colitis, and KEGG pathway visualization for tissue microenvironment analysis and therapeutic target discovery. |

## Getting started

1. Choose a workshop above and review its prerequisites and exercise order.
2. Open a notebook from the workshop page. The links point to files in this repository's `Notebooks/` directory.
3. For **Google Colab**, download the notebook and upload it through **File → Open notebook → Upload**. Sign in with a Google account and connect to a runtime.
4. Run the notebook's setup and data-loading cells, then work through the exercises in order. Follow any notebook-specific instructions for the runtime, package versions, and input files.

For **local execution**, clone or download the repository and open the notebooks in JupyterLab or Jupyter Notebook. `Anaconda_environment_setting.md` contains Korean instructions for Anaconda, conda environments, and an R kernel. Most exercises use Python; the KEGG Pathview exercises use R. Dependencies vary by notebook, so use the setup instructions supplied with each exercise.

Basic Python knowledge is expected for the machine learning and biological big data workshops. Statistics and linear algebra are helpful. The bioinformatics and single-cell workshops also assume relevant biology or genomics background; familiarity with Linux shell commands is useful for sequencing workflows.

## Repository layout

```text
mlbi-workshop/
├── README.md
├── Anaconda_environment_setting.md
├── Workshop/       # Workshop guides and notebook links
├── Notebooks/      # Python and R practice notebooks
└── Docs/           # Supporting materials, including the KOTHEA preparation PDF
```

## Data and exercise dependencies

Many notebooks download example data through their setup cells or dataset utilities. Some require additional files, Google Drive access, or outputs from an earlier exercise. Check the data-loading section before starting; the repository does not bundle all required datasets.

- **Genome-to-Field regression:** The notebooks expect `g2f_2014_hybrid_data_clean.csv` and `g2f_2014_weather.csv` under `G2F_2014/` relative to the working directory. Supply these files or adjust `DATA_DIR` before running the exercises.
- **Biological big data, exercises 5A and 5B:** Run the model-saving cells in 5A before the Tiny SMILES-BERT portion of 5B. Exercise 5B uses the saved weights, vocabulary, and configuration from `outputs/tiny_smiles_bert_model`.
- **SCODA exercises:** Follow the notebook instructions to download preprocessed example data or load your own SCODA results. Keep any package version pins specified by the selected notebook.
- **Sequencing exercises:** Follow the notebook-specific installation and reference-data preparation steps for the required command-line bioinformatics tools.
