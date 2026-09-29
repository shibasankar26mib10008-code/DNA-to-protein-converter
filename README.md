# DNA-to-protein-converter
This Python script translates a DNA sequence into a protein sequence. It validates the input to ensure it contains only A, T, G, and C, then transcribes it to RNA by swapping 'T' for 'U'. Reading the RNA in three-letter codons, it maps each triplet to its matching amino acid via a dictionary, stopping at any stop codon to output the protein chain.

## About the Project
The DNA to Protein Converter is a Python-based bioinformatics utility designed to simulate the biological processes of transcription and translation. It takes a raw DNA nucleotide sequence from the user, verifies its validity, converts it into an RNA sequence, and maps the corresponding amino acids to assemble the resulting protein sequence.

---

## Problems This Program Solves
* Eliminates Manual Translation Errors: Translating long nucleotide sequences manually using a codon table is time-consuming and prone to human error.
* Input Validation: Prevents processing invalid or corrupted sequence data by checking for unexpected characters before execution.
* Early Termination Handling: Automatically stops sequence translation when encountering a biological stop codon, simulating natural protein synthesis termination.

---

## Core Mechanism
1. Validation: Iterates through each character of the user input string to confirm it only contains the standard nitrogenous bases: Adenine (A), Thymine (T), Guanine (G), and Cytosine (C).
2. Transcription: Replaces every instance of Thymine (T) with Uracil (U) to derive the messenger RNA (mRNA) sequence.
3. Reading Frame Parsing: Slices the RNA sequence into non-overlapping 3-letter segments called codons.
4. Translation: Queries each codon against a pre-defined dictionary (codon_table).
   - If a match maps to an amino acid single-letter code, it appends to the protein sequence.
   - If a match maps to a stop codon (*), translation ceases immediately.

---

## Modules Used
* Built-in Python Features Only:
  - String Manipulation (.upper(), .replace(), string slicing)
  - Data Structures (dict for codon-to-amino-acid mapping)
  - Control Flow (for loops, if-else conditionals)

No third-party libraries or external modules are required.

---

## Key Features
* Case-Insensitive Input Handling: Automatically converts user input to uppercase so lowercase sequences like "atgc" work seamlessly.
* Strict Input Verification: Flags invalid characters (e.g., numbers, unknown letters) and alerts the user without crashing.
* Standard Genetic Code Mapping: Implements a dictionary covering all 64 standard RNA codons and their respective amino acids or stop signals.
* Incomplete Codon Handling: Ignores trailing incomplete sequence fragments (fewer than 3 characters at the end).

---

## How to Run
1. Prerequisites: Install Python 3.x on your system.
2. Save the Code: Save the script as dna_converter.py.
3. Execute: Open your terminal or command prompt and run:
   python dna_converter.py
4. Input: Enter a DNA sequence when prompted (e.g., ATGGCCATTTAA).
