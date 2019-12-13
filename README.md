# sbx_spades [beta]

Sometimes we want to collecte all the aligned reads from the [**mapping**](https://github.com/sunbeam-labs/sunbeam/blob/dev/rules/mapping/mapping.rules) bam files and de novo assemble the reads using spades. 

## Install

To install:

    sunbeam extend https://github.com/sunbeam-labs/sbx_spades/

Paramaters for `sbx_spades` are automatically added to your `sunbeam_config.yml` on `sunbeam init`. If you're installing an extension in a project where you already have a config file, run the following to add the options for your newly added extension to your config (the `-i` flag means in-place config file modification; remove the `-i` flag to see the new config in stdout):

    sunbeam config update -i sunbeam_config.yml

See legacy instructions for older Sunbeam versions below.


## Running

This extension performs de novo assembly on reads mapped to targets in the `mapping` rules of Sunbeam--make sure you've added relevant mapping targets to your `sunbeam_config.yml` file!

To run:

  ```bash
  sunbeam run --configfile sunbeam_config.yml --use-conda all_spades
  ```

The `--use-conda` flag is required to let Snakemake know that you want to use the conda environment(s) included with your extension.

What's next?

Want to know whether your freshly assembled genomes are complete? Use your favoriate genome assessment tools, e.g. [checkM](http://ecogenomics.github.io/CheckM/), or simply the 139 single-copy genes for Bacteria species using [sbx_anvio](https://github.com/sunbeam-labs/sbx_anvio) 😳


----

## Install (legacy instructions for sunbeam <3.0)
 
 With your [sunbeam](https://github.com/sunbeam-labs/sunbeam) conda environment activated, 
 
 1. Clone into your Sunbeam directory:
 
  ```bash
  git clone https://github.com/zhaoc1/sbx_spades
  ```
 
 2. Add the new config options to your config file
 
  ```bash
  cat sunbeam/extensions/sbx_spades/config.yml >> sunbeam_config.yml
  ```

