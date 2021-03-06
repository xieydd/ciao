# Installation

## Requirements

- Jupyter Notebook v4.4.0 or above (We do not test other versions now.)
- Kubernetes v1.9 or above
- Kubeflow v0.2 or above
- S2I v1.1.10 or above
- Docker

## Get the kernel

We do not release any version of the kernel, so please build it from the source, please see the [Development Guide](./development.md).

## Setup Kubernetes and Kubeflow

Please see [Getting Started with Kubeflow](https://www.kubeflow.org/docs/started/getting-started/). Currently, we only support one-node cluster since we do not push the image to the Docker Registry.

## Install the Kernel

Run the script `hack/install.sh`, then the specification of the kernel will be installed to `${HOME}/.local/share/jupyter/kernels/kubeflow`, then Jupyter will know the information about Ciao.

## Run the Kernel

First, we need to set the environment variable `KUBECONFIG` to tell the kernel where to find the kubeconfig:

```bash
export KUBECONFIG={path to your kubeconfig}
```

Then run Jupyter Notebook or Lab, choose Kubeflow kernel.
