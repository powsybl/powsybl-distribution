# PowSyBl Distribution

[![Actions Status](https://github.com/powsybl/powsybl-distribution/workflows/CI/badge.svg)](https://github.com/powsybl/powsybl-distribution/actions)
[![MPL-2.0 License](https://img.shields.io/badge/license-MPL_2.0-blue.svg)](https://www.mozilla.org/en-US/MPL/2.0/)
[![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/powsybl)

PowSyBl (**Pow**er **Sy**stem **Bl**ocks) is an open source framework written in Java, that makes it easy to write complex
software for power systems’ simulations and analysis. Its modular approach allows developers to extend or customize its
features.

PowSyBl is part of the LF Energy Foundation, a project of The Linux Foundation that supports open source innovation projects
within the energy and electricity sectors.

<p align="center">
<img src="https://raw.githubusercontent.com/powsybl/powsybl-gse/master/gse-spi/src/main/resources/images/logo_lfe_powsybl.svg?sanitize=true" alt="PowSyBl Logo" width="50%"/>
</p>

Read more at https://www.powsybl.org !

This project and everyone participating in it is governed by the [PowSyBl Code of Conduct](https://github.com/powsybl/.github/blob/master/CODE_OF_CONDUCT.md).
By participating, you are expected to uphold this code. Please report unacceptable behavior to [powsybl-tsc@lists.lfenergy.org](mailto:powsybl-tsc@lists.lfenergy.org).

## PowSyBl vs PowSyBl Distribution

PowSyBl Distribution allows the generation of a basic distribution of PowSyBl. It supports the following itools commands:

**Computation**
- [`compare-security-analysis-results`](https://www.powsybl.org/docs/tools/compare-security-analysis-results.html)
- [`loadflow`](https://www.powsybl.org/docs/tools/loadflow.html)
- [`loadflow-validation`](https://www.powsybl.org/docs/tools/loadflow-validation.html)
- [`security-analysis`](https://www.powsybl.org/docs/tools/security-analysis.html)


**Data conversion**
- [`convert-network`](https://www.powsybl.org/docs/tools/convert-network.html)

**Misc**
- [`plugins-info`](https://www.powsybl.org/docs/tools/plugins-info.html)

**Script**
- [`run-script`](https://www.powsybl.org/docs/tools/run-script.html)

## Getting started

Create a `.itools` folder in your `${HOME}` if it does not exist and copy the [configuration file](resources/config/config-distrib.yml) in it:
```
$ cp ${PROJECT_ROOT_PATH}/resources/config/config-distrib.yml ${HOME}/.itools/config-distrib.yml
```

NB: Please note that this distribution **will not** take your personal `config.yml` file into account if you have one.

To generate a PowSyBl basic distribution, you can then launch from the root repository:
```
$ cd ${PROJECT_ROOT_PATH}
$ mvn clean package
```

The PowSyBl distribution is generated in the `${PROJECT_ROOT_PATH}/target` folder.