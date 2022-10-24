# RBNsims
(Updated for readability) Jupyter notebooks to run (noisy) Random Boolean Network simulations that generate synthetic gene expression data.

Paper reference: Kocaoglu, B; Alexander, W., _Degeneracy measures in biologically plausible random Boolean networks_. BMC Bioinformatics (2022) 23:71. ([open access link](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-022-04601-5))


In type-1 lesioning, only incoming edges were lesioned incrementally while it is possible (due to the pseudo-random algorithm to generate the logic functions) that outgoing edges stayed intact (for details see “Methods”). In the second type of lesioning (hence the name type-2 lesion), we lesioned all incoming and outgoing edges for randomly chosen nodes incrementally.

For classical RBNs, both types of lesioning result in an increase on degeneracy measures. That is, removing edges from the network paradoxically increased degeneracy. One reason for this may be that progressive lesioning increases the chances of a node becoming isolated. In the context of classical RBNs, the activity of the isolated node remains constant over time. However, a constant activity profile may also be a result of a function of a (set of) node(s) that is highly robust and yields same output over time. Therefore, the degeneracy metric might fall short in cases where the outputs of the isolated nodes remain static over time. Here, we hypothesize that degeneracy only works as a measure when all units have varying activity. 

The simulations here, thus, have varying activity as noisy bit-flip probability of 0.05. This probability can be adjusted in the code (line 55 in Sim Run cell) (see below, 'p') if one wishes to do so.

```python
...
 # ADD SMALL FLIPPY THING FOR ALL GENES - INCLUDING PERTURBED ONES
 for luckygene in range(n):
    coin = ['heads','tails']
    flip = np.random.choice(coin, p=[0.05, 0.95])
                        
```
