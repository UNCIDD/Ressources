A description of ressources available for the UNC-IDD group. For the moment, concentrate on computing ressources.

## Accessing the Patron node from VScode


First, SSH on longleaf cluster:
 ```
 ssh [your_username]@longleaf.unc.edu
 ```
and start the compute node by launching an interactive job on it:
 ```
 srun -p jlessler --gres=gpu:1 --pty /bin/bash
 ```
Here, you can see that the hostname is `g1803jles01.ll.unc.edu`, by typing command `hostname`. Then, the rest is done from your computer:
In VScode, install these three extensions:
<img width="407" alt="Screenshot 2023-10-04 at 12 21 18" src="https://github.com/UNCIDD/Ressources/assets/7485811/0c10ae10-837a-4412-a025-bfc4d8da1644">

And add a remote config with
 ````
 Host uncidd-patronnode
   HostName g1803jles01.ll.unc.edu
   ProxyJump longleaf.unc.edu
   User [your_username]
 ```
 We use a proxyjump because we need to go through the login node to access the compute nodes.

You can now run your notebook, choosing the right enviroment in the upper right corner.
