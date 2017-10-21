# Long-read sequencing of the human cytomegalovirus transcriptome with the Pacific Biosciences RSII platform
Short package for basic statistics of mapping data described in the article.

Open the solution file with Visual Studio 2017 Community Edition and build. After starting the application you can select from the following 6 routines:

1. Read Counts From Bam requires .bam files and outputs the numbers of reads in the bam file and the numbers of mappings (one read can map many times to a genome) to the clipboard.

2. Read Count From Fastq requires .fastq or .fasta files and outputs the number of sequences in the file

3. Average Aligned Reads Best requires .bam files as input and creates a .tsv file with the same name as the input file. The .tsv file lists all read IDs and the lengths of the best mappings of the reads. Mappings with a longest alignment are considered the mapping of any given read.

4. Average Indel Mismatch Best .bam files as input and creates a .tsv file with the same name as the input file. The .tsv file lists all read IDs and the numbers of deletions, insertions, matches and mismatches of the best mappings of the reads in the .bam file. Mappings with a longest alignment are considered the mapping of any given read. Deletions, matches and mismatches values were calculated from the SAM optional field MD and the insertion values are from the CIGAR code. We find these quality values to be informative as we sometimes find that SMRTAnalysis deems a read more error-prone than it could be justified based on the mapping.

5. General coverage requires .bam files as an input files and outputs the total aligned read lengths in basepairs, divided by the complete genome length. Values are taken from the bam header.

6. BlastN parses Blast output files formated with -outfmt = 7 paramterer (Tabular with comment lines).
We sum every Hits' best HSP identity percent and number of mismatches by organism and print the total numbers of Mismatches, Numbers of reads aligned and Average Identity percents for each SeqID.
