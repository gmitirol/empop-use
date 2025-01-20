## 2. Concept

**Main functions of EMPOP**

1)	Estimate the frequecy of a mitotype in a given population
2)	Check mitotype alignment
3)	Estimate haplogroup and evaluate its distribution
4)	Examine the quality of a mitotype/an mtDNA dataset

EMPOP stores anonymized mitotypes that are not linked to any personal information about the sample donors. Through an EMPOP query, only the country of origin and the self-reported metapopulation of the sample donors are accessible.

⚠️ EMPOP cannot be used to re-identify the sample donor

⚠️ EMPOP does not provide evidentiary leads

⚠️ Data cannot be downloaded from EMPOP


### 2.1	 Mitotype submission and quality control
Anonymized population data are contributed to EMPOP by international research groups. All data submissions must comply with the ethical regulations of the countries where the samples were collected and analyzed. This includes providing documentation from the respective Ethics Boards and Informed Consent Forms. The process is guided by recommendations outlined in the Report of the Forensic Database Advisory Board(https://doi.org/10.1016/j.fsigen.2024.103053).

The individual mitotypes undergo rigorous quality control (QC) using plausibility checks and investigations based on phylogenetic and population genetic principles. Unobserved and ambiguous variation is scrutinized using the sequencing raw data in dialogue with the data submitters. The mitotypes are further examined with respect to alignment and haplogroup assignment (fine-tuned) and corrected if needed. The final dataset passing QC is shared with the submitters along with an EMPOP QC report and an EMPOP accession number that is used to document the successful QC process for later dissemination (e.g., publication).

### 2.2	 Accessibility and status of mtDNA data
Data uploaded onto EMPOP are again anonymized and no sample names are made available to prevent re-identification of the sample donors. EMPOP mitotypes cannot be directly accessed or downloaded via the EMPOP webpage. MtDNA data cannot be shared with third parties, except explicit written consent is provided by the data submitters, e.g., for collaborative research. Mitotypes can only be accessed by specific EMPOP software that performs database queries. The output of an EMPOP search only provides information that is necessary to understand the distribution and frequency of mitotypes (=lineages; not individuals) on a national (country) or metapopulation (link) level. No personal data of the sample donors are available or provided via the EMPOP database.

### 2.3	 EMPOP queries
Database queries can only be performed via dedicated software implemented in EMPOP. The scientific basis of these software modules (String Alignment Method; SAM) is laid out in the scientific literature (Röck 2010; Huber 2018, Dür 2021). In brief, rCRS-coded mitotypes, that are typically used to communicate mtDNA sequences, are turned into alignment-free strings of nucleotides (FASTA-like format) and searched in a database of FASTA-like sequences. Thus, matches between query and database sequences are found independent of the alignment used in a query, which would otherwise lead to biased frequency values. The EMPOP output lists the number of observed mitotypes in a given country/metapopulation, the probability of the mitotype following Clopper/Pearson and offers correction factors for sampling bias.
Under the ALIGNMENT tab the phylogenetic representation of the query mitotype is provided and the HAPLOGROUPING tab lists the best matching haplogroups.

The scientific concept and the quality control measures applied in EMPOP were found suitable for forensic purposes, e.g. by a declaration of the German Supreme Court of Justice (2010), the SWGDAM mtDNA interpretation guidelines (2013), and the updated ISFG guidelines for mtDNA analysis and interpretation (2014).


The scientific contents presented in EMPOP were developed by the
[Institute of Legal Medicine (GMI)](http://www.gmi.eu), Medical
University of Innsbruck and the [Institute of Mathematics, University of
Innsbruck](http://www.uibk.ac.at/mathematik/index.html.de).
