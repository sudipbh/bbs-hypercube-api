# HyperCube API

Let you access all your Data on HyperCube Data Platform 

visit https://www.hcube.io

# Requirements
- Python 3.6.2
- Pip

The HyperAPI package requires the HyperAPI_routes package, which is included as a wheel in the repository.
`.\resources\HyperAPI_routes-1-py3-none-any.whl`

# User Documentation

[Direct link](http://hyperapi-doc.s3-website.eu-west-3.amazonaws.com/29dc2abb-fc26-403e-bad0-0088c7640168/index.html)

# Quick installation

_on windows_

```pip install --upgrade HyperAPI -r requirements.txt``` 

_on linux/mac_

```pip3 install --upgrade HyperAPI -r requirements.txt```

Sample python code : 

```
from hdp_lib_api import Router
api = Router(token="<USER_TOKEN>", url="https://trial.hcube.io")

```


# Building and installing the HyperAPI module manually

### Building the python wheel

From the repository root folder, run the following command lines:

Set an environment variable `PACKAGE_VERSION` the define the version number for the HyperAPI. 

_on windows_

```set PACKAGE_VERSION=x``` 

_on linux/mac_

```export PACKAGE_VERSION=x```

Generate the HyperAPI wheel file. 

_on windows_

```python setup.py bdist_wheel```

_on linux/mac_

```python setup.py bdist_wheel```

The file will be generated on the in the `/dist` folder and be named HyperAPI-_x_-py3-none-any.whl _x_ being the provided version number.

### Installing the python wheels

Install the HyperAPI_routes package first:
_on windows_

```pip install /resources/HyperAPI_routes-1-py3-none-any.whl```

_on linux/mac_

```pip3 install /resources/HyperAPI_routes-1-py3-none-any.whl```

The HyperAPI wheel can then be installed directly using pip: 

_on windows_

```pip install /dist/HyperAPI-_x_-py3-none-any.whl```

_on linux/mac_

```pip3 install /dist/HyperAPI-_x_-py3-none-any.whl```

# Using the module from the source files 

- *Option 1:* run python from the source forlder.
- *Option 2:* add the HyperAPI folder to the python path.

# Running Tests

From the Repository root folder run the following command line:

_on windows_

```python -m unittest discover -s tests -p "*_test.py" -v```

_on linux/max_

```python3 -m unittest discover -s tests -p "*_test.py" -v```