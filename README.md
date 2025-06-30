# DNA Sequence Analysis (Ambiguous and Unambiguous)
@travelerfromeast
<b>[01-07-2025]</b>
This repository contains two Jupyter notebooks for analyzing DNA sequences:

<ol>
  <li> <b> `seq_unambiguous.ipynb` </b> – Handles standard DNA sequences containing only A, T, G, C. </li>
  <li> <b> `seq_ambiguous.ipynb`</b> – Supports sequences containing IUPAC ambiguous bases like N, R, Y, etc. </li>
</ol>

<br>
<br>

## Contents
<table>
  <tr>
    <td> file name </td>
    <td> description </td>
  </tr>
  <tr>
    <td> `seq_unambiguous.ipynb` </td>
    <td> Analyzes standard DNA sequences (no ambiguity). Includes transcription, translation, GC content, and reverse-complement generation. </td>
  </tr>
  <tr>
    <td> `seq_ambiguous.ipynb` </td>
    <td> Performs all the same functions as above, but with full support for IUPAC ambiguous bases (e.g., N, R, Y, B, D, etc.) and approximated GC content. </td>
  </tr>
</table>

## Features
- DNA Template → Coding Strand
- Coding Strand → mRNA (Transcription)
- mRNA → Protein (Translation)
- Reverse Transcription: mRNA → Coding → Template DNA
- GC Content Calculation (with weighted ambiguity in ambiguous version)
- Reverse & Complement strand generation
- <b>Does not include error-correction or sequence alignment features</b>

<br>
</br>

## Ambiguous Base Codes (IUPAC)
<table>
  <tr>
    <td><b> symbol </b></td>
    <td><b> bases represented </b></td>
    <td><b> complement </b></td>
  </tr>
  <tr>
    <td><b> N </b></td>
    <td><b> A/C/G/T </b></td>
    <td><b> N </b></td>
  </tr>  
  <tr>
    <td><b> R </b></td>
    <td><b> A/G </b></td>
    <td><b> Y </b></td>
  </tr>
  
  <tr>
    <td><b> Y </b></td>
    <td><b> C/T </b></td>
    <td><b> R </b></td>
  </tr>
  <tr>
    <td><b> S </b></td>
    <td><b> C/G </b></td>
    <td><b> W </b></td>
  </tr>
  <tr>
    <td><b> W </b></td>
    <td><b> A/T </b></td>
    <td><b> S </b></td>
  </tr>
  <tr>
    <td><b> M </b></td>
    <td><b> A/C </b></td>
    <td><b> K </b></td>
  </tr>
  <tr>
    <td><b> K </b></td>
    <td><b> G/T </b></td>
    <td><b> M </b></td>
  </tr>
  <tr>
    <td><b> N </b></td>
    <td><b> A/C/G/T </b></td>
    <td><b> N </b></td>
  </tr>
  <tr>
    <td><b> B </b></td>
    <td><b> C/G/T </b></td>
    <td><b> V </b></td>
  </tr>
    <tr>
    <td><b> V </b></td>
    <td><b> A/C/G </b></td>
    <td><b> B </b></td>
  </tr>
  <tr>
    <td><b> D </b></td>
    <td><b> A/G/T </b></td>
    <td><b> H </b></td>
  </tr>
  <tr>
    <td><b> H </b></td>
    <td><b> A/C/T </b></td>
    <td><b> D </b></td>
  </tr>
</table>
For RNA, replace T with U (e.g., Y = C or U)

<br>
<br>

## Example Usage

### For Unambiguous Input:
Input DNA Template Strand: TACGCATGC
template strand:  TACGCATGC
coding strand:  ATGCGTACG
mRNA:  AUGCGUACG
protein:  MRT

### For Ambiguous Input:
Input DNA Template Strand: ATGNGTRCG 
template strand:  ATGNGTRCG
coding strand:  TACNCAYGC
mRNA:  UACNCAYGC
protein:  YXX (here, X is an ambiguous amino acid corresponding to the ambiguous codon)
