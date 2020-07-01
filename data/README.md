# Ancient bacterial genomes reveal a high diversity of _Treponema pallidum_ strains in early modern Europe**Kerttu Majander**, **Saskia Pfrengle**, Judith Neukamm, Arthur Kocher, Louis du Plessis, Marta Pla-Díaz, Natasha Arora, Gülfirde Akgül, Kati Salo, Rachel Schats, Sarah Inskip, Markku Oinonen, Heiki Valk, Martin Malve, Aivar Kriiska, Päivi Onkamo, Fernando González-Candelas, Denise Kühnert, **Johannes Krause**, **Verena J. Schuenemann**

---

## Molecular clock dating input data

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