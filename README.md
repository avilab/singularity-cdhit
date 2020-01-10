[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/3969)

# CD-HIT singularity image

## Download container

```bash
singularity pull --name avocado_container.sif shub://avilab/singularity-cdhit
```

## Run CD-HIT

```bash
singularity exec avocado_container.sif psi-cd-hit.pl -i contigs.fa -o clustered-contigs.fa -c 0.9 -G 1 -g 1 -prog megablast
```
