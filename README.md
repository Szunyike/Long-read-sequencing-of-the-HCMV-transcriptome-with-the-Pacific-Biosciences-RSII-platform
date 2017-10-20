# Long-read sequencing of the human cytomegalovirus transcriptome with the Pacific Biosciences RSII platform
Short package for basic statistics of mapping data described in the article.

Open the solution file with Visual Studio 2017 Community Edition and build.

Running each module copies data to the clipboard.

Read Counts From Bam requires .bam files and outputs the numbers of reads in the bam file and the numbers of mappings (one read can map many times to a genome) to the clipboard.

Read Count From Fastq requires .fastq or .fasta files and outputs the number of sequences in the file

Average Aligned Reads Best requires .bam files as input and creates a .tsv file with the same name as the input file. The .tsv file lists all read IDs and the lengths of the best mappings of the reads. Mappings with a longest alignment are considered the mapping of any given read.

Average Indel Mismatch Best
