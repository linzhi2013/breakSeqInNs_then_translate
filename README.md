# breakSeqInNs_then_translate

## 1 Introduction

`breakSeqInNs_then_translate` is a tool to filter the sequences by translating the protein coding genes (PCGs) with proper genetic code table, if one of the PCGs has interal stop codon, filter out this sequence. By Guanliang MENG, see https://github.com/linzhi2013/extract_fasta_seq

## 2 Installation

    pip install breakSeqInNs_then_translate

There will be a command `breakSeqInNs_then_translate` created under the same directory as your `pip` command.

## 3 Usage

    usage: breakSeqInNs_then_translate.py [-h] [-seq <seq>] [-seqfile <file>]
                                          [-seqformat {fa,gb}] [-code <int>] [-nb]
                                          [-gb_genes <int>] [-maxStopGenes <int>]

    Filter the sequences by translating the protein coding genes (PCGs) with
    proper genetic code table, if one of the PCGs has interal stop codon, filter
    out this sequence. Beware: if the seq has Ns, then this script will translate
    the sub seqs with three frames (0, 1, 2), only when all these three kinds of
    frames have interal stopCodon the seq will be treated as have InternalStop!.
    By Guanliang MENG, see https://github.com/linzhi2013

    optional arguments:
      -h, --help           show this help message and exit
      -seq <seq>           input sequence
      -seqfile <file>      input fasta or genbank file
      -seqformat {fa,gb}   input -seqfile format [fa]
      -code <int>          genetic code table [1]
      -nb                  do not break sequence in Ns when translate [break]
      -gb_genes <int>      if a genbank record has no less than -gb_genes PCGs and
                           no more than -maxStopGenes PCGs has InternalStops, we
                           keep this record. But if a genbank record has less than
                           -gb_genes PCGs, then we will discard this record if any
                           of its PCGs has InternalStops. This is because we may
                           want to tolerate some assembly/sequencing errors. This
                           has no effect on fasta input file. [5]
      -maxStopGenes <int>  the maximum number of PCGs can have InternalStops in a
                           genbank record if do not discard it [0]

## 4 Author
Guanliang MENG

## 5 Citation
Currently I have no plan to publish `breakSeqInNs_then_translate`.






