# 🧠 Deep Learning Training Guide

This repository is designed to help you set up your environment for running deep learning models, especially with TensorFlow and GPU support on Windows (NVIDIA GPU).

---

## ✅ Requirements
- Anaconda or Miniconda (Download from [Anaconda](https://www.anaconda.com/download/success))
- NVIDIA GPU (Optional, for acceleration)
- VS Code (Recommended for running Notebooks)

---

## 🛠️ Setup Instructions

### 1. Install Anaconda / Miniconda
👉 Download and install from [https://www.anaconda.com/download/success](https://www.anaconda.com/download/success)

---

### 2. Create a Virtual Environment
Open **Anaconda Prompt** and run:
```bash
conda create -n your_env_name python=3.10 anaconda
```

### 3. Activate the Environment
``` bash
conda activate your_env_name
```

### 4. Install TensorFlow (Choose based on your setup)
💻 With NVIDIA GPU Support (Recommended):
``` bash
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
python -m pip install "tensorflow<2.11"
```

💻 Without GPU Support:
``` bash
python -m pip install "tensorflow<2.11"
```

### 5. Install Project Dependencies
📜 Option 1: If you're in the project directory:
``` bash
pip install -r requirements.txt
```

📂 Option 2: Specify the path to requirements.txt
``` bash
pip install -r path/to/your/requirements.txt
```

📦 Option 3: Manually install the required packages using pip.

### 6. Install Visual Studio Code (VS Code)
👉 Download from https://code.visualstudio.com/
✅ Install the Jupyter Notebook extension from the VS Code extensions marketplace.

### 7. Load the Training Notebook
Open your `.ipynb` file in VS Code.

### 8. Select the Correct Kernel
On the top right, click `"Select Kernel"`
Choose your Anaconda environment (the one you created earlier).

### 9. ✅ Train your Model!
Run the cells and start training 🚀


### 📌 Notes
TensorFlow 2.11 and above drops GPU support for native Windows. That's why we use `tensorflow<2.11`.
Make sure your NVIDIA GPU drivers and CUDA are properly set up if running with GPU.
