# Readme

## Jupyter
```
# Start
jupyter lab

```

## Jupyter kernels
```
# Create
python -m ipykernel install --user --name=myenv

# List
jupyter kernelspec list 

# Remove
jupyter kernelspec uninstall env 
```

## Python environment
```
# Create virtualenv
virtualenv --python=C:\Python36\python36.exe env

# Enable scripts
Get-ExecutionPolicy
Set-ExecutionPolicy Unrestricted -Scope Process

# activate
.\env\Scripts\activate.ps1

# deactivate
deactivate
```

## Fix python3.6
```
pip3.6 install --upgrade pip3.6 setuptools wheel
pip3.6 install -I tensorflow
pip3.6 install -I keras
```
