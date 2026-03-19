# Region-specific and nutritionally adequate dietary transitions can bolster sustainability and socioeconomic benefits

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18092979.svg)](https://doi.org/10.5281/zenodo.18092979)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Supplementary material for the journal publication **Rodés-Bachs, C., Sampedro, J., Van de Ven, D., Horowitz, R., Pardo, G., & Zhao, X. (2026).
[Region-specific and nutritionally adequate dietary transitions can bolster sustainability and socioeconomic benefits](https://www.nature.com/articles/s43016-026-01316-1). Nature Food. DOI: [10.1038/s43016-026-01316-1](10.1038/s43016-026-01316-1)**.


Related repositories:

* [Code Ocean Platform](https://doi.org/10.24433/CO.8681666.v1): online interactive version of the analysis code. It also contains the required data.
* [Data Zenodo archive](https://doi.org/10.5281/zenodo.18086406): data required for the analysis descrived in this repo.
* [Code Zenodo archive](https://doi.org/10.5281/zenodo.18092979): latest version of the analysis code provided in this repo.
* [GCAM version](https://github.com/klau506/gcam-core/tree/gcam_v7.0p_diets): GCAM version used to run all 1,298 dietary change the scenarios.

This repository is released under the Apache v2.0 license; see the LICENSE for details. For any doubts, contact claudia.rodes@bc3research.org.


## What's in this repo?

This repository provides the complete analysis code and data visualization scripts used in the study. To ensure seamless reproducibility, we provide a Docker image containing the full environment. Alternatively, you can access an interactive online version of the analysis via the [Code Ocean Platform](https://doi.org/10.24433/CO.8681666.v1).

This repo is structured in the following way:

- `R` folder: R scripts.
- `data` folder: folder to store the data for the analysis and figure creation.
- `results` folder: folder where the created figures will be stored.

Due to the `output` and `input` folders' size, the corresponding data can be found in [this Zenodo archive](https://doi.org/10.5281/zenodo.18086406).

## How to run the code?

1. Download the data from [this Zenodo archive](https://doi.org/10.5281/zenodo.18086406) and unpack the files. Store them in the `data` folder.
2. Clone or download this repository to your local computer.
3. Run the code. If you are familiarized with Docker we recommend you to follow option `a)`, which provides you an R running environment. Otherwise, you can follow option `b)`, which requires Rstudio and to install manually the necessary libraries.

    a) Download [Docker](https://docs.docker.com/get-docker/), open Docker Desktop, and download the following Docker image through your console:
      ```base
      docker pull claudiarodes/implications_sustainable_diets:diets_v2
      ```
      Run the docker image adjusting the full path to the repository folder:
      ```bash
      docker run -v /full_path_to_the_repository_folder/implications_sustainable_diets:/app -it implications_sustainable_diets 
      ```
      Run the `R/paper_analysis.R` script to produce all the figures of the study, both from the main manuscript and the supplementary information and the `R/paper_methodology.R` script to produce the graphics to illustrate the  ensemble design and uncertainty dimensions considered in the study.

    b) Download [RStudio](https://posit.co/products/open-source/rstudio/), open it, and run the `R/paper_analysis.R`script to produce all the figures of the study, both from the main manuscript and the supplementary information and the `R/paper_methodology.R` script in to produce the graphics to illustrate the  ensemble design and uncertainty dimensions considered in the study.


## Funding acknowledgement

<img src="./logo.png" alt="IAM COMPACT logos" width="130" height="40" align="left"/>
This project has received funding from the European Union's Horizon 2020 research and innovation program under grant agreement number 101056306 (IAM COMPACT project).



<br /><br />
For questions, contact claudia.rodes@bc3research.org.
