# _Treponema pallidum_ in early modern Europe

## Data

### Metadata

- [`treponema_metadata.csv`](https://github.com/laduplessis/Treponema_pallidum_in_early_modern_Europe/blob/master/data/treponema_metadata.csv): Metadata table with sampling locations and radiocarbon date ranges.

### Nichols reference

Alignments of genomes reconstructed by mapping to the TPA reference genome Nichols (CP004010.2). For each alingment the full alignment (`fullAlignment...`) as well as only the variable sites (`snpAlignment...`) are provided.

- `Nichols_reference/full/`: The full alignment with no sites removed.
- `Nichols_reference/norecomb/`: Alignment after excluding recombining genes and sites with too much missing data (>25%, >50%, >75% cutoffs). 
- `Nichols_reference/norecomb_nohypervariable/`: Alignment after excluding recombining and hypervariable genes as well as sites with >25% missing data.

### CDC2 reference

Alignments of genomes reconstructed by mapping to the TPE reference genome CDC2 (CP002365.1). For each alingment the full alignment (`fullAlignment...`) as well as only the variable sites (`snpAlignment...`) are provided.

- `CDC2_reference/norecomb_nohypervariable/`: Alignment after excluding recombining and hypervariable genes as well as sites with >25% missing data.