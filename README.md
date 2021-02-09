### TPM-Transcripts-Per-Million-Normalization

**Description**
 
 This is a simple easy to follow tutorial on TPM normalization in python. After a wide web search, I couldn't find a descrption of the TPM normalization process using python. So I have put this together hoping that it helps someone <br>

**Transcripts Per Million (TPM)** is a normalization method for RNA-seq, should be read as "for every 1,000,000 RNA molecules in the RNA-seq sample, x came from this gene/transcript."

1. For each transcript in the gene model, the number (raw count) of reads mapped is divided by the transcript's length, giving a normalized transcript-level expression.
The distribution of ambiguous reads (between transcripts of the same gene, or between different genes) is handled by OmicSoft's RSEM implementation.<br>
2. The sum of ALL normalized transcript expression values is divided by 1,000,000, to create a scaling factor.<br>
3. Each transcript's normalized expression is divided by the scaling factor, which results in the TPM value.<br>
4. Gene-level TPM's are calculated by summing up the transcript-level TPM for each gene.<br>
Check: In this scaling, the sum of all TPMs (transcript-level or gene-level) should always equal 1,000,000. For cells that have approximately the same number of transcripts-per-cell, the TPM expression values can be compared between these cells to estimate relative abundance.


Reference: http://www.arrayserver.com/wiki/index.php?title=TPM#:~:text=Transcripts%20Per%20Million%20(TPM)%20is,from%20this%20gene%2Ftranscript.%22
