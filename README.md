# PowSyBl Distribution

[![Actions Status](https://github.com/powsybl/powsybl-distribution/workflows/CI/badge.svg)](https://github.com/powsybl/powsybl-distribution/actions)
[![MPL-2.0 License](https://img.shields.io/badge/license-MPL_2.0-blue.svg)](https://www.mozilla.org/en-US/MPL/2.0/)
[![Slack](https://img.shields.io/badge/slack-powsybl-blueviolet.svg?logo=slack)](https://join.slack.com/t/powsybl/shared_invite/zt-rzvbuzjk-nxi0boim1RKPS5PjieI0rA)

PowSyBl (**Pow**er **Sy**stem **Bl**ocks) is an open source framework written in Java, that makes it easy to write complex
software for power systems’ simulations and analysis. Its modular approach allows developers to extend or customize its
features.

PowSyBl is part of the LF Energy Foundation, a project of The Linux Foundation that supports open source innovation projects
within the energy and electricity sectors.

<p align="center">
<img src="https://raw.githubusercontent.com/powsybl/powsybl-gse/main/gse-spi/src/main/resources/images/logo_lfe_powsybl.svg?sanitize=true" alt="PowSyBl Logo" width="50%"/>
</p>

Read more at https://www.powsybl.org !

This project and everyone participating in it is governed by the [PowSyBl Code of Conduct](https://github.com/powsybl/.github/blob/main/CODE_OF_CONDUCT.md).
By participating, you are expected to uphold this code. Please report unacceptable behavior to [powsybl-tsc@lists.lfenergy.org](mailto:powsybl-tsc@lists.lfenergy.org).

## PowSyBl vs PowSyBl Distribution

PowSyBl Distribution allows for the generation of a basic distribution of PowSyBl. It supports the following itools commands:

**Computation**
- [`compare-security-analysis-results`](https://www.powsybl.org/pages/documentation/user/itools/compare-security-analysis-results.html)
- [`loadflow`](https://www.powsybl.org/pages/documentation/user/itools/loadflow.html)
- [`loadflow-validation`](https://www.powsybl.org/pages/documentation/user/itools/loadflow-validation.html)
- [`security-analysis`](https://www.powsybl.org/pages/documentation/user/itools/security-analysis.html)
- [`action-simulator`](https://www.powsybl.org/pages/documentation/user/itools/action-simulator.html)
- [`sensitivity-computation`](todo)
- [`dynamic-simulation`](https://www.powsybl.org/pages/documentation/user/itools/dynamic-simulation.html)
- [`list-dynamic-simulation-models`](todo)

**Data conversion**
- [`convert-network`](https://www.powsybl.org/pages/documentation/user/itools/convert-network.html)
- [`cim-anonymizer`](https://www.powsybl.org/pages/documentation/user/itools/cim-anonymizer.html)

**Misc**
- [`plugins-info`](todo)

**Script**
- [`run-script`](https://www.powsybl.org/pages/documentation/user/itools/run-script.html)

## Getting started

To generate a basic PowSyBl distribution, you can then launch from the root repository:
```
$ cd <PROJECT_ROOT_PATH>
$ mvn clean package
```

The PowSyBl distribution is generated in the `<PROJECT_ROOT_PATH>/target` folder. For easier use of itools commands, adding
`<PROJECT_ROOT_PATH>/target/powsybl-distribution-<powsybldistribution.version>/bin` to your environment variable `PATH` is recommended.

Notes:
- Test network files in the [`resources`](https://github.com/powsybl/powsybl-distribution/tree/main/resources) folder are present
in the `etc` folder of the generated distribution.
- A configuration file is provided in this distribution but will be overriden by your local configuration file if you have one.

To learn more about how to use this basic PowSyBl distribution, go to our [beginner guide](https://www.powsybl.org/docs/todo.html).
