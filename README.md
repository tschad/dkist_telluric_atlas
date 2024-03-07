## DKIST Telluric Atlases

The goal of this project rep is to document how to create transmission absorption spectra for terrestrial atmospheres, in particular for DKIST. 

## Project Setup 

### Initial setup of the conda environment 



Get tarball file wi

```
wget -nH https://atmos.eoc.dlr.de/tools/Py4CAtS/py4cats.tgz
tar zxvf py4cats.tgz


## get the python wheel file for py4CaAts and install
##wget https://atmos.eoc.dlr.de/tools/Py4CAtS/py4cats-3.2.0-py3-none-any.whl
##pip install py4cats-3.2.0-py3-none-any.whl
##rm -rf py4cats-3.2.0-py3-none-any.whl

## test 
python -c "import py4cats"

```

### HiTRAN database parameters 

mkdir HITRAN_VIS_IR 
cd HITRAN_VIS_IR

To get the HITRAN database parameters:

#### Option 1:  Previously querys on Hitran.org: 

wget https://hitran.org/results/65e912c9.par
wget https://hitran.org/results/65e912c9.bib.html
wget https://hitran.org/results/65e912c9.bib
wget https://hitran.org/output-format-readmes/readme-1.txt

(dkist_telluric_atlas) [tschad@cn7 HITRAN_VIS_IR]$ ls -lath 
total 221M
drwxrwxr-x 2 tschad dkist    6 Mar  6 15:08 .
drwxrwxr-x 3 tschad dkist    3 Mar  6 15:06 ..
-rw-rw-r-- 1 tschad dkist 174K Mar  6 15:05 65e912c9.bib
-rw-rw-r-- 1 tschad dkist 249K Mar  6 15:05 65e912c9.bib.html
-rw-rw-r-- 1 tschad dkist 220M Mar  6 15:05 65e912c9.par
-rw-rw-r-- 1 tschad dkist 3.5K Jun 14  2023 readme-1.txt

cd ../

#### Option 2 -- Regenerate queried data on Hitran.org 

Go to https://hitran.org/ 
Select Data Access > Line-by-Line Search 
Select first 7 individual molecules on top (these are the 'main' molecules)
Click "select isotopologues"
Click "Select wavenumber / wavelength range" (accepting default isotopologues )
Enter range of wavenumbers:  vmin = 1990; vmax = 28600 (this covers ~350 to 5000 nm)
Click "select output options"
login if necessary 
Selection *.par (160 chars) output on left and click "Start Data Search"
Download all 4 files generated and place in an accessible folder 

### Run example notebook 
