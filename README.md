

# Medical AI Project Setup Guide

This guide will help you set up Miniconda with Python 3.12 and create a virtual environment for the workshop that you will be attending.

## Installing Miniconda

### For Windows Users:

1. Visit [Miniconda's official website](https://docs.conda.io/projects/miniconda/en/latest/)
2. Download the latest Windows installer (Miniconda3 Windows 64-bit)
3. Run the downloaded installer
4. During installation:
   - Select "Install for all users" or "Just Me" (recommended)
   - Check "Add Miniconda3 to my PATH environment variable"
5. Verify installation by opening Command Prompt and typing:
   ```
   conda --version
   ```

### For Unix Users (macOS/Linux):

1. Visit [Miniconda's official website](https://docs.conda.io/projects/miniconda/en/latest/)
2. Download the latest installer for your OS:
   - For macOS: Download the macOS installer (pkg or bash script)
   - For Linux: Download the Linux installer (bash script)
3. Install Miniconda:
   - For macOS pkg installer: Double click and follow the installation wizard
   - For bash script (macOS/Linux):
     ```bash
     bash ~/Downloads/Miniconda3-latest-*-x86_64.sh
     ```
   - Follow the prompts and say "yes" to initialize Miniconda
4. Close and reopen your terminal
5. Verify installation:
   ```bash
   conda --version
   ```

## Create a new directory for the project

### For Windows Users:

1. Open Command Prompt
2. Navigate to where you want to create the project directory:
   ```cmd
   cd path\to\desired\location
   ```
3. Create a new directory:
   ```cmd
   mkdir Medical_AI
   ```
4. Navigate into the project directory:
   ```cmd
   cd Medical_AI
   ```

### For Unix Users (macOS/Linux):

1. Open Terminal
2. Navigate to where you want to create the project directory:
   ```bash
   cd path/to/desired/location
   ```
3. Create a new directory:
   ```bash
   mkdir Medical_AI
   ```
4. Navigate into the project directory:
   ```bash
   cd Medical_AI
   ```

## Setting Up Conda Environment

### For Both Windows and Unix Users:

1. Open Command Prompt (Windows) or Terminal (macOS/Linux)
2. Navigate to your project directory:
   ```bash
   cd path/to/Medical_AI   # Use path\to\Medical_AI on Windows
   ```
3. Create a new conda environment with Python 3.12:
   ```bash
   conda create -n medical_ai python=3.12
   ```
4. Activate the conda environment:
   ```bash
   conda activate medical_ai
   ```

## Verifying Conda Environment

After activation, you should see (medical_ai) at the beginning of your command prompt. You can verify the Python installation:

```bash
# For both Windows and Unix
python --version  # Should show Python 3.12.x
conda list  # Shows all installed packages
```

## Install Dependencies in Conda Environment

1. Download the `requirements.txt` file in the folder of the workshop that you are attending: 
    - [predictive analysis](predictive_analysis/requirements.txt)
    - [computer vision](computer_vision/requirements.txt)
    - [LLM](NLP_LLM/requirements.txt)

2. Install the dependencies:
   ```bash
   conda install --file requirements.txt
   ```

   If some packages are not available through conda, you can use pip as a fallback:
   ```bash
   pip install -r requirements.txt
   ```

## Deactivating Conda Environment

When you're done working on the project:

```bash
conda deactivate
```

## Notes

- Always activate the conda environment before working on the project
- The environment name 'medical_ai' can be changed to your preference during creation
- Use conda to install dependencies when possible, falling back to pip when needed
