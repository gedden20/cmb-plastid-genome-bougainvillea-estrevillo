# Plastid Genome Report: Bougainvillea peruviana

**Name:** Gedden D. Estrevillo

**Course / Section:** Cell and Molecular Biology, Section A

**Date:** October 1, 2026

## 1. Organism and genome
| Item | Answer |
|---|---|
| Scientific name | Bougainvillea peruviana |
| Family | Nyctaginaceae |
| Accession | NC_049005.1 (same sequence as MT407463.1) |
| Database | NCBI RefSeq |
| Genome size | 154,465 bp |

## 2. How I know it is a complete plastid genome
- The NCBI title says "chloroplast, complete genome" and the record says the assembly is full length.
- The organelle is listed as plastid:chloroplast and the topology is circular.
- In Galaxy, the genome came out as 1 sequence record with 154,465 bp and no gaps or N bases.
- It is not a barcode. The rbcL gene alone is only about 1.4 kb, but this record is over 154 kb and has 131 genes.
- It has photosynthesis genes (psa, psb, atp, pet, rbcL), plastid rRNA and tRNA genes, and the usual plastid layout. A nuclear sequence would not look like this.

## 3. Overall organization
| Region | Position | Size (bp) |
|---|---|---|
| LSC | 1..85,563 | 85,563 |
| IRA | 85,564..110,989 | 25,426 |
| SSC | 110,989..129,039 | 18,050 |
| IRB | 129,040..154,465 | 25,426 |

Yes, it has the common LSC-IR-SSC-IR layout. The four regions add up to the full 154,465 bp.

## 4. Gene content
| Type | Number |
|---|---|
| Total genes | 131 |
| Protein-coding | 86 |
| tRNA | 37 |
| rRNA | 8 |
| Pseudogenes | 0 annotated |

Genes in the inverted repeats show up twice because the two IR regions are copies of each other, so each gene in them is annotated two times. For example, all four rRNA genes have two entries, and rpl2, rpl23 and ycf2 are also in the IR. This means the total of 131 counts those genes twice.

## 5. Protein-coding genes from different groups
| Gene | Group | What it does |
|---|---|---|
| psbA | Photosystem II | Makes the D1 protein in the PSII reaction center |
| psaB | Photosystem I | Makes a core protein of photosystem I |
| atpA | ATP synthase | Alpha subunit of the enzyme that makes ATP |
| petA | Cytochrome b6f | Makes cytochrome f, used in electron transport |
| rbcL | Carbon fixation | Large subunit of Rubisco |
| rpoB | RNA polymerase | Beta subunit of the plastid RNA polymerase |
| rps16 | Ribosomal protein | Small ribosome subunit protein S16 |
| ndhF | NADH dehydrogenase | Part of the NAD(P)H dehydrogenase complex |
| clpP | Protease | Protease subunit that breaks down proteins |
| accD | Lipid synthesis | Beta subunit of acetyl-CoA carboxylase |
| matK | RNA processing | Maturase that helps splice introns |

## 6. RNA and RNA-processing features
**rRNA genes:** 16S, 23S, 4.5S and 5S rRNA. Each one is found twice, once in each IR.

**tRNA examples:** trnH-GUG (His), trnK-UUU (Lys), trnG-UCC (Gly), trnL-UAA (Leu), trnV-UAC (Val).

**Genes with introns** (I worked out the intron positions from the join() coordinates in the GenBank record):

| Gene | Intron size (bp) |
|---|---|
| trnK-UUU | 2,524 |
| rps16 | 869 |
| trnG-UCC | 704 |
| atpF | 752 |
| trnL-UAA | 537 |
| trnV-UAC | 605 |
| clpP | 633 and 752 (two introns) |

rps12 is trans-spliced, which means its exons are far apart in the genome and the RNA pieces get joined later. Also, matK is located inside the intron of trnK-UUU.

## 7. Unusual features
- No pseudogenes are annotated in this record.
- rps12 is trans-spliced.
- clpP has two introns.
- ycf1 sits across the junction between IRA and SSC.
- The record doesn't report any gene losses or rearrangements. I did not compare it with other species, so I can't say more than that.

## 8. GC content and other observations
The GC content is **36.49%** (from Galaxy).
1. The genome is AT-rich. A (48,567) and T (49,527) together are about 63.5% of the bases.
2. The two IR copies take up about a third of the genome (50,852 of 154,465 bp). Also, the Galaxy result shows no gaps or N bases, and the genome is one single record.

## 9. Plastid vs mitochondrial genome
**Five similarities**
1. Both came from bacteria that were engulfed by an ancestral cell (endosymbiosis).
2. Both have their own DNA, separate from the nucleus.
3. Both are in organelles with double membranes.
4. Both code for rRNAs, tRNAs and some proteins, but most of their proteins come from nuclear genes.
5. Both have many copies per cell and are mostly passed on by one parent, often the mother in flowering plants.

**Five differences**
1. The plastid genome is in the plastid (chloroplast) and the mitochondrial genome is in the mitochondrion.
2. The plastid genome supports photosynthesis, and the mitochondrial genome supports respiration.
3. Most plastid genomes are about 120 to 160 kb, but plant mitochondrial genomes vary a lot in size and are often much bigger.
4. Plastid genomes keep a stable structure (LSC-IR-SSC-IR). Plant mitochondrial genomes rearrange often and can exist in several pieces.
5. Plastid genomes carry more genes (131 here) than plant mitochondrial genomes, which often have around 50 to 60.

| Feature | Plastid genome | Mitochondrial genome |
|---|---|---|
| Cellular location | Plastid (chloroplast) | Mitochondrion |
| Main biological functions | Photosynthesis and other plastid work | Respiration and ATP production |
| Typical genome organization | Circular map with LSC, SSC and two IRs | Often many forms and sub-circles in plants |
| Relative genome size | Small and fairly constant | Varies a lot, often larger in plants |
| Gene content | Photosynthesis, ribosomal, RNA polymerase, tRNA and rRNA genes | Respiration, ribosomal, tRNA and rRNA genes |
| Copy number | Many copies per plastid, many plastids per cell | Many copies per cell, varies by tissue |
| Inheritance | Mostly maternal in flowering plants, but it varies | Mostly maternal in plants, but it varies |
| Recombination / structural change | Low, structure is stable | High, rearranges often |
| Mutation / substitution pattern | Slow, steady substitutions | Slow substitutions but fast structural change in plants |
| Common research applications | Phylogeny, barcoding, species ID | Used more in animals, less common in plants |

## 10. Why plastid genomes are useful
**Advantages compared with the nuclear genome**
- There are many copies per cell, so it is easy to get lots of DNA.
- It is small, so it can be assembled into one complete sequence.
- Gene content and order are well conserved, so it is easy to align between species.
- There is little recombination, so the genome is passed on as one block.
- It is usually inherited from one parent, so it tracks one lineage clearly.
- It avoids the problems of nuclear sex chromosomes. The X and Y (or Z and W) differ in copy number and recombination, but the plastid genome is the same in both sexes.
- Substitutions happen at a steady rate, which helps with phylogeny.
- Markers like rbcL and matK are already widely used to identify plants.

**Limitations**
- It is one locus with one inheritance pattern, so it only shows one lineage, usually the maternal one.
- It can't show gene flow through pollen or hybridization very well.
- It says little about most traits.
- Closely related species may not differ enough in plastid DNA to be separated.
- Plastid DNA can sometimes be found inside the nucleus, which can confuse results.

**Question for plastid data:** Which species are the closest relatives of Bougainvillea peruviana within Nyctaginaceae?

**Question for nuclear data:** Which genes control bract color in Bougainvillea?

## References
- NCBI RefSeq record: [NC_049005.1](https://www.ncbi.nlm.nih.gov/nuccore/NC_049005.1)
- NCBI GenBank record: [MT407463.1](https://www.ncbi.nlm.nih.gov/nuccore/MT407463.1)
- Galaxy: [usegalaxy.org](https://usegalaxy.org), Fasta Statistics tool
- Karp et al., Cell and Molecular Biology 
- Liu G. and Lee S. Characterization of the complete chloroplast genome of ornamental plant, Bougainvillea peruviana (Nyctaginaceae). Mitochondrial DNA B, 2020. [DOI: 10.1080/23802359.2020.1768948](https://doi.org/10.1080/23802359.2020.1768948)
