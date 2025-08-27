# PDM-artifacts
This repository contains the artifacts for the paper "PROBE+DETECT+MITIGATE (PDM): Enabling Cloud Tenants to Self-Defend against Microarchitectural Attacks".

# Detection (Datasets and Models)

The detection datasets and model artifact were tested with Python 3.9+. You will need the following Python packages:

pandas, numpy, torch, scikit-learn, joblib

You can install them with:

``` bash
pip install -r requirements.txt
```

Next, you can open the corresponding jupyter notebook for each environment (testbed or AWS Fargate) and run inference on each dataset.


# Mitigation Binaries
We provide precompiled ELF 64-bit binaries for evaluating the mitigation approach on different cryptographic primitives
Each binary can be executed in two modes, selected by a command-line argument:

``` bash
./ecdh 1
./ecdh 2
```

> **Execution Modes**
> - **1**: Run the primitive without protection  
> - **2**: Run the primitive with mitigation enabled


⚠️ Note: These binaries were compiled for x86-64 Linux with GNU libc. They may not run correctly on systems with different environments (e.g., macOS, non-glibc Linux distros). If you encounter issues, use the Docker container below.

For guaranteed reproducibility across machines, a ready-to-use Docker image is provided.
Run the container interactively:

``` bash
docker run --rm -it pdmanon123/pdm-artifacts
```

Inside the container, all required dependencies and binaries are pre-installed.

## Licenses
The dataset files contains are under the CC-BY-4 license. The source code presented in this repository are under the MIT License.

## Disclaimer
This repository is provided for academic purposes only.

