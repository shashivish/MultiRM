# MultiRM: Attention-based multi-label neural networks for integrated prediction and interpretation of twelve widely occuring RNA modifications

## Prerequisites
* `python`: 3.7.6
* `CUDA`: 10.1
* `pytorch`: 1.2
## Installation
Our current release has been tested on Ubuntu 16.04.4 LTS

**Cloning the repository and downloading MultiRM**
```
git clone git@github.com:Tsedao/MultiRM.git
cd MultiRM
```

## Demo
Usage:
```
python main.py -s [RNA sequence] --top [No. of top-k highlighted sites] --gpu [which gpu to use]
```
Example:
```
python main.py -s CCTTTCCTCACCCATCTTAAGGTTCAATGGCTGACACTTCTGCAACAAAAG --top 3 --gpu 0
```
Predicting the RNA modification of a singe RNA sequence (Minimum length:21-bp), the result generates as:
```
****************************************Sample 1****************************************
The sequence is predicted as: m6Am with prob 0.127927 at threshold 0.032172
CCTTTCCTCACCCATCTTAAGGTTCAATGGCTGACACTTCTGCAACAAAAG Original Seqs
----TCC--ACC-----------TCA------------------------- Highlighted nucleotides by attention
The sequence is predicted as: AtoI with prob 0.362751 at threshold 0.360362
CCTTTCCTCACCCATCTTAAGGTTCAATGGCTGACACTTCTGCAACAAAAG Original Seqs
--------CAC------------TCA----------------CAA------ Highlighted nucleotides by attention

```
