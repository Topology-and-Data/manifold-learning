# Manifold Learning

This is a pure-Julia reproduction of [this Python project on Manifold Learning](https://github.com/drewwilimitis/Manifold-Learning). The goal is to apply mathematical techniques in topological data analysis using Julia, a modern, general-purpose programming language.

## Setup

Download and install Julia 1.6+ from [the official source](https://julialang.org/downloads/).

### Install IJulia for Jupyter Notebooks
To use Jupyter Notebooks for Julia, run the Julia application (e.g., `path_to_julia/julia-1.6.0/bin/julia`) following which a window with a `julia>` prompt will appear. Type the below commands to install IJulia that tells the Jupyter server how to launch Julia.

```
using Pkg
Pkg.add("IJulia")
```
More detailed information on this is available in the [Julia docs](https://julialang.github.io/IJulia.jl/stable/manual/installation/).

### Set up virtual environment
It is strongly recommended to use [clean, independent virtual environments](https://pkgdocs.julialang.org/v1.6/environments/) for Julia projects.

#### From scratch
If setting up a new project from scratch, use the below steps (enter the package manager by pressing the `]` key in an IJulia shell):

```
shell> cd ~/path_to_project/manifold-learning
shell> julia

(@v1.6) pkg> activate .

(manifold-learning) pkg> status
    Status `~/path_to_project/manifold-learning/Project.toml
```

Once in the package manager shell, install any required packages (such as `Plots.jl` as normal).

```
(manifold-learning) pkg> add Plots
```

#### Use an existing environment

If using an existing environment from a clone of a GitHub repo, simply load and instantiate the existing environment from the `Project.toml` file. If the project contains a manifest (specified in `Manifest.toml`), this will install the packages in the same state that is given by that manifest. Otherwise, it will resolve the latest versions of the dependencies compatible with the project.

```
shell> julia

(@v1.6) pkg> activate .

(manifold-learning) pkg> instantiate

(manifold-learning) pkg> status
    Status `~/path_to_project/manifold-learning/Project.toml
```

#### Open Jupyter Notebook within the project's custom environment
To avoid any ambiguity with environments when using Jupyter Notebooks and Julia, **always** run the `jupyter notebook` command from the root directory of the project, i.e., the one that has the `Project.toml` file, and then navigate to the directory that houses the required notebooks to open them. This ensures that all project-specific packages are available within the Jupyter environment.



