# sbx_spades

Sometimes we want to collecte all the aligned reads from the [**mapping**](https://github.com/sunbeam-labs/sunbeam/blob/dev/rules/mapping/mapping.rules) bam files and de novo assemble the reads using spades or velvet. 

## Usage
 
 With you [sunbeam](https://github.com/sunbeam-labs/sunbeam) conda environemnt activated, 
 
 1. Clone into your Sunbeam directory:
 
  ```bash
  git clone https://github.com/zhaoc1/sbx_spades
  ```
 
 2. Add the new config options to your config file
 
  ```bash
  cat sunbeam/extensions/sbx_spades/config.yml >> sunbeam_config.yml
  ```
 
 3. Run time

  ```bash
  snakemake --configfile sunbeam_config.yml all_spades
  ```
 4. What's next?
 
  Want to know whether your freshly assembled genomes are complete? Use your favoriate genome assessment tools, e.g. [checkM](http://ecogenomics.github.io/CheckM/), or simply the 139 single-copy genes for Bacteria species using [sbx_anvio](https://github.com/sunbeam-labs/sbx_anvio) 😳

