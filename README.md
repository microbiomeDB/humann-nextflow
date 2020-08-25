# Humann(+wget, kneaddata) in a Nextflow pipeline

Runs humann for a list of samples.

In:
- list of sample + fastq URLs, single or paired end
- config

Out:
- species tables from metaphlan
- abundances of ECs
- abundances of pathways
- coverages of pathways

## Install

pip3, metaphlan, and humann:
```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
~/.local/bin/pip3 install {cython, numpy, metaphlan, humann, kneaddata}
```

diamond:
```
wget http://github.com/bbuchfink/diamond/releases/download/v2.0.2/diamond-linux64.tar.gz
tar xzf diamond-linux64.tar.gz
```
minpath:
```
cd ~/lib
wget 'https://omics.informatics.indiana.edu/mg/get.php?justdoit=yes&software=minpath1.4.tar.gz' -O minpath1.4.tar.gz

```

trimmomatic:
```
cd ~/lib
wget 'http://www.usadellab.org/cms/uploads/supplementary/Trimmomatic/Trimmomatic-0.39.zip'
unzip *zip

```
databases:

```

kneaddata_database --download human_genome bowtie2 ~/kneaddata_databases/

humann_databases chocophlan full ~/humann_databases
humann_databases uniref uniref50_diamond ~/humann_databases
humann_databases utility_mapping full ~/humann_databases
```

Also the metaphlan_installation comes with its own chocophlan from 2019.

Using `uniref50_diamond`: might be revised to the EC filtered version.
