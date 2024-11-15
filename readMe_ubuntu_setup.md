
# Installation Guide

1. **Clone Bits and Bytes Repository**
   ```bash
   git clone https://github.com/bitsandbytes-foundation/bitsandbytes.git
   ```

2. **Run CUDA Installation Script**
   Change directory to `bitsandbytes` if needed, and install the required CUDA version:
   ```bash
   cd bitsandbytes
   python install_cuda.py 118
   ```

3. **Set CUDA Paths**
   Update your environment paths to ensure proper CUDA configuration:
   ```bash
   export PATH=/home/cap6411.student2/cuda/cuda-11.8/bin:$PATH
   export LD_LIBRARY_PATH=/home/cap6411.student2/cuda/cuda-11.8/lib64:$LD_LIBRARY_PATH
   ```

4. **Refresh Shell Configuration**
   Load the new configurations by refreshing `.bashrc`:
   ```bash
   source ~/.bashrc
   ```

5. **Verify CUDA Installation**
   - Check `nvcc` version:
     ```bash
     nvcc --version
     ```
   - Verify NVIDIA drivers with `nvidia-smi`:
     ```bash
     nvidia-smi
     ```

This setup guide ensures you load the necessary modules, install CUDA, and update your paths, enabling proper CUDA functionality for your project.
