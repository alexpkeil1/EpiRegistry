Julia package registry to allow easy installation of:

- [Qgcomp.jl](https://github.com/alexpkeil1/Qgcomp.jl)
- [LSurvival.jl](https://github.com/alexpkeil1/LSurvival.jl)
- [PolyaGammaDistribution.jl](https://github.com/alexpkeil1/PolyaGammaDistribution.jl)


### How to:

- Get into package REPL [instructions here](https://juliateachingctu.github.io/Julia-for-Optimization-and-Learning/dev/lecture_03/pkg/)
- copy/paste this: `registry add https://github.com/alexpkeil1/EpiRegistry`

Then you can add any package (within the package REPL) using:
- `add Qgcomp`
- `add LSurvival`
- `add PolyaGammaDistribution`

Locally, this was built with:

("test.txt" file in the registry root folder, if present (uses LocalRegistry))
```
cd(regPath)
using LocalRegistry

register("../Qgcomp_julia/Qgcomp.jl", registry=regPath, push=false, commit=false)
register("../LSurvival.jl", registry=regPath, push=false, commit=false)
register("../PolyaGammaDistribution.jl", registry=regPath, push=false, commit=false, repo="https://github.com/alexpkeil1/PolyaGammaDistribution.jl.git")
```