# NEURON tutorial for implementing simulations of thalmamic relay neurons
```
Alain Destexhe
Laboratory for Computational Neuroscience
Unité de Neurosciences Intégratives et Computationnelles (UNIC)
Centre National de la Recherche Scientifique (CNRS)
91198 Gif-sur-Yvette, France 
```

Formerly from (when this work was created):
```
Department of Physiology, Laval University,
Quebec G1K 7P4, Canada

Destexhe@iaf.cnrs-gif.fr
http://cns.iaf.cnrs-gif.fr/Main.html
```

This package is running with the NEURON simulation program written by Michael
Hines and available on internet at:
- [https://neuron.yale.edu](https://neuron.yale.edu)
- [https://nrn.readthedocs.io](https://nrn.readthedocs.io)

The package contains mechanisms (`.mod` files) and programs (`.oc` files) needed
to simulate different models of thalamocortical (TC) relay neurons, relative
to the paper:

Destexhe A, Neubig M, Ulrich D and Huguenard JR. Dendritic low-threshold calcium currents in thalamic relay cells. *Journal of Neuroscience* 18: 3574-3588, 1998. [https://pubmed.ncbi.nlm.nih.gov/9570789/](https://pubmed.ncbi.nlm.nih.gov/9570789/)

  
## Programs

- `tc1_cc.oc` - current clamp in 1-compartment TC cell
- `tc3_cc.oc` - current clamp in 3-compartment TC cell
- `tc200_cc.oc` - current clamp in 200-compartment TC cell (intact cell)
- `tc200_vc.oc` - voltage clamp in 200-compartment TC cell (intact cell)
- `tcD_cc.oc` - current clamp in 8-compartment TC cell (dissociated cell)
- `tcD_vc.oc` - voltage clamp in 8-compartment TC cell (dissociated cell)


## Mechanisms
- `hh2.mod` - fast sodium spikes (Na and K currents)
- `ITGHK.mod`	- T-type calcium current of TC cells
- `cadecay.mod` - intracellular calcium dynamics
- `VClamp.mod` - mechanism for single-electrode voltage-clamp


## How to run

Use autolaunch on modeldb or:

### unix platform:

To compile the demo, NEURON and INTERVIEWS must be installed and working on
the machine you are using.  Just type `nrnivmodl` to compile the mechanisms
given in the mod files.

Then, execute the main demo program by typing:

```
nrngui mosinit.hoc
```
### mswin platform:

Compile the mechanism (mod) files by using `mknrndll`.  Then start the simulation
by clicking on `mosinit.hoc` in windows explorer.

### back to any platform:

Once the menu and graphics interface has appeared, click on a simulation from
the Simulations of TC cells window.  Then click on "Init and Run"
button to start the simulation on the RunControl window.  If you do not see a RunControl
window you can bring it to the front by selecting it under Tools from the NEURON main menu.

For more information about how to get NEURON and how to install it, please
refer to the following sites:
- [https://neuron.yale.edu](https://neuron.yale.edu)
- [https://nrn.readthedocs.io](https://nrn.readthedocs.io)


For further information, please contact:

```
Alain Destexhe
Laboratory for Computational Neuroscience
Unité de Neurosciences Intégratives et Computationnelles (UNIC)
Centre National de la Recherche Scientifique (CNRS)
91198 Gif-sur-Yvette, France 

Destexhe@iaf.cnrs-gif.fr
http://cns.iaf.cnrs-gif.fr/Main.html
```

## Changelog

- Further updated 7/10/05 for button restart fix.
- model version 10/28/02 updated to neuron 5.2.
- readme standardized to markdown, NEURON and PubMed links updated 12/01/23.
