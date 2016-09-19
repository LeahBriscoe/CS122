# Detecting Inversions in the Genome 
Final Project for CS122: Bioinformatics Algorithms
## Workflow:
Step 1: Detect SNPs and identify insertions and deletions
Step 2: Filter SNPs to determine boundary points for putative inversions in the DNA sequence.
Step 3: Refine boundaries for inversions

## Program Description:
Starter code provided by course instructor. Functions that were modified to improve accuracy and efficiency are indicated in italics: 

**read_reads**: _Edited to improve speed of processing input reads by a factor of 10._ 
Takes in reads from input file and places in array. 

**read_reference**: Process input genome provided as reference. 

**pretty_print_aligned_reads_with_ref**: Display alignment of reads to reference.  

**generate_pileup**: _Replaced method for SNP detection to account for misaligned reads and to account for coverage. That is, portions of  the genome with poor coverage were treated more cautiously. The detection of inverions using a dynamic programming approach was also implemented here._ Interprets alignment of reads to reference to determine SNPs, INDELS, and STRs. 

**process_lines**: Analyzes given segment of genome from reference and donor reads aligned to that reference segment. Calls the indentity_changes function to find differences between ref and donor for given segment.

**align_to_donor**: _Implemented filtering method to throw out poorly aligned reads/erroneous reads that were not detected in a previous step._: Returns index for location in reference sequence where the given read aligns best 

**generate_donor**: _Improved accuracy finding optimal thresholds for error rate._ Returns a string for the donor sequences based on high coverage regions of sequence alignment. The reference sequence is used to fill in gaps.

**edit_distance matrix**: _Improved dynamic programming scoring method_ Dynamic programming matrix used to find optimal location to align given read on the reference.

**identify_changes**: Indentify which bases in the reference sequence were changed to what base in the donor sequence. Returns location and identity of indels.

**consensus**: Uses read aligned to reference alone to generate a consensus sequence. Does not take reference into account. 




