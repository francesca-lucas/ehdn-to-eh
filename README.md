# ehdn-to-eh

In order to transform the output from ExpansionHunter Denovo (EHdn) into a variant catalog usable for ExpansionHunter (EH), the scripts in 'create_variant_vatalog.py' can be used.
EHdn has two modes of analysis, for which a different function is needed. In case of the 
  - outlier analysis, use function: 'transform_outlier_format'.
  - casecontrol analysis, use function: 'transform_casecontrol_format'.
  
These functions take the input- and output files as arguments, using the following parameters:
  - ehdn_file:  the file as outputted by EHdn (tsv format).
  - refgen_file:  the file containing the reference genome, used for the EHdn analysis (fasta format).
  - varcat_out_file:  the filename used for the variant catalog output file. 
  - unmatched_out_file: the filename used for the unmatched regions output file; i.e. the regions that have no repeats in the reference genome.
  - excluded_out_file: the filename used for the excluded regions output file; i.e. the regions that contain more than 5 N's in the reference genome (EH doesn't accept these regions).
  
The outputs will be written to the specified output files.
