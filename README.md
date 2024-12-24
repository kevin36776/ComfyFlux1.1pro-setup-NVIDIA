# ComfyFlux1.1pro-setup-NVIDIA
How to setup Comfy and Flux 1.1 pro raw &amp; ultra in Git Bash. NVIDIA GPU.

----------------------------------------------------------------------------------

Open Git Bash. Make sure you have python installed:

Check if Python is installed:

python --version

If not found, install Python first:

winget install Python.Python.3.11

--------------------------------------------------------------------------------------

These steps include adding a virtual environment for your files.

Continue with these steps:

Create and activate virtual environment:

python -m venv venv
source venv/Scripts/activate

---------------------------------------------------------------------------------------

Clone ComfyUI:

git clone https://github.com/comfyanonymous/ComfyUI

Install PyTorch with CUDA support:

python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

Install ComfyUI requirements:

pip install -r requirements.txt

Install Flux node:

cd custom_nodes
git clone https://github.com/ShmuelRonen/ComfyUI_Flux_1.1_RAW_API

Configure Flux API (if using):

cd ComfyUI_Flux_1.1_RAW_API
# Edit config.ini with your API key

Run ComfyUI:

cd ComfyUI
python main.py
To restart later:
cd ComfyUI
source venv/Scripts/activate
cd ComfyUI
python main.py
