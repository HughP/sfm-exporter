# SFM exporter (Toolbox/FLEx SIL) [v2.0.0]

This repository contains an `R` script and the code of a Shiny app for converting a file with lexical data to a [Standard Format Markers](http://www-01.sil.org/computing/shoebox/MDF_2000.pdf?_ga=GA1.2.1165924973.1480287656) file (Toolbox/FLEx SIL).

## The script: `sfm-exporter.R`

The script converts from a tab delimited file (`txt`, `.csv`, `.tsv`) or a Microsoft Excel `.xlsx` file to a plain text `.txt` file with standard format markers.


**Input**:
- a prompt let you choose the lexicon file
- the lexicon file is a tab delimited or a Microsoft Excel `.xlsx` file
- the name of the columns in the file will be the markers (so, the lexeme column should be called `\lx`, the gloss column `\ge` and so on)

**Output**:
- the output file is a `.txt` file named "lexicon-sfm" with SF markers

**Process**:
The script reads the lexicon file and appends the marker to each cell according to the name of the column. Empty cells are skipped. This avoids the presence of empty markers.

## The app: `sfm-exporter`
The Shiny app `sfm-exporter` is based on the script and reachable at https://stefanocoretta.shinyapps.io/sfm-exporter/.

## Acknowledgements

Thanks to Hong Ooi and David Arenburg for providing the implementation of a `mapply` function on [stackoverflow](http://stackoverflow.com/questions/25666170/r-subsetting-dataframe-in-for-loop-with-double-and-single-brackets).
