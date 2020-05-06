# Autosomal DNA Converter

## About
The aim of this project is to enable the conversion of different data formats for autosomal DNA file. Supports the conversion of raw autosomal dna data from ftdna, 23andme, ancestry and decodeme to ftdna, 23andme and ancestry. You can download pre-built executable from [releases](https://github.com/fiidau/Autosomal-DNA-Converter/releases/latest).

## Usage:
```
Syntax:

        aconv <in-file> <out-file> [options]

Optional Parameters:
 -i  [Input Type]  - Value can be detect,ftdna,23andme,decodeme,
                     geno2 or ancestry. This values is optional and 
                     not required. Use only if autodetect fails.
                     Default is detect
 -o  [Output Type] - Value can be ftdna,23andme,geno2,ancestry, 
                     plink or eigenstrat. Default is ftdna

Example:
    aconv 264652-o36-results.csv.gz 23andme.txt -o 23andme


Note: Converting to FTDNA from 23andme or ancestry will lose Y and mtDNA data as
they are not part of raw download format. Converting Geno 2.0 to anything will not
have build positions, but just a format change.
```

## Change Log
Version 1.4:
- Support for plink and eigenstrat.

Version 1.3:
- Support for extremely large files. Fixed Out of memory issue.

Version 1.2:
- Basic support for Geno 2.0 conversion to another format. Since Geno 2.0 does not have any build positions, the output format will also not have any build positions.

Version 1.1:
- Auto-detects input file. Supports ftdna, 23andme, ancestry and decodeme. Also supports compressed .gz files.

Version 1.0:
- Converts FTDNA Autosomal DNA (FamilyFinder) raw download file format to 23andMe format.
