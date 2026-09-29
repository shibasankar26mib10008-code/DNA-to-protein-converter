# DNA-to-protein-converter
This Python script translates a DNA sequence into a protein sequence. It validates the input to ensure it contains only A, T, G, and C, then transcribes it to RNA by swapping 'T' for 'U'. Reading the RNA in three-letter codons, it maps each triplet to its matching amino acid via a dictionary, stopping at any stop codon to output the protein chain.
