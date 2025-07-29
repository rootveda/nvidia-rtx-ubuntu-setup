# Nvidia RTX Driver Installation Guide for Ubuntu

This repository provides step-by-step instructions for installing the official Nvidia RTX drivers on Ubuntu systems.

## Prerequisites

- An Nvidia RTX GPU
- Ubuntu Linux (any recent version)
- Terminal access with sudo privileges


## Installation Steps

1. **List Available Nvidia Drivers**

Open a terminal and run:

```bash
sudo ubuntu-drivers list
```

2. **Install the Recommended Nvidia Driver**

To automatically install the appropriate driver for your system:

```bash
sudo ubuntu-drivers install
```

3. **Verify Driver Installation**

After installation is complete, check your Nvidia driver version with:

```bash
cat /proc/driver/nvidia/version
```


## Verify with `nvidia-smi`

After installing the Nvidia driver, use the following command to confirm the GPU is active and the driver is functioning:

```bash
nvidia-smi
```

This should display information about your Nvidia GPU, driver version, CUDA version, and GPU activity.

### Example Output

```markdown
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 575.64.03              Driver Version: 575.64.03      CUDA Version: 12.9     |
|-----------------------------------------+------------------------+----------------------+
| GPU  Name                 Persistence-M | Bus-Id          Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |           Memory-Usage | GPU-Util  Compute M. |
|                                         |                        |               MIG M. |
|=========================================+========================+======================|
|   0  NVIDIA GeForce RTX 5090        Off |   00000000:01:00.0  On |                  N/A |
|  0%   33C    P8             11W /  600W |     424MiB /  32607MiB |      0%      Default |
|                                         |                        |                  N/A |
+-----------------------------------------+------------------------+----------------------+

```

## Troubleshooting

- If you encounter issues, check hardware compatibility and ensure your system is up to date.
- For more details, consult the official Ubuntu documentation on Nvidia drivers.


## License

This project is provided for educational purposes. For official driver distribution and licensing, see Nvidia's website.
