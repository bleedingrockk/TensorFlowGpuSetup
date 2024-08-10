# TensorFlow GPU Installation Guide

To ensure proper functionality and compatibility of the project, please follow these guidelines:

- **Library Versions:** Use the specific library versions listed below, as they are interdependent and require exact versions to function correctly.
- **GPU Requirement:** A GPU is necessary for TensorFlow GPU support to work on your PC.
- **Conda/Miniconda:** Ensure you have Conda or Miniconda installed, as these are required for managing the library dependencies.
- **Basic Knowledge:** Basic knowledge of how to use Conda is essential.
- **Command Execution:** Use Anaconda PowerShell or Command Prompt for running the necessary commands.

## INSTALL

1. **Create a Conda Environment**:
   
   ```bash
   conda create -n pygpuenv python=3.10
   
This command creates a new Conda environment named pygpuenv with Python version 3.10.

2. **Activate the Environment**:
   
   ```bash
   conda activate pygpuenv
   ```
   
Activate the newly created Conda environment.

3. **Install CUDA Toolkit and cuDNN:**:
   
   ```bash
   conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
   ```
   
Install CUDA Toolkit 11.2 and cuDNN 8.1.0.

4.**Install TensorFlow:**
   
   ```bash
   python -m pip install "tensorflow=2.10"
   ```

Install TensorFlow version 2.10.

## Test GPU
   
```python
# Your Python code here
import tensorflow as tf

# List all physical devices detected by TensorFlow
print("Physical devices:", tf.config.list_physical_devices('GPU'))
# Output: Physical devices: [PhysicalDevice(name='/physical_device:GPU:0', device_type='GPU')]

# Check if a GPU is available and can be used by TensorFlow
print("Is GPU available:", tf.test.is_gpu_available())
# Output: Is GPU available: True
```

## Troubleshooting
1.**Uninstall NumPy:**
```
pip uninstall numpy
```
2.**Install a compatible NumPy version:**
```
pip install numpy<2
```
These commands ensure that the NumPy version is compatible with TensorFlow 2.10.

### Contact [here](https://www.linkedin.com/in/suresh-suthar-800792182/) if you have any further doubts

