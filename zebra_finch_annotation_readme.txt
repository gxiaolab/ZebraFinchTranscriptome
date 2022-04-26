# README

** README for zebra_finch_annotation.gtf**

Date created: 2022-04
--

## Overview

zebra_finch_annotation.gtf is a refined gene annotation based on Ensembl zebra finch (Taeniopygia guttata) gene annotation bTaeGut1_v1.p. In addition to the existing information from the ensembl annotation (access: http://ftp.ensembl.org/pub/release-106/gtf/taeniopygia_guttata/), the refined annotation also includes 220 novel genes and 8,134 transcript variants discovered from our bioinformatic analysis. 

There are three gene/transcript sources in this annotation: ensembl, StringTie,and TALON. StringTie is software used for NGS RNA-seq analysis and TALON is the softare pipeline used for PacBio data analysis. The refined annotation adopts the same file format as the Ensembl gene annotation. For details, please see section 'Definition and file format'

--

## Definition and file format 

The GTF (General Transfer Format) is an extension of GFF version 2 
and used to represent transcription models. GFF (General Feature Format) 
consists of one line per feature, each containing 9 columns of data. 

Fields

Fields are tab-separated. Also, all but the final field in each 
feature line must contain a value; "empty" columns are denoted 
with a '.'

    seqname   - name of the chromosome or scaffold; chromosome names 
                without a 'chr' 
    source    - name of the program that generated this feature, or 
                the data source (database or project name)
    feature   - feature type name. Current allowed features are
                {gene, transcript, exon, CDS, Selenocysteine, start_codon,
                stop_codon and UTR}
    start     - start position of the feature, with sequence numbering 
                starting at 1.
    end       - end position of the feature, with sequence numbering 
                starting at 1.
    score     - a floating point value indiciating the score of a feature
    strand    - defined as + (forward) or - (reverse).
    frame     - one of '0', '1' or '2'. Frame indicates the number of base pairs
                before you encounter a full codon. '0' indicates the feature 
                begins with a whole codon. '1' indicates there is an extra
                base (the 3rd base of the prior codon) at the start of this feature.
                '2' indicates there are two extra bases (2nd and 3rd base of the 
                prior exon) before the first codon. All values are given with
                relation to the 5' end.
    attribute - a semicolon-separated list of tag-value pairs (separated by a space), 
                providing additional information about each feature. A key can be
                repeated multiple times.

Attributes

The following attributes are available. All attributes are semi-colon
separated pairs of keys and values.

- gene_id: The stable identifier for the gene
- gene_version: The stable identifier version for the gene
- gene_name: The official symbol of this gene
- gene_source: The annotation source for this gene
- gene_biotype: The biotype of this gene
- transcript_id: The stable identifier for this transcript
- transcript_version: The stable identifier version for this transcript
- transcript_name: The symbold for this transcript derived from the gene name
- transcript_source: The annotation source for this transcript
- transcript_biotype: The biotype for this transcript
- exon_id: The stable identifier for this exon
- exon_version: The stable identifier version for this exon
- exon_number: Position of this exon in the transcript
- ccds_id: CCDS identifier linked to this transcript
- protein_id: Stable identifier for this transcript's protein
- protein_version: Stable identifier version for this transcript's protein
- tag: A collection of additional key value tags
- transcript_support_level: Ranking to assess how well a transcript is supported (from 1 to 5)

  
