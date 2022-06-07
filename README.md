# RBNsims
Jupyter notebooks to run Random Boolean Network simulations.

Paper reference: Kocaoglu, B; Alexander, W., _Degeneracy measures in biologically plausible random Boolean networks_. BMC Bioinformatics (2022) 23:71. ([open access link](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-022-04601-5))


For classical RBNs, both types of lesioning result in an increase on degeneracy measures. That is, removing edges from the network paradoxically increased degeneracy. One reason for this may be that progressive lesioning increases the chances of a node becoming isolated. In the context of classical RBNs, the activity of the isolated node remains constant over time. However, a constant activity profile may also be a result of a function of a (set of) node(s) that is highly robust and yields same output over time. Therefore, the degeneracy metric might fall short in cases where the outputs of the isolated nodes remain static over time. Here, we hypothesize that degeneracy only works as a measure when all units have varying activity. 

Simulations here have varying activity as noisy bit-flip probability of 0.05. This probability can be adjusted in the code as one wishes to do so.

```python
s = "Python syntax highlighting"
print s
```
