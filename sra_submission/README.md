# Synopsis #
NCBI SRA accepts genetic data and the associated quality scores produced by next generation sequencing technologies. Files
can be compressed using `gzip` or `bzip2`, and may be submitted in a tar archive. All file names must be unique and not
contain any sensitive information. File names as submitted will appear publicly in the Goolge and AWS clouds. Finally, all
files for a submission must be uploaded into a single folder. If you have any question or concern about your data or
submission, you should contact [SRA support](mailto:sra@ncbi.nlm.nih.gov).

Submission to SRA requires the Python scripts, `sra_xml.py` and `sra_ascp.py`. The first script, `sra_xml.py` generates
the required XML file for submission, and second sends all files to SRA. The XML file consolidates all the metadata and
sequence files associated with the project, and is required by SRA. `mothur` has provided a similar function (see `mothur`
[Creating a new submission](https://www.mothur.org/wiki/Creating_a_new_submission)) but is limited to only the survey and
metagenome packages.

**Note**: Do not submit human data into the public SRA database without consent. Make sure that you have consent from the
donating individual to make this data available in an unprotected database. Do not transmit human data intended for dbGAP
submissions to the public SRA database. For more information, please visit
[NCBI SRA submission guideline](https://www.ncbi.nlm.nih.gov/sra/docs/submit/).

# Prerequisites #
* Python 3.5 or newer
* `xml.dom.minidom`: a minimal DOM implementation for Python
* `xml.etree.ElementTree`: the ElementTree API, a simple and lightweight XML processor for Python
* `ascp`: [Aspera secure copy](https://download.asperasoft.com/download/docs/entsrv/3.9.6/client_admin_win/webhelp/index.html)

# Example Project #
### Generate the XML Files ###
The folder `example` contains an example project. To generate the XML required for SRA submission, run the command:

```
sra_xml.py --email your.email@domain.com --input-dir 'example/' --listfile 'example/listfile.txt' --projectfile 'example/project.txt' --metadatafile 'example/samplegroup.txt' --orientation 'forward' --libselection 'CF-M' --libstrategy 'Bisulfite-Seq' --datatype 'ASSEMBLY' --instrument 'PromethION' --libsource 'METATRANSCRIPTOMIC' --platform 'Oxford Nanopore'
```

If the command completes successfully, you should see the message similar to the one below. The script should generate 2 XML
files, `submission.xml` and `validate.xml`. `submission.xml` should contain all the metadata needed for the submission to
SRA. The script also sends `submission.xml` to SRA for validation, and the file `validate.xml` shows the validation results.

```
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  7427    0   653  100  6774   5062  52511 --:--:-- --:--:-- --:--:-- 57573
```

The following is the description of the arguments and its default value.

* `-f/--input-dir`: Directory where all of the FASTQ files are located. This directory should not contain any
subdirectories.
* `-l/--listfile`: Name of the list file containing your sample ID to file mapping (does not require file locations,
just the names of the files). The list file should be in the following format and should contain no header row:
`SAMPLE_ID FORWARD_FILE REVERSE_FILE`. The default file name is `listfile.txt`. Please see the example list file,
`listfile.txt`, for the correct format.
* `-p/--projectfile`: Name of the file describing your project. The project file is contains the information on the
project in SRA that the samples are to be associated with. The default file name is `project.txt`. Please see the
example project file, `project.txt`, for the correct format.
* `-m/--metadatafile`: Name of the metadata file. This file contains all the metadata associated with the project.
The data should be saved in the CSV format. The default metadata file name is `samplegroup.txt`. Please see the
example metadata file, `samplegroup.txt`, for the correct format.
* `-a/--platform`: Specify sequencing platform. The options are `_LS454`, `ABI_SOLID`, `BGISEQ`, `CAPILLARY`,
`COMPLETE_GENOMICS`, `HELICOS`, `ILLUMINA`, `ION_TORRENT`, `OXFORD_NANOPORE`, and `PACBIO_SMRT`. The default
platform is `ILLUMINA`.
* `-o/--orientation`: Direction of the reads. The options are `forward` and `reverse`. Default: `forward`.
* `-s/--libstrategy`: Sequencing library preparation strategy. The options are `AMPLICON`, `ATAC-seq`,
`Bisulfite-Seq`, `ChIA-PET`, `ChIP-Seq`, `CLONE`, `CLONEEND`, `CTS`, `DNase-Hypersensitivity`, `EST`, `FAIRE-seq`,
`FINISHING`, `FL-cDNA`, `Hi-C`, `MBD-Seq`, `MeDIP-Seq`, `miRNA-Seq`, `MNase-Seq`, `MRE-Seq`, `ncRNA-Seq`, `OTHER`,
`POOLCLONE`, `RAD-Seq`, `RIP-Seq`, `RNA-Seq`, `SELEX`, `ssRNA-seq`, `Synthetic-Long-Read`, `Targeted-Capture`,
`Tethered Chromatin Conformation Capture`, `Tn-Seq`, `WCS`, `WGA`, `WGS`, and `WXS`. Default: `amplicon`.
* `-t/--datatype`: Data type is a general label indicating the initial primary study goals. The options are
`Assembly`, `Clone Ends`, `Epigenomics`, `Exome`, `Genome Sequencing`, `Genotype`, `MAP`, `Metagenome`,
`Metagenomic Assembly`, `Other`, `Phenotype`, `Proteomic`, `Random Survey`, `Targeted Loci`, `Transcriptome`,
`Variation`. `Genome sequencing` is set automatically as the Project Data Type of BioProjects that are created
during submission of prokaryotic or eukaryotic genomes. `Raw sequence reads` is set automatically as the Project
Data Type of BioProjects that are created during submission of sequences reads to SRA. The default option is
`metagenome`.
* `-r/--libsource`: Source of samples for sequence library. The options are `Genomic Single Cell`, `Genomic`,
`Metagenomic`, `Metatranscriptomic`, `Other`, `Synthetic`, `Transcriptomic Single Cell`, `Transcriptomic`, and
`Viral RNA`. Default: `metagenomic`.
* `-n/--instrument`: Sequencing platform used in the project. For the Roche 454 sequencing platform, the options are
`454 GS`, `454 GS 20`, `454 GS FLX`, `454 GS FLX+`, `454 GS FLX Titanium`, and `454 GS Junior`. For the Life
Technologies ABI SOLiD platform, the options are `AB 5500 Genetic Analyzer`, `AB 5500xl Genetic Analyzer`,
`AB 5500x-Wl Genetic Analyzer`, `AB SOLiD 3 Plus System`, `AB SOLiD 4 System`, `AB SOLiD 4hq System`,
`AB SOLiD PI System`, `AB SOLiD System`, `AB SOLiD System 2.0`, and `AB SOLiD System 3.0`. For the BGI sequencing
platform, the only option is `BGISEQ-500`. For the Applied Biosystems capillary sequencing platform, the options are
`AB 310 Genetic Analyzer`, `AB 3130 Genetic Analyzer`, `AB 3130xL Genetic Analyzer`, `AB 3500 Genetic Analyzer`,
`AB 3500xL Genetic Analyzer`, `AB 3730 Genetic Analyzer`, `AB 3730xL Genetic Analyzer`. For the Complete Genomics
sequencing platform, the only option is `Complete Genomics`. For the Helicos Biosciences sequencing platform, the
only option is `Helicos HeliScope`. For the Illumina sequencing platform, the options are `HiSeq X Five`,
`HiSeq X Ten`, `Illumina Genome Analyzer`, `Illumina Genome Analyzer II`, `Illumina Genome Analyzer IIx`,
`Illumina HiScanSQ`, `Illumina HiSeq 1000`, `Illumina HiSeq 1500`, `Illumina HiSeq 2000`, `Illumina HiSeq 2500`,
`Illumina HiSeq 3000`, `Illumina HiSeq 4000`, `Illumina iSeq 100`, `Illumina NovaSeq 6000`, `Illumina MiniSeq`,
`Illumina MiSeq`, `NextSeq 500`, and `NextSeq 550`. For the Ion Torrent platform, the options are `Ion Torrent PGM`,
`Ion Torrent Proton`, `Ion Torrent S5 XL`, and `Ion Torrent S5`. For the Oxford Nanopore platform, the options are
`GridION`, `MinION`, and `PromethION`. For the Pacific Biosystems SMART platform, the options are `PacBio RS`,
`PacBio RS II`, and `PacBio Sequel`. The default sequencing instrument is `Illumina MiSeq`.
* `-b/--libselection`: The permitted options are `5-methylcytidine antibody`, `CAGE`, `cDNA`, `cDNA_oligo_dT`,
`cDNA_randomPriming`, `CF-H`, `CF-M`, `CF-S`, `CF-T`, `ChIP`, `DNAse`, `HMPR`, `Hybrid Selection`, `Inverse rRNA`,
`MBD2 protein methyl-CpG binding domain`, `MDA`, `MF`, `MNase`, `MSLL`, `Oligo-dT`, `other`,
`Padlock probes capture method`, `PCR`, `PolyA`, `RACE`, `RANDOM`, `RANDOM PCR`, `Reduced Representation`,
`repeat fractionation`, `Restriction Digest`, `RT-PCR`, `size fractionation`, and `unspecified`. Default: `PCR`.

### Submit to SRA ###
When you are ready to submit to SRA, type:

```
sra_ascp.py --ncbi-sra-dir 'submit/' --input-dir 'example/' --ncbi-sra-dir 'sra_dir' --ncbi-username 'username' --ncbi-private-key 'keyfile'
```

**Note**: Do not run this command unless you have collected all required files for your project. The input folder should
contain all the files required by SRA for a submission.

This script will run `ascp` to transfer all the files to SRA. You should make sure that `ascp` has been successfully
installed on the system. Otherwise, the command will fail. NCBI has chosen to use a product from
[Aspera, Inc (Emeryville, CA)](https://www.aspera.com/en/) because of improved data transfer characteristics. The software
includes a command line tool (`ascp`) that allows scripted data transfer. The software client is free for users exchanging
data with NCBI. For more information about `ascp`, please visit the
[Aspear Transfer Guide](https://www.ncbi.nlm.nih.gov/books/NBK242625/).

The following is the description of the arguments.

* `-f/--input-dir`: Directory that contains all the files for a submission.
* `-d/--ncbi-sra-dir`: Path to the destination BioProject SRA submission folder.
* `-i/--ncbi-private-key`: Path to your private key file. In order to use the Aspera upload service you will need to use a
private SSH key, individual users should contact [SRA](mailto:sra@ncbi.nlm.nih.gov) to request an Aspera private key.
* `-u/--ncbi-username`: Username of your SRA account.

# Epilogue #
If your SRA submission is successful, you should receive an email with the subject *Submission ownership transfer*. After
the ownership transfer, you can view the submission process at the [Submission Portal](https://submit.ncbi.nlm.nih.gov/subs/).
You may need to log in with the NCBI credentials for the account you used in the submission metadata.

If your submission contain errors, you will receive an email informing you about the error. You should retrieve the file
`report.xml` from the SRA servers. If no `report.xml` is retrieved, this does not necessarily mean your submission failed.
The SRA system may not have generated it yet. You should wait for notification from the SRA that the submission has been
received and processed. During error correction, only make changes to SRA detected errors. All other changes will be ignored
by the SRA during resubmission. If additional changes are required, they can be made using the NCBI website after successful
submission.

If you are unsuccessful with the submission, you should contact [SRA staff](mailto:sra@ncbi.nlm.nih.gov) with the temporary
submission ID for assistance.

# Comments and Suggestions #
If you have any comments or suggestions, please [email us](mailto:metagenote@nih.gov).

Bioinformatics and Computational Biosciences Branch (BCBB)<br>
Office of Cyber Infrastructure and Computational Biology (OCICB)<br>
National Institute of Allergy and Infectious Diseases (NIAID)<br>
National Institutes of Health (NIH)<br>
Rockville, MD 20852

# Creative Common License #
UNLESS OTHERWISE SEPARATELY UNDERTAKEN BY THE LICENSOR, TO THE EXTENT POSSIBLE, THE LICENSOR OFFERS THE LICENSED MATERIAL
AS-IS AND AS-AVAILABLE, AND MAKES NO REPRESENTATIONS OR WARRANTIES OF ANY KIND CONCERNING THE LICENSED MATERIAL, WHETHER
EXPRESS, IMPLIED, STATUTORY, OR OTHER. THIS INCLUDES, WITHOUT LIMITATION, WARRANTIES OF TITLE, MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT, ABSENCE OF LATENT OR OTHER DEFECTS, ACCURACY, OR THE PRESENCE OR ABSENCE OF
ERRORS, WHETHER OR NOT KNOWN OR DISCOVERABLE. WHERE DISCLAIMERS OF WARRANTIES ARE NOT ALLOWED IN FULL OR IN PART, THIS
DISCLAIMER MAY NOT APPLY TO YOU.

TO THE EXTENT POSSIBLE, IN NO EVENT WILL THE LICENSOR BE LIABLE TO YOU ON ANY LEGAL THEORY (INCLUDING, WITHOUT LIMITATION,
NEGLIGENCE) OR OTHERWISE FOR ANY DIRECT, SPECIAL, INDIRECT, INCIDENTAL, CONSEQUENTIAL, PUNITIVE, EXEMPLARY, OR OTHER
LOSSES, COSTS, EXPENSES, OR DAMAGES ARISING OUT OF THIS PUBLIC LICENSE OR USE OF THE LICENSED MATERIAL, EVEN IF THE
LICENSOR HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH LOSSES, COSTS, EXPENSES, OR DAMAGES. WHERE A LIMITATION OF LIABILITY
IS NOT ALLOWED IN FULL OR IN PART, THIS LIMITATION MAY NOT APPLY TO YOU.

The disclaimer of warranties and limitation of liability provided above shall be interpreted in a manner that, to the
extent possible, most closely approximates an absolute disclaimer and waiver of all liability.

*Last updated on April 30, 2020*.
