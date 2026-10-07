About sac-feedstock
===================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/sac-feedstock/blob/main/LICENSE.txt)


About sac
---------

Home: https://github.com/EarthScope/sac-community

Package license: Apache-2.0 AND BSD-2-Clause AND BSD-3-Clause AND LGPL-3.0-or-later

Summary: Seismic Analysis Code, community edition

Development: https://github.com/EarthScope/sac-community

Documentation: https://ds.iris.edu/files/sac-manual/index.html

SAC (Seismic Analysis Code) is a general purpose interactive program
designed for the study of sequential signals, especially time series
data. It is used in seismology for reading and writing binary seismic
data files, for filtering, spectral analysis and deconvolution, and for
interactive display of waveforms.

This is the community maintained continuation of SAC. In addition to the
`sac` interpreter the package contains the `saclst`, `sacswap`, `sgftops`,
`bbfswap` and `sgfswap` utilities, the headers, and the auxiliary data
(colour tables, travel-time tables, macros, ...) in the `aux` and `macros`
directories of the installation prefix. SAC finds that data through the
`SACAUX` environment variable, which is compiled into the binaries; the
`bin/sacinit.sh` and `bin/sacinit.csh` scripts set `SACHOME`, `SACAUX` and
`PATH` for a session.

The static libraries needed to link programs against SAC are in the
separate `sac-static` package.

About sac-static
----------------

Home: https://github.com/EarthScope/sac-community

Package license: Apache-2.0 AND BSD-2-Clause AND BSD-3-Clause AND LGPL-3.0-or-later

Summary: Static libraries of SAC (Seismic Analysis Code)

Development: https://github.com/EarthScope/sac-community

Documentation: https://ds.iris.edu/files/sac-manual/index.html

Static archives of the SAC libraries (`libsac.a`, `libsacio.a` and the
`sacio.a` compatibility name), for linking user programs against SAC,
e.g. the tools in `utils/` that ship with the `sac` package:

    $(sac-config -c) mytool.c $(sac-config -l sacio) -o mytool

The headers are in the `sac` package, which this package depends on.

Current build status
====================


<table><tr>
    <td>GitHub Actions</td>
    <td>
      <a href="https://github.com/conda-forge/sac-feedstock/actions/workflows/conda-build.yml">
        <img src="https://github.com/conda-forge/sac-feedstock/actions/workflows/conda-build.yml/badge.svg?event=push&branch=main">
      </a>
    </td>
  </tr>
    
  <tr>
    <td>Azure</td>
    <td>
      <details>
        <summary>
          <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=29737&branchName=main">
            <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/sac-feedstock?branchName=main">
          </a>
        </summary>
        <table>
          <thead><tr><th>Variant</th><th>Status</th></tr></thead>
          <tbody><tr>
              <td>osx_64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=29737&branchName=main">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/sac-feedstock?branchName=main&jobName=osx&configuration=osx%20osx_64_" alt="variant">
                </a>
              </td>
            </tr>
          </tbody>
        </table>
      </details>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-sac-green.svg)](https://anaconda.org/conda-forge/sac) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/sac.svg)](https://anaconda.org/conda-forge/sac) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/sac.svg)](https://anaconda.org/conda-forge/sac) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/sac.svg)](https://anaconda.org/conda-forge/sac) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-sac--static-green.svg)](https://anaconda.org/conda-forge/sac-static) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/sac-static.svg)](https://anaconda.org/conda-forge/sac-static) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/sac-static.svg)](https://anaconda.org/conda-forge/sac-static) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/sac-static.svg)](https://anaconda.org/conda-forge/sac-static) |

Installing sac
==============

Installing `sac` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

How to use
----------

<details>
<summary>With conda</summary>

```
conda install sac sac-static
```

</details>

<details>
<summary>With mamba</summary>

```
mamba install sac sac-static
```

</details>

<details>
<summary>With pixi</summary>

```
# for adding to your local project
pixi add sac sac-static
# for installing globally
pixi global install sac sac-static
```

</details>

Search package versions
-----------------------

It is possible to list all of the versions of `sac` available on your platform:

<details>
<summary>With conda</summary>

```
conda search sac --channel conda-forge
```

</details>

<details>
<summary>With mamba</summary>

```
mamba search sac --channel conda-forge
```

</details>

<details>
<summary>With pixi</summary>

```
pixi search sac --channel conda-forge
```

</details>

<details>
<summary>With mamba repoquery, which may provide more information</summary>

```
# Search all versions available on your platform:
mamba repoquery search sac --channel conda-forge

# List packages depending on `sac`:
mamba repoquery whoneeds sac --channel conda-forge

# List dependencies of `sac`:
mamba repoquery depends sac --channel conda-forge
```

</details>


About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/), [GitHub](https://github.com/),
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/),
[Drone](https://cloud.drone.io/welcome), and [TravisCI](https://travis-ci.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [anaconda.org](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance,
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information, please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating sac-feedstock
======================

If you would like to improve the sac recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/sac-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@claudiodsf](https://github.com/claudiodsf/)

