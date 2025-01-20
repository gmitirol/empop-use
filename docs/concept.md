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
Anonymized population data are contributed to EMPOP by international research groups. All data submissions must comply with the ethical regulations of the countries where the samples were collected and analyzed. This includes providing documentation from the respective Ethics Boards and Informed Consent Forms. The process is guided by recommendations outlined in the Report of the [Forensic Database Advisory Board](https://doi.org/10.1016/j.fsigen.2024.103053).

Individual mitotypes undergo a rigorous quality control (QC) process that includes plausibility checks and analyses based on phylogenetic and population genetic principles. Unobserved or ambiguous variations are carefully examined by reviewing the sequencing raw data in collaboration with the data submitters. Mitotypes are also assessed for proper alignment and precise haplogroup assignment, with adjustments made as necessary.

The finalized dataset that passes QC is shared with the submitters, accompanied by an EMPOP QC report and an EMPOP accession number. This accession number serves as documentation of the successful QC process and should be referenced for future dissemination, such as in publications.

### 2.2	 Accessibility and status of mitotypes
Data uploaded to EMPOP are fully anonymized, with no sample names available to prevent the re-identification of sample donors. EMPOP mitotypes cannot be directly accessed or downloaded via the EMPOP webpage. Furthermore, mitotypes cannot be shared with third parties unless explicit written consent is provided by the data submitters, such as for collaborative research purposes.

Access to mitotypes is restricted to specific EMPOP software, which facilitates database queries. The output of an EMPOP search provides only the information necessary to understand the distribution and frequency of mitotypes (representing lineages, not individuals) at a national (country) or metapopulation level. No personal data about the sample donors are stored or provided through the EMPOP database.

### 2.3	 EMPOP queries
Database queries can only be performed using dedicated software implemented in EMPOP. The scientific foundation of these software modules, known as the String Alignment Method (SAM), is detailed in the scientific literature (Röck 2010; Huber 2018; Dür 2021). In summary, mitotypes encoded in the rCRS format, which is commonly used to represent mtDNA sequences, are converted into alignment-free nucleotide strings (FASTA-like format) and compared against a database of similarly formatted sequences. This approach ensures that matches between query and database sequences are identified independently of the alignment used in the query, eliminating alignment-related biases that could otherwise distort frequency values.

The EMPOP query output provides:

    The number of observed mitotypes in a given country or metapopulation
    The probability of the mitotype, calculated using the Clopper-Pearson method
    Correction factors to address sampling bias

Additionally, the ALIGNMENT tab offers a phylogenetic representation of the query mitotype, while the HAPLOGROUPING tab displays the best-matching haplogroups.

The scientific framework and quality control measures implemented in EMPOP have been deemed suitable for forensic purposes, as affirmed by several authoritative sources. These include a declaration by the German Supreme Court of Justice (2010), the SWGDAM mtDNA Interpretation Guidelines (2013, 2024), and the updated ISFG Guidelines for mtDNA Analysis and Interpretation (2014).


The scientific contents presented in EMPOP were developed by the
[Institute of Legal Medicine (GMI)](http://www.gmi.eu), Medical
University of Innsbruck and the [Institute of Mathematics, University of
Innsbruck](http://www.uibk.ac.at/mathematik/index.html.de).
