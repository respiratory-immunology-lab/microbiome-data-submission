# submit-microbiome-data-to-SRA
Pipeline on how to register a BioProject, BioSamples and submit sequencing data to NCBI SRA.

## Steps
1. Register a BioProject
2. Register BioSamples for the related BioProject
3. Submit data to SRA

Note: Can take some time for each step to get approved and updated.

## Details
Go to https://submit.ncbi.nlm.nih.gov/ and submit BioProject and BioSamples sequencially.

#### BioProject
The BioProject will be the link between the host and microbiome samples and data.
- Sample scope: Multispecies
- Target description: Bacterial 16S metagenomics (change it if there is also host transcriptomics)
- Organism name: Human
- Project type: metagenome (add transcriptome if also host transcriptomics)

#### BioSample
Microbiome samples will be registered as *MIMARKS Specimen samples*. On the BioSample metadata tab, download the BioSample metadata Excel template and fill it accordingly before uploading it. Be very careful with the required field formats.
- Use the BioProject accession number previously generated
- Organism: human metagenome
- Strain, isolate, cultivar, ecotype: not applicable
- Add any relevant host information in the table as well as the host tissue samples
- Any other colum which is not relevant: not applicable

#### SRA
This is where everything gets linked! Use the BioProject (same for all samples and data) and the BioSamples (different for each sample and data) accession numbers. On the SRA metadata tab, download the SRA metadata Excel template and fill it accordingly before uploading it. 
- Title: metagenome of "insert the organism and important information" e.g. "metagenome of human lower airways"
- Library ID: Sample name
- Library strategy: AMPLICON
- Library source: METAGENOMIC
- Library selection: PCR
- Library layout: paired
- Platform: ILLUMINA
- Instrument model: Illumina MiSeq
- Design description: put variable region (e.g. 16S V1-V2)
- File type: fastq
- Input the file names of R1 and R2

Upload the individual R1 and R2 demultiplexed fastq files. 

Note: can take a few days for the processing.

#### 









