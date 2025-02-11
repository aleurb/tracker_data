# @title: setup.md
# @date : 2025-02-11 ALUR

Python version: 3.12
Python libraries: Pandas, NumPy, SeaBorn, MatPlotLib
Exact versions of libraries are saved in <requirements.txt>

# Create environment with Python
$ py -3.12 -m venv .venv
# Install dependencies
(.venv) $ python -m pip install --upgrade pip
(.venv) $ python -m pip install wheel setuptools
# 1) Install dependencies (specific versions)
(.venv) $ python -m pip install -r requirements.txt
# 2) Install fresh versions
(.venv) $ python -m pip install jupyter
(.venv) $ python -m pip install numpy pandas matplotlib seaborn
