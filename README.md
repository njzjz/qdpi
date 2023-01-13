# QDπ: Quantum Deep Potential Interaction Model for Drug Discovery

## Versions

### v1.0

Model file: [qdpi-1.0.pb](./qdpi-1.0.pb)

Supported elements: C, H, O, N

Citation: Jinzhe Zeng, Yujun Tao, Timothy J Giese, Darrin M York, QDπ: Quantum Deep Potential Interaction Model for Drug Discovery, Journal of Chemical Theory and Computation, 2023, DOI: [10.1021/acs.jctc.2c01172](https://doi.org/10.1021/acs.jctc.2c01172).


## Usage

### General usage

$$
E_{QD\pi} = E_{DFTB3} + E_{NNP}
$$

To calculate DFTB3 energy, you can use either [AMBERTools](https://ambermd.org/) or [DFTB+](https://github.com/dftbplus/dftbplus), or any software that can produce the same potential energies.

To calculate NNP energy, you have to use [DeePMD-kit](https://github.com/deepmodeling/deepmd-kit).

### Python interface

A dpdata driver plugin is provided in [njzjz/dpdata_qdpi](https://github.com/njzjz/dpdata_qdpi) to use the QDπ model. Note that the dpdata driver provides an interface to convert to an ASE calculator.

### MD simulation

[AmberDPRc](https://gitlab.com/RutgersLBSR/AmberDPRc) supports both DFTB3 and DeePMD-kit. To use the QDπ model, set `intrafile(1)="qdpi-1.0.pb"` in [NVTMD.mdin](https://gitlab.com/RutgersLBSR/AmberDPRc/-/blob/main/examples/AmberInputQuickReference/NVTMD.mdin).
