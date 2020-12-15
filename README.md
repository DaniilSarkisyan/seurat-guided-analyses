# seurat-guided-analyses

Can not get docker container `satijalab/seurat` to work: container exits immediately, 
when I try to `docker start` it, R complains that it is not interactive.
Perhaps `CMD["/init"]` is missing in the Dockerfile to enable RStudio

Following http://bioinformatics.sph.harvard.edu/knowledgebase/scrnaseq/rstudio_sc_docker.html
I installed Seurat_3.9.9.9003 from https://github.com/vbarrera/docker_configuration, pulling
docker container vbarrerab/singlecell-base:R.4.0.3-BioC.3.11-ubuntu_20.04

```R
sudo docker run \
  -v /home/daniil/Documents:/home/rstudio/Documents \
  -e USER='rstudio' -e PASSWORD='???' -e ROOT=TRUE \
  -d -p 8787:8787 --name seurat \
  vbarrerab/singlecell-base:R.4.0.3-BioC.3.11-ubuntu_20.04
```

Now testing the Guided Analyses from https://satijalab.org/seurat/vignettes.html

## https://satijalab.org/seurat/v3.2/pbmc3k_tutorial.html

works ok

