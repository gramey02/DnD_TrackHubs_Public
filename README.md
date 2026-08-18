# Dominant & Dispensable (D&D) Gene TrackHubs

## Overview
This repository includes bed and bigBed files that can be uploaded to UCSC Genome Browsers' TrackHub page.

## Easy Quickstart
A saved session with a track showing all D&D gene editing targets can be found [here](https://genome.ucsc.edu/s/gramey02/All_DnDgenes_session). Note that the initial view opens on _AARS1_, but one can navigate to any gene of interest and the track will persist. Navigate to the main page for the track to get a description of the color scheme and variant identification methods, or visit [this description html](https://gramey02.github.io/DnD_TrackHubs_Public/track_descriptions/dnd_track_description.html).

## How to view variants for all D&D genes
The `trackhub_current` and `trackhub_description` folders contain the necessary files for uploading the track the UCSC genome browser. Within each of these, you will see:
- genomic data files
    * `.bb` file - bigBed file (created from the .bed file from all of the genes (not currently uploaded due to size) and .as files) of common variants. This bigBed format is necessary to include metadata in the track.
- .txt files. _These are important for uploading the tracks to TrackHub_
    * `All_DnD_genes_hub_file_wCellLines_ng.txt` file - text file with track metadata that points to gene's bigbed file. Also incorporates commonly used cell line genomes as tracks for visualizing whether certain cell lines are heterozygous at common variant locations
- cell line files
    * These currently live in the `archived_trackhubs/bed_files/all_genes_w_filtering` folder. Current cell lines represented are Wild Type (WT) B, WTC, WTD, and KOLF2.

To upload these files yourselves instead of using the preloaded session link above, navigate to the .txt file, click on `Raw`, and copy the resulting link at the top of the page. Then, navigate to UCSC's [TrackHub](https://genome.ucsc.edu/cgi-bin/hgHubConnect#unlistedHubs) location.

In the "Connected Hubs" Tab, upload the raw Github link that was copied, and click "Add Hub". Now, when you navigate to your gene of interest in the browser, you should see the track displayed.

## Tutorials
Please view the BrowserTrack_Tutorial.mp4 video for a tutorial on how to use the tracks. The current video displayed includes use of the filter-by-edit strategy feature, and soon will display the color scheme addition.

## Citation
Please cite the following [medRxiv preprint](https://www.medrxiv.org/content/10.64898/2026.03.26.26349431v1) when using code from this repository:
```bash
Ramey, G. D., Cowan, Q. T., Saxena, A. G., Macklin, B. L., Watry, H. L., Mei, S., ... & Capra, J. A. (2026). Leveraging human genetic variation to therapeutically target hundreds of genes with dominant & dispensable disease alleles. medRxiv, 2026-03.
```

## Issue reporting
Please use the 'Issues' tab at the top of the repository (next to 'Code') to report issues. Please use the bug reporting template for pipeline errors and the feature request template for suggested changes to browser tracks, such as color changes and viewing properties.
