# Protein disorder summarizer

This script downloads, parses, and analyzes a proteins' pLDDT information via their associated AlphaFold predicted structure. it can take in a single UniProt accession as a string, or several accessions via a list of strings or through a Pandas dataframe. Simply call the "master_function" to try it out!

Dependencies

* Python3
* Pandas
* Biopython
* requests

note: the script will download a pdb file locally (called "{UniProt_accession_entered}.pdb") from the AlphaFold API. A lot of the specific functions were built around taking a Pandas Dataframe as input (what was used for this dissertation) but the basic functionality and output (see below) of this script will still be the same for other inputs when the master_function is called.



The script will output a Pandas dataframe of summary information...

```
average_pLDDT_for_entire_protein	Length_AlphaFold	num_disordered_res	num_ordered_res	percent_disordered_res_for_entire_protein	N_terminal_IDR_presence	N_IDR_length_over_10	C_terminal_IDR_presence	C_IDR_length_over_10	Disordered_tail_N_or_C_presence	Disordered_tails_N_and_C_presence	n_IDR_pLDDT_mean	c_IDR_pLDDT_mean	number_of_dis_regions_over_10_res	disordered_regions	average_length_dis_region	longest_length_dis_region	shortest_length_dis_region
0	73.355155	1544	460	1084	29.792746	1	25	0	0	1	0	35.3544	None	10	[25, 124, 13, 12, 17, 26, 10, 10, 69, 115]	42.1	124	10
```
