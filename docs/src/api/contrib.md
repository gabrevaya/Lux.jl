```@meta
CurrentModule = Lux
```

All features listed on this page are **experimental** which means:

  1. No SemVer Guarantees. We use code here to iterate fast and most users should wait for
     these features to be marked non-experimental.
  2. The code will probably be moved into a separate repository in the future.
  3. Expect edge-cases and report them. It will help us move these features out of
     experimental sooner.
  4. None of the features are exported.

## Training

!!! note
    This module will be moved into a separate package in the near future.

Helper Functions making it easier to train `Lux.jl` models.

Lux.Training is meant to be simple and provide extremely basic functionality. We provide
basic building blocks which can be seamlessly composed to create complex training pipelines.

```@docs
Lux.Training.AbstractVJP
Lux.Training.backend
Lux.Training.EnzymeVJP
Lux.Training.YotaVJP
Lux.Training.ZygoteVJP
Lux.Training.TrainState
Lux.Training.compute_gradients
Lux.Training.apply_gradients
```

### Why VJP rules when we already have [AbstractDifferentiation.jl](https://github.com/JuliaDiff/AbstractDifferentiation.jl/)?

In the long term, the goal is to just use AD.jl directly. However, there are current
refactors being planned (See [this issue](https://github.com/EnzymeAD/Enzyme.jl/issues/349#issuecomment-1144514285)).
Once the package is stable and we have the necessary backend support, we will be dropping
the VJP rules in this module.

## Index

```@index
Pages = ["contrib.md"]
```
