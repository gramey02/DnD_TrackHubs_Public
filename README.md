# Dominant & Dispensable (D&D) Gene TrackHubs

## Overview
This repository includes bed and bigBed files that can be uploaded to UCSC Genome Browsers' TrackHub page.

## Easy Quickstart
A saved session with a track showing all D&D gene editing targets can be found [here](https://genome.ucsc.edu/s/gramey02/All_DnDgenes_session). Note that the initial view opens on _NEFL_, but one can navigate to any gene of interest and the track will persist.

## How to view variants for your specific gene
Navigate to the `bed_files/per_gene_files` folder and select your gene of interest. There are a few files in each gene's folder:
- genomic data files
    * `.bed` file - tabular common variant information and allele/sequence metadata
    * `.as` file - contains metadata on .bed columns for conversion to bigBed
    * `.bb` file - bigBed file (created from the .bed and .as files) of common variants. This bigBed format is necessary to include metadata in the track
- .txt files. _These are important for uploading the tracks to TrackHub_
    * `<gene>_hub_file_ng.txt` file - text file with track metadata that points to gene's bigbed file
    * `<gene>_hub_file_wCellLines_ng.txt` file - text file with track metadata that points to gene's bigbed file. Also incorporates commonly used cell line genomes as tracks for visualizing whether certain cell lines are heterozygous at common variant locations

For uploading single gene files, use either of the .txt files (depending on whether you want to view cell line variants along with your reference genome common variants on interest).

To upload the file, click into the .txt file, click on `Raw`, and copy the resulting link at the top of the page. Then, navigate to UCSC's [TrackHub](https://genome.ucsc.edu/cgi-bin/hgHubConnect#unlistedHubs) location.

In the "Connected Hubs" Tab, upload the raw Github link that was copied, and click "Add Hub". Now, when you navigate to your gene of interest in the browser, you should see the track displayed.

## How to view all gene editing targets for DnD genes
Follow the steps above to upload the .txt file of interest for all genes. The .txt file relevant to all genes is located in the `bed_files/metadata` folder.

## Tutorials
A step-by-step guide (similar to the above but with screenshots of each step) and a Youtube tutorial video are in development.


