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
- ycf1 is found at both SSC-IR junctions. The long copy (124774..130410) crosses the SSC-IRB junction, and a shorter copy (109619..110992) sits at the IRA-SSC junction.
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
5. Both have several copies of their DNA in each organelle, and the DNA is usually circular (Karp).

**Five differences**
1. The plastid genome is in the plastid (chloroplast) and the mitochondrial genome is in the mitochondrion.
2. The plastid genome supports photosynthesis, and the mitochondrial genome supports respiration.
3. Plastid genomes carry many more genes. Karp says chloroplast DNA has about 60 to 200 genes, and mine has 131. Human mtDNA has only 37 (13 proteins, 2 rRNAs and 22 tRNAs).
4. They use different RNA polymerases. The plastid uses a bacterial-type polymerase, and my genome carries rpoB, rpoC1 and rpoC2. The mitochondrial polymerase is a single-subunit enzyme related to bacteriophage enzymes (Karp).
5. Their mutation patterns differ. Human mtDNA mutates more than 10 times faster than nuclear DNA (Karp), but plant mitochondrial coding sequences change very slowly even though their structure rearranges a lot.  

| Feature | Plastid genome | Mitochondrial genome |
|---|---|---|
| Cellular location | Stroma of the chloroplast | Matrix of the mitochondrion |
| Main biological functions | Photosynthesis (Karp) | Oxidative energy metabolism and ATP formation (Karp) |
| Typical genome organization | Small, double-stranded, circular DNA (Karp). Mine has the LSC-IRA-SSC-IRB layout. | Circular in higher plants and animals (Karp). In plants it can also exist as a mix of linear, circular and branched forms (Biochimie review). |
| Relative genome size | Highly conserved in size (Solanum paper). Mine is 154,465 bp. | Animals about 15-17 kb. Plants are much larger and vary a lot, up to 11.7 Mb in Larix. |
| Gene content | About 60 to 200 genes (Karp). Mine has 131. | Human: 13 proteins, 2 rRNAs, 22 tRNAs (Karp) |
| Copy number | Usually high copy number (Solanum paper) | Many copies per cell (Karp) |
| Inheritance | Usually maternal in plants (Solanum paper) | Maternal in humans (Karp), usually maternal in plants (Solanum paper) |
| Recombination / structural change | Conserved structure. Recombination between short repeats is kept in check by proteins such as RECG (moss study). | Frequent recombination between repeats, so plant mtDNA rearranges often |
| Mutation / substitution pattern | Not covered in the sources I checked | Human mtDNA mutates more than 10 times faster than nuclear DNA (Karp). Plant mitochondrial coding regions change very slowly. |
| Transcription enzyme | Bacterial-type polymerase. My genome carries rpoB, rpoC1 and rpoC2. | Single-subunit polymerase related to bacteriophage enzymes (Karp) |
| Common research applications | Phylogeny and species identification (see Section 10) | Tracing human ancestry and ancient DNA (Karp) |

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
- Galaxy: [usegalaxy.org](https://usegalaxy.org), Fasta Statistics tool.
- Karp et al., Cell and Molecular Biology, 7th ed.
- Liu G. and Lee S. Characterization of the complete chloroplast genome of ornamental plant, Bougainvillea peruviana (Nyctaginaceae). Mitochondrial DNA B, 2020. [DOI: 10.1080/23802359.2020.1768948](https://doi.org/10.1080/23802359.2020.1768948)
- [Plant mitochondrial DNA replication components review, Plants 2019](https://doi.org/10.3390/plants8120533)
- [Mitochondrial genome recombination in somatic hybrids of Solanum commersonii and S. tuberosum](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9127095/)
- [The plant mitochondrial genome: Dynamics and maintenance (Biochimie)](https://www.sciencedirect.com/science/article/abs/pii/S0300908413003301)
- [RECG maintains plastid and mitochondrial genome stability (PLoS Genetics)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4358946/)
