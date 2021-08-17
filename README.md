# Example Notebook: Finding data for your research organism: Plants and RNA-Seq
# Delivered as a webinar for NCBI on August 18, 2021
## Adelaide Rhodes, Ph.D,


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ncbi/finding-data-demo-08-21/HEAD)

### What is this?

A Binder-compatible repo to support the demo notebook for this webinar. 
If you want to use this notebook on your own machine, be sure to install the requirements found in the binder folder.

`environment.yml` - conda installs for relevant python packages

`apt.txt` - tools loaded using `apt` on an ubuntu server (e.g. for samtools, type `sudo apt install samtools -y`

`postBuild` - postbuild installation script - these programs can be loaded on your notebook server by running this as a bash script

Access this Binder by clicking the blue badge above or at the following URL:

https://mybinder.org/v2/gh/Arhodes-NCBI/conda/HEAD


## Notes
The `environment.yml` file should list all Python libraries on which your notebooks
depend, specified as though they were created using the following `conda` commands:

```
conda activate example-environment
conda env export --from-history -f environment.yml
```

Note that the only libraries available to you will be the ones specified in
the `environment.yml`, so be sure to include everything that you need! 

Also note that if you skip the `--from-history`, conda may include OS-specific
packages in `environment.yml`, which you would have to manually prune from
`environment.yml`.  For example, confirmed macOS-specific packages that should
be removed are:

* libcxxabi=4.0.1
* appnope=0.1.0
* libgfortran=3.0.1
* libcxx=4.0.1
