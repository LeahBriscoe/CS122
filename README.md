# Detecting Inversions in the Genome 
Final Project for CS122: Bioinformatics Algorithms
## Workflow:
Step 1: Detect SNPs and identify insertions and deletions
Step 2: Filter SNPs to determine boundary points for putative inversions in the DNA sequence.
Step 3: Refine boundaries for inversions

## Program Description:
Starter code provided by course instructor. Functions that were modified to improve accuracy and efficiency are indicated below in parantheses: 
_read_reads_(edited to improve speed of processing input reads): 
takes in reads from input file and places in array 
_read_reference_: process input genome provided as reference 
_pretty_print_aligned_reads_with_ref_: display alignment of reads to reference  
_generate_pileup_ (method for SNP detection replaced to account for misaligned reads and to account for coverage. That is, portions of  the genome with poor coverage were treated more cautiously. The detection of inverions using a dynamic programming approach was also implemented here.): Interprets alignment of reads to reference to determine SNPs, INDELS, and STRs. 
_process_lines_
# align_to_donor
# generate_donor: Generate 
# edit_distance matrix
# identify_changes
# consensus


