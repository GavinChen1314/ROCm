# ROCm installation options (Linux)

Users installing ROCm must choose between various installation options. A new
user should follow the [Quick Start guide](../../quick-start/linux).

## Package manager versus AMDGPU installer

ROCm supports two methods for installation:

* Directly using the Linux distribution's package manager
* The `amdgpu-install` script

There is no difference in the final installation state when choosing either
option.

Using the distribution's package manager lets the user install,
upgrade and uninstall using familiar commands and workflows. Third party
ecosystem support is the same as your OS package manager.

The `amdgpu-install` script is a wrapper around the package manager. The same
packages are installed by this script as the package manager system.

The installer automates the installation process for the AMDGPU
and ROCm stack. It handles the complete installation process
for ROCm, including setting up the repository, cleaning the system, updating,
and installing the desired drivers and meta-packages. Users who are
less familiar with the package manager can choose this method for ROCm
installation.

(installation-types)=

## Single-version versus multi-version ROCm install

ROCm packages are versioned with both semantic versioning that is package
specific and a ROCm release version.

### Single-version installation

The single-version ROCm installation refers to the following:

* Installation of a single instance of the ROCm release on a system
* Use of non-versioned ROCm meta-packages

### Multi-version installation

The multi-version installation refers to the following:

* Installation of multiple instances of the ROCm stack on a system. Extending
  the package name and its dependencies with the release version adds the
  ability to support multiple versions of packages simultaneously.
* Use of versioned ROCm meta-packages.

```{attention}
ROCm packages that were previously installed from a single-version installation
must be removed before proceeding with the multi-version installation to avoid
conflicts.
```

```{note}
Multi-version install is not available for the kernel driver module, also referred to as AMDGPU.
```

The following image demonstrates the difference between single-version and
multi-version ROCm installation types:

![ROCm installation types](../../../data/tutorials/install/linux/linux001.png "ROCm installation types")
