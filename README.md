# Characterization of the Bougainvillea peruviana Plastid Genome

**Student:** Gedden D. Estrevillo

**Course / Section:** Cell and Molecular Biology, A

## Genome used
| Item | Details |
|---|---|
| Genus and species | *Bougainvillea peruviana* |
| Family | Nyctaginaceae |
| Accession | NC_049005.1 (RefSeq) |
| Identical GenBank record | MT407463.1 |
| Source link | https://www.ncbi.nlm.nih.gov/nuccore/NC_049005.1 |
| Date retrieved | September 30, 2026|
| Genome size | 154,465 bp |
| Topology | Circular |
| GC content | 36.49% (Galaxy) |

## How I got the genome
I searched NCBI Nucleotide for "Bougainvillea peruviana chloroplast complete genome" and picked the RefSeq record NC_049005.1. I downloaded the FASTA file and the full GenBank file from the record page using Send to > Complete Record > File.

## Galaxy analysis
- Galaxy server: usegalaxy.org (my own account)
- History name: Plastid_Bougainvillea_Estrevillo
- Dataset name: Bougainvillea_peruviana_NC_049005.1
- Tool used: Fasta Statistics

| Galaxy result | Value |
|---|---|
| Number of sequences | 1 |
| Length | 154,465 bp |
| GC content | 36.49% |
| Gaps / N bases | 0 |

The whole plastome is in one sequence record.

## Plastome summary
| Feature | Result |
|---|---|
| LSC | 85,563 bp |
| IRA | 25,426 bp |
| SSC | 18,050 bp |
| IRB | 25,426 bp |
| Total genes | 131 |
| Protein-coding genes | 86 |
| tRNA genes | 37 |
| rRNA genes | 8 |
| Pseudogenes | 0 annotated |

The genome has the usual LSC-IRA-SSC-IRB layout. Genes in the inverted repeats, such as rpl2, rpl23, ycf2 and the four rRNA genes, appear twice. Genes with introns include trnK-UUU, rps16, trnG-UCC, atpF, trnL-UAA, trnV-UAC and clpP. The gene rps12 is trans-spliced. The matK gene sits inside the trnK-UUU intron.

## Folder guide
- `data/` FASTA and GenBank files
- `results/` gene tables and summary
- `figures/` Galaxy screenshots
- `report/` final report

## How to repeat this analysis
1. Open the NCBI link above and download the FASTA and GenBank files.
2. Sign in to usegalaxy.org and make a new history.
3. Upload the FASTA, set the type to fasta, and run Fasta Statistics.
4. Count the gene types in NCBI Gene (filter by protein-coding, small RNAs, pseudogenes).
5. Find the region coordinates in the GenBank FEATURES section.

## References
- NCBI RefSeq NC_049005.1 and GenBank MT407463.1
- Liu G. and Lee S. Direct submission, Sun Yat-sen University
- Characterization of the complete chloroplast genome of ornamental plant, Bougainvillea peruviana (Nyctaginaceae). Mitochondrial DNA B, 2020. DOI: 10.1080/23802359.2020.1768948
