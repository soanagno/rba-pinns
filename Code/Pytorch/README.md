# File description

```
"allen-cahn_enhancements.ipynb": Best convergence inlcuding the PINN enhancements (Section 3.1).
"allen-cahn_rba-sa.ipynb": Comparison of RBA vs SA vs Vanilla for the Allen-Cahn PDE (Section 3.4).
"helmholtz_rba-sa.ipynb": Comparison of RBA vs SA vs Vanilla for the Helmholtz PDE (Section 3.4).
```

# Instructions

Simply edit the constructor of the PINN class to activate each mode.
Make sure that either RBA or SA weights are activated but not both at the same time.

```
self.rba = 1  # activate RBA
self.sa = 0  # activate SA
self.first_opt = 30000  # Adam optimizer iterations
```

The RBA initialization can also be edited in the same constructor:

```
self.rsum = 0  # initial value
self.eta = 0.001  # learning rate
self.gamma = 0.999  # decay factor
self.init = 1  # initialization mode (1 or 2, see Algorithm 1)
```

The algorithm outputs the total loss, the realtive L2, the relative L infinity norm and the time (s)required for each iteration of the optimizer.
