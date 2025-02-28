# Install Ollama with AMD Support on Windows
## Install HIP SDK (ROCm)
**ROCm** are the official drivers from AMD meant to allow AI models to run on **AMD GPUs**.
They add a compatibility layer which allows programs meant to run with **CUDA** to run on an AMD GPU.\
\
Go to the official [AMD site](https://www.amd.com/en/developer/resources/rocm-hub/hip-sdk.html) to download and install it.

> Even if your GPU doesn't appear on the [HIP SDK compatibility chart](https://rocm.docs.amd.com/projects/install-on-windows/en/latest/reference/system-requirements.html#supported-gpus-win),
> install it. The **Ollama For AMD** script will automatically install the needed extra support.
## Find out your GPU model
To install the required software for your GPU, you will need to know your specific model.\
> **Example:** If you have a Radeon RX 6600, your model should be **gfx1032**
### Quickest Method
Open **cmd/powershell** and type 
``
clinfo | findstr "Device Name"
``
### Other methods
- Go to this [site](https://www.techpowerup.com/gpu-specs/) and search for your GPU. After finding it, use Ctrl+F to search for "gfx" in the specs.
- Ask chatgpt for the **LLVM target** of your GPU model (with the **Search** option on)

## Download and install [Ollama For AMD](https://github.com/likelovewant/ollama-for-amd) by [likelovewant](https://github.com/likelovewant)
We won't be installing the Ollama For AMD script directly. Instead we will use the [automated installer](https://github.com/ByronLeeeee/Ollama-For-AMD-Installer) developed 
by [ByronLeeeee](https://github.com/ByronLeeeee) that does all the hard work.\
Download the latest release of the installer and execute it. It will generate the following popup.\

## Check logs to find out if Ollama recognizes your AMD GPU
