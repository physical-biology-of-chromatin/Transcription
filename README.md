# Transcription
Contains the polymer simulation codes (in fortran), the data analysis codes (in python, jupyter notebooks) and the processed data (in txt) used in the manuscript: Salari, Fourel & Jost, bioRxiv, 2023.07.18.549489 (2023).

* computing_IC_IR_score.ipynb: This Python Jupyter Notebook provides a comprehensive solution for computing both Intra-Gene Contact (IC) and Intra-Gene RNA Polymerase II (IR) scores. The tool has been rigorously tested and verified on Jupyter Notebook version 6.3.0. Dependencies: To utilize this tool effectively, ensure you have the following Python libraries and packages installed: 'Numpy', 'Matplotlib', 'Pandas', 'cooler 0.9.2', 'pyBigWig 0.3.18', 'cooltools 0.5.1', 'bioframe 0.3.2' and 'gtfparse 2.0.1'. Input Files: The tool expects the following input files in specific formats: Hi-C data (in .cool or .mcool format), ChIP-seq track data (in .BigWig format), and gene annotation data (in .gtf or .gff3 format). Output File: The tool provides a data frame containing gene position (chromosome, start, end, and direction), gene id name, and IC and IR scores. Usage: Ensure you have the required dependencies installed. Download test input files from https://zenodo.org/record/8225287 into "inputs" folder. Open the Jupyter Notebook in a compatible environment (e.g., Jupyter Notebook version 6.3.0). Execute the code cells sequentially, following the provided instructions. Ensure you have "outputs" folder for output files. The typical run time of the test on MAC OS 13.4.1 (c) is less than 10 minutes.
* PMGA_intragene_HiC.ipynb: This Python Jupyter Notebook provides a comprehensive solution for computing pileup meta-gene analysis (PMGA) for intra-gene Hi-C contact maps. The tool has been rigorously tested and verified on Jupyter Notebook version 6.3.0. Dependencies: To utilize this tool effectively, ensure you have the following Python libraries and packages installed: 'Numpy', 'Matplotlib', 'Pandas', 'cooler 0.9.2', 'pyBigWig 0.3.18', 'cooltools 0.5.1', 'bioframe 0.3.2' and 'gtfparse 2.0.1'. Input Files: The tool expects the following input files in specific formats: Hi-C data (in .cool or .mcool format), ChIP-seq track data (in .BigWig format), and gene annotation data (in .gtf or .gff3 format). Output File: The tool provides a obs/exp matrix corresponding to the specified gene cluster. Usage: Ensure you have the required dependencies installed. Download test input files from https://zenodo.org/record/8225287 into "inputs" folder. Open the Jupyter Notebook in a compatible environment (e.g., Jupyter Notebook version 6.3.0). Execute the code cells sequentially, following the provided instructions. Ensure you have "outputs" folder for output files. The typical run time of the test on MAC OS 13.4.1 (c) is less than 10 minutes.
* PMGA_intragene_ChIP.ipynb: This Python Jupyter Notebook provides a comprehensive solution for computing pileup meta-gene analysis (PMGA) for intra-gene ChIP-seq tracks. The tool has been rigorously tested and verified on Jupyter Notebook version 6.3.0. Dependencies: To utilize this tool effectively, ensure you have the following Python libraries and packages installed: 'Numpy', 'Matplotlib', 'Pandas', 'cooler 0.9.2', 'pyBigWig 0.3.18', 'cooltools 0.5.1', 'bioframe 0.3.2' and 'gtfparse 2.0.1'. Input Files: The tool expects the following input files in specific formats: Hi-C data (in .cool or .mcool format), ChIP-seq track data (in .BigWig format), and gene annotation data (in .gtf or .gff3 format). Output File: The tool provides a Numpy array containing the averaged ChIP-seg track corresponding to the specified gene cluster. Usage: Ensure you have the required dependencies installed. Download test input files from https://zenodo.org/record/8225287 into "inputs" folder. Open the Jupyter Notebook in a compatible environment (e.g., Jupyter Notebook version 6.3.0). Execute the code cells sequentially, following the provided instructions. Ensure you have "outputs" folder for output files. The typical run time of the test on MAC OS 13.4.1 (c) is less than 10 minutes.
* PMGA_intergene_HiC.ipynb: This Python Jupyter Notebook provides a comprehensive solution for computing pileup meta-gene analysis (PMGA) for inter-gene HiC contact maps. The tool has been rigorously tested and verified on Jupyter Notebook version 6.3.0. Dependencies: To utilize this tool effectively, ensure you have the following Python libraries and packages installed: 'Numpy', 'Matplotlib', 'Pandas', 'cooler 0.9.2', 'pyBigWig 0.3.18', 'cooltools 0.5.1', 'bioframe 0.3.2' and 'gtfparse 2.0.1'. Input Files: The tool expects the following input files in specific formats: Hi-C data (in .cool or .mcool format), ChIP-seq track data (in .BigWig format), and gene annotation data (in .gtf or .gff3 format). Output File: The tool provides an off-diagonal obs/exp matrix corresponding to the interaction of the specified gene clusters. Usage: Ensure you have the required dependencies installed. Download test input files from https://zenodo.org/record/8225287 into "inputs" folder. Open the Jupyter Notebook in a compatible environment (e.g., Jupyter Notebook version 6.3.0). Execute the code cells sequentially, following the provided instructions. Ensure you have "outputs" folder for output files. The typical run time of the test on MAC OS 13.4.1 (c) is less than 10 minutes.
* intragene_data.txt: This data frame is the processed data for mESC in Wildtype condition using publicly available data downloaded from GEO through accession no: GSE130275, GSE178982, GSE90893, GSE90994. It contains gene position (chromosome, start, end, and strand), intragene contact, RNA Pol II, SMC1a, RAD21, and CTCF scores, and also RNA-seq (fpkm). 
* polymer_simulation.zip: Fortran codes to simulate the biophysical model that couples a TASEP model of transcription and a polymer model of chromatin organization. Codes can run on Unix OS using GNU fortran and C compilers (gfortran & gcc). To compile, write 'make' in a Terminal. To run the program, open the 'script.sh' file, change the simulation parameters, save and then write 'bash script' in a Terminal. Output Files: The code provides a matrix of contact map for gene region and mean-squared displacement (MSD) (in nm^2) of the gene as a function time-lag (in MCS). The typical run time of 2*10^5 MCS on MAC OS 13.4.1 (c) is less than 10 minutes.

