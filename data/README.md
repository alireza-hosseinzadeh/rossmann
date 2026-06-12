# Data folder

Place the project datasets here before running the notebook.

Recommended layout:

```text
data/
├── raw/
│   ├── train.csv
│   ├── test.csv
│   ├── store.csv
│   ├── store_states.csv              # or the relevant store-to-state mapping file
│   └── weather_state_files/*.csv      # optional: state-level weather files
└── processed/
```

The raw data are not committed to the repository. This avoids uploading large files and respects the original data-source terms.

After downloading the data, check the file paths in `notebooks/Rossmann_Final.ipynb` and update them if necessary.
