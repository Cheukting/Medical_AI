

# Medical AI Project Setup Guide

This guide will help you set up Python and create a virtual environment for the the workshop that you will be attending.

## Downloading Python (CPython)

In this workshop, we recommend using Python 3.11

### For Windows Users:

1. Visit [Python's official website](https://www.python.org/downloads/)
2. Click on the "Download Python" button (latest stable version recommended)
3. Run the downloaded installer
4. Important: Check the box that says "Add Python to PATH" during installation
5. Click "Install Now"
6. Verify installation by opening Command Prompt and typing:
   ```
   python --version
   ```

### For Unix Users (macOS/Linux):

1. Visit [Python's official website](https://www.python.org/downloads/)
2. Download the latest stable version for your OS
   - For macOS: Download the macOS installer
   - For Linux: Many distributions come with Python pre-installed. If needed:
     ```bash
     # Ubuntu/Debian
     sudo apt update
     sudo apt install python3

     # Fedora
     sudo dnf install python3
     ```
3. Verify installation:
   ```bash
   python3 --version
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

## Setting Up Virtual Environment (.venv)

### For Windows Users:

1. Open Command Prompt
2. Navigate to your project directory:
   ```cmd
   cd path\to\Medical_AI
   ```
3. Create virtual environment:
   ```cmd
   python -m venv .venv
   ```
4. Activate virtual environment:
   ```cmd
   .venv\Scripts\activate
   ```

### For Unix Users (macOS/Linux):

1. Open Terminal
2. Navigate to your project directory:
   ```bash
   cd path/to/Medical_AI
   ```
3. Create virtual environment:
   ```bash
   python3 -m venv .venv
   ```
4. Activate virtual environment:
   ```bash
   source .venv/bin/activate
   ```

## Verifying Virtual Environment

After activation, you should see (.venv) at the beginning of your command prompt. You can verify the Python installation path:

```bash
# For both Windows and Unix
python -c "import sys; print(sys.executable)"
```

## Install Dependencies in Virtual Environment

1. Download the `requirements.txt` file in the folder of the  workshop that you are attending: 
    - [predictive analysis](predictive_analysis/requirements.txt)
    - [computer vision](computer_vision/requirements.txt)
    - [LLM](NLP_LLM/requirements.txt)
    
2. Install the dependencies:
   ```bash
   python -m pip install -r requirements.txt

## Deactivating Virtual Environment

When you're done working on the project:

```bash
deactivate
```

## Notes

- Always activate the virtual environment before working on the project
- The .venv directory is already included in .gitignore
- Use pip to install project dependencies after activating the virtual environment
