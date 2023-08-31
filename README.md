# Ressources

```
ssh chadi@longleaf.unc.edu
```


First, starts the compute node by launching an interactive node.

```
srun -p jlessler --gres=gpu:1 --pty /bin/bash
```
Ensure that the hostname is `g1803jles01.ll.unc.edu` by typing command `hostname`

In VScode remote write:
````
Host uncidd-patronnode
  HostName g1803jles01.ll.unc.edu
  ProxyJump longleaf.unc.edu
  User yourusername
```
because we need to proxy through the login node as the computes nodes are not available from outside.

## Run the diffusion
Make sure on the upper right corner, that the conda environment kernel `Python (diffusion_torch)` is activated.

Create synthetic data from the `dataset_builder.ipynb` notebook, and run the inpainting forecast from `inpaintingFluForecasts.ipynb`
