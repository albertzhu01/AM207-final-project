# AM207-final-project

In this repository, you will find the following Jupyter notebook ``TBLG-PSO.ipynb`` and a bunch of folder names ``N_{n}`` where ``n`` is between 4 and 9 inclusive.

``TBLG-PSO.ipynb`` is where the PSO is implemented. The comments in the notebook should be sufficient to help you understand what is going on (hopefully).

Each of the folders contains the files for running DFT on twisted bilayer graphene for a particle twist angle. The number ``n`` is defined as follows: a moire supercell is defined by lattice vectors that have magnitude ``n * a1`` and ``(n + 1) * a2`` (if this doesn't make sense, that's fine. The exact formulas aren't crucial, just know that each folder contains the DFT simulations for a specific twist angle. If you're curious, see reference 5 in my writeup for more information). Within each folder, there are 3 folders called ``DFT-structures``, ``PSO-2params``, and ``PSO_z``, which correspond to the baseline, PSO-1, and PSO-2 in my writeup, respectively. For ``N_4``, each of the 3 folders also has a subfolder called ``unrelaxed``, which contains the atomic forces of the initial structures R_0, R_{PSO-1}, and R_{PSO-2} defined in my writeup.

The important part is that you can run the PSO implementations in the notebook, and then there are cells that write the results of PSO to a file called ``structure.fdf`` in one of the folders, which will be used as input to the DFT relaxations. If you have access to the Siesta DFT software, you can then run Siesta using the ``run.script`` file provided in each of the folders.