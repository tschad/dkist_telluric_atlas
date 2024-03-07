## DKIST Telluric Atlases

This project use

## Project Setup 

FOR FIRST INITIALIZATIO
Download and install Py4CAtS Wheel file
Test 

```
git clone git@github.com:tschad/dkist_telluric_atlas.git
conda create -n dkist_telluric_atlas "python<3.12" pip ipympl tqdm
conda activate dkist_telluric_atlas

wget https://atmos.eoc.dlr.de/tools/Py4CAtS/py4cats-3.2.0-py3-none-any.whl
pip install py4cats-3.2.0-py3-none-any.whl
rm -rf py4cats-3.2.0-py3-none-any.whl


## for using jupyter lab with multiple kernels -- install kernel 
python -m ipykernel install --user --name=dkist_telluric_atlas

## test 
python -c "import py4cats"

```

To get the HITRAN database parameters 

Option 1 -- Directly from HITRAN database: 
Go to https://hitran.org/ and login if necessary 
Select 
