## 6. EMPOP Tools

The EMPOP tools section provides a suite of software to support the analysis and interpretation of mitochondrial DNA sequence variation.

### 6.1.	Haplogroup Browser
This tool represents the established most recent Phylotree haplogroups in convenient searchable format and provides the number of EMPOP sequences assigned to the respective haplogroups by SAM2. Note that EMPOP provides the MRCA haplogroup if multiple haplogroup assignments are feasible. 
Individual haplogroups can also be found by querying differences to the rCRS in a database of > 20.000 mtGenome sequences.

![](images/fig12_populations.png)

### 6.2.	EMPcheck
EMPcheck is a tool to perform plausibility checks on an rCRS-coded data table.
The file format must meet the requirements described below and in Carracedo et al 2014.

#### 6.2.1.	Structure of the emp-file
Lines starting with "#!" indicate the sequence range of the mitotype. Note that a given sequence range is applied to all mtDNA mitotypes following this range until a new range is defined. Thus, multiple mitotypes with different sequence ranges can be handled in one file. 
The file lists the mitotypes in columns with the following contents.

- Column A: Sequence name: don't use blank space or special characters (allowed characters are letters (except umlauts ä, ö, ü), numbers, "-", "_", "/")

- Column B: Haplogroup (hg) status: indicate hg, if unknown, use "?"

- Column C: Frequency of mitotype (0 - 9999). Typically, this value is “1”, as individual mitotypes should be presented. If it is set to 0 the sample is not considered for the analysis.

- Column D: Annotation of the mitotype relative to the rCRS. Separate differences by tabs (or use individual cells in MS Excel). Use forensic notation of sequences as outlined in the revised and updated ISFG recommendations for mtDNA typing (Parson et al (2014)).

Text lines can be included everywhere in the file for comments or description. They need to be marked with "#".
Avoid blank lines (except when marked with "#").

The structure of an EMP file is illustrated below and the file can also be downloaded from: Downloads section in EMPOP.

EXAMPLE EMP FILE

### 6.3.	NETWORK

This tool can be used to calculate and draw quasi-median networks. They are useful to examine the quality of an mtDNA dataset.

MtDNA data tables can be depicted as quasi-median networks to enhance the understanding of the data in regard to homoplasmy and potential artifacts. Highly recurrent mutations are removed from the dataset (filtering) to help detect data idiosyncrasies that pinpoint sequencing and data interpretation problems. A detailed discussion of the method can be found in Bandelt and Dür (2007) and its application in Parson and Dür (2007). 

The following section leads you through
- the input and parameter selection of a network analysis
- the output generated by NETWORK
- network drawing and
- interpretation of the results.

#### 6.3.1.	Input

**Sample Info:**
The sample-specific information identifies a search. This is also the reference under which the query is reported. The history of NETWORK searches can be found under YOUR ACCOUNT.

**Input file (=emp file):**
The input file contains the annotated population data. The emp-file is a tab delimited text file that can be created using standard text software or MS Excel (then, safe file under .txt format and rename "txt" by "emp"). Its format needs to meet the following criteria:

**Ambiguous symbols:**
The software accepts the IUB-code. However, ambiguous symbols (e.g. sequence heteroplasmy Y ~ C/T) can cause artificial nodes and links in the network. Therefore it may be necessary to specify a non-ambiguous symbol either by calling the dominant type or by using the phylogenetic background of the sample. You will be notified on the presence of ambiguous symbols on the screen and in the network analysis report. For your information you also get a list of new insertions in your data set that are not known to the current EMPOP database.

**New insertions:**
We collect positions with observed insertions in an EMPOP datafile to which new data are compared. New insertions that have not been recorded in EMPOP yet are displayed to draw the attention on them. This however does not impact the performance of NETWORK.

**Filtering:**
Highly recurrent mutations are removed from the data set (filtering) that would otherwise increase the complexity of the network. You can choose between different filters depending on the application. The contents of the filters can be viewed by clicking on the symbol next to the dropdown box.


**Available filters:**
- EMPOPspeedy: This filter removes highly recurrent mutations based on the lists provided in Bandelt et al (2002 and 2006). This filter is typically used for the analysis of mtDNA population data within the hypervariable segments - HVS-I (16024 - 16569) and HVS-II (1 - 576).
- EMPOPspeedyWE: This filter removes highly recurrent mutations as presented in Zimmermann et al (2010). This filter is typically used for the analysis of west Eurasian mtDNA population data within the hypervariable segments - HVS-I (16024 - 16569) and HVS-II (1 - 576).
- EMPOPall_R11: This is a superfine filter that contains all mutations observed in EMPOP. This filter provides a very quick check on the data by highlighting only yet unobserved mutations. We update the EMPOPall filter periodically.
- Unfiltered: None of the mutations are removed from your dataset. This is useful for the analysis of very short sequence stretches in the mtDNA CR (see below). The complexity of the network will increase rapidly if no filter is applied to the analysis of larger sequence regions.

**Range:**
The range determines the region for which the network is computed. Any range within 16024-16569 and 1-576 can be queried. In some data very small regions may be interesting for detailed network analysis (e.g. 450-460).

Submit starts the execution.


#### 6.3.2.	Output

After clicking on the Submit Button, the network calculation is initiated. Depending on the size of the file and the used filter options this process may take some time.
When finished, result files will be listed in “Network Result Files” on the “your account” page.

![](images/fig13_network.png)

Download the file and unzip it to obtain the folder [RID_FILTERNAME_REGION], which contains the following files:
- Results file [FILENAME_report.txt]: This file summarizes the settings and the results of the network analysis - for details see chapter Interpretation. 
- File for drawing the network [FILENAME_network.dnw]: This file can be used to draw the entire network of the mtDNA datafile by dnw.exe. 
- File for drawing the torso [FILENAME_torso.dnw]: This file can be used to draw the torso of the network of the mtDNA datafile by dnw.exe. 
- Difference table of the network [FILENAME_network.txt]: This file contains the filtered and reduced mitotypes of the entire network, displayed in dot table format. 
- Difference table of the torso [FILENAME_torso.txt]: This file contains the filtered and reduced mitotypes of the torso of the network, displayed in dot table format. 
- EMP-File [EMPFileName.emp]: The emp file which was uploaded
- Info-file [FILENAME_info.txt]: Contains the sample identification (which was defined in “Sample info”, see 6.3.1 Input) and the title of the emp file.

**Drawing**
1.	Download the software for drawing the network (DrawNetWorkSetup.exe) from the EMPOP download page.
2.	Execute the file and follow the instructions given by the software. Choose a destination folder where the software is to be installed.
3.	Once the installation is finished you can find a folder called DrawNetWork containing the software and an uninstaller in the start menu. Files having ".dnw" as file ending are automatically linked to the software. Double-clicking a dnw file opens the network in a separate window. The help menu contains a legend of keys to edit the network (e.g. t ... for drawing a draft of the network, l ... for adding labels, etc.). During execution the current drawing can be exported in SVG (Scalable Vector Graphic), EPS (Encapsulated PostScript) or GIF format for printing or editing.

**Interpretation**
The Report.txt file summarizes relevant information of the network analysis. The network is described in a table by the number of samples (n), the number of polymorphic positions (p), the number of partitions or condensed characters (p’), the number of mitotypes (h), the number of nodes in the network (q), the number of nodes in the torso (t) and the number of nodes of the peeled torso (t’). These values are indicative for the quality of a network. However, they depend on the size and composition of the population data set in question. Generally, small t’-values (ideally 1) describe a star-like structure of the network, which is in agreement with the expected evolutionary pattern. 
A more suggestive representation of the data is the graph of the quasi-median network. The nodes of this graph are given by the mitotypes or the quasi-medians generated from the mitotypes. In the drawing the frequencies of the mitotypes or quasi-medians are also shown. The root node is drawn with a bold circle and contains the filtered and reduced Anderson sequence (In the rare case that no mitotype contains the filtered and reduced Anderson sequence, the first mitotype is chosen instead and a warning is included in the report). The links are single or combined mutations specified by the syntax for single mutations or / for combined mutations, where the orientation is from the root node outwards. Links with the same mutation are drawn parallel and are labeled only once. The torso is obtained from the quasi-median network by collapsing all pendant subtrees into their base nodes. Thus the analysis of homoplasmy can be restricted to the torso which contains all the reticulation of the network. For each base node the coinciding mitotypes are listed in the report to make it easy to find all corresponding samples.
 
#### References & Further Reading
- Bandelt HJ et al (2002) The fingerprint of phantom mutations in mitochondrial DNA data. Am J Hum Genet 71:1150-1160
- Bandelt HJ et al (2006) Estimation of mutation rates and coalescence times: some caveats. In: Human mitochondrial DNA and the evolution of Homo sapiens. Springer-Verlag eds. Hans-Jürgen Bandelt, Vincent Macaulay, Martin Richards
- Bandelt and Dür (2007) Translating DNA data tables into quasi-median networks for parsimony analysis and error detection. Mol Phylogenet Evol 42:256-271
- Parson and Dür (2007) EMPOP - A forensic mtDNA database. FSI:Genetics 1:88-92
- Schwarz and Dür (2011) Visualization of quasi-median networks. Discrete Applied Mathematics 159(15):1608-1616
- Zimmermann et al (2014) Improved visibility of character conflicts in quasi-median networks with the EMPOP NETWORK software. Croat Med J 55(2): 115-120.
- Parson et al (2013) Evaluation of next generation mtGenome sequencing using the Ion Torrent Personal Genome Machine (PGM). FSI: Genetics 7(5): 543-549
- Eduardoff et al (2017) Optimized mtDNA Control Region Primer Extension Capture Analysis for Forensically Relevant Samples and Highly Compromised mtDNA of Different Age and Origin. Genes 8(10)
- Strobl et al (2018) Evaluation of the precision ID whole MtDNA genome panel for forensic analyses. FSI: Genetics 35: 21-25.
