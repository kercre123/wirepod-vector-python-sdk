
# Anki/DDL Vector - Python SDK
by cyb3rdog

## With support for any bot on wire-pod!
(theoretically) Compatible with Ubuntu 16.04 - 22.04 and Python 3.6.1 - 3.11

This is the extended fork of the original Anki Vector Python SDK.

Originally forked by [cyb3rdog](https://github.com/cyb3rdog/vector_python_sdk), then forked by [MoonDog83](https://github.com/MoonDog82/vector-python-sdk) who added 3.11 support and regenerated the proto, and finally forked by me (kercre123).

![Vector](docs/source/images/vector-sdk-alpha.jpg)


## Getting Started

I am hosting SDK documentation here: [https://keriganc.com/sdkdocs](https://keriganc.com/sdkdocs)

The documentation contains installation guides, helpful tips, walkthroughs, and function descriptions which will help you use the thing.

### Python Installation

#### Windows:

If you dont have python installed yet, download and install it from the [Python.org](https://www.python.org/downloads/windows/).
Make sure to tick the “Add Python 3.X to PATH” checkbox on the Setup screen.

To avoid dificulties during the SDK install on your existing python installation, open the command line and run:

```
py -m pip install -U pip
py -m pip install --upgrade setuptools
```

#### Linux:

Open the Terminal and run following commands to install and update the Python, and packages required by SDK:

```
sudo apt-get update
sudo apt-get install -y python3 python3-pip python3-tk python3-pil.imagetk build-essential libssl-dev libffi-dev freeglut3
```

If you are using Python 3.11 or abnove, create a file at ~/.config/pip/pip.conf with the following text:

```
[global]
break-system-packages = true
```

### SDK Installation

 - Note: Use either **```pip```** or **```pip3```** correspondingly to the Python version you are using.

In case you have previously installed the original ***Anki*** or ***Ikkez*** SDK, uninstall it/them with following command(s):

- ```pip uninstall anki_vector``` or ```pip3 uninstall anki_vector```
- ```pip uninstall ikkez_vector``` or ```pip3 uninstall ikkez_vector```
- ```pip uninstall cyb3r_vector_sdk``` or ```pip3 uninstall cyb3r_vector_sdk```

To install this new SDK, run:

- ```pip install wirepod_vector_sdk``` or ```pip3 install wirepod_vector_sdk```
and
- ```pip install "wirepod_vector_sdk[3dviewer]"``` or ```pip3 install "wirepod_vector_sdk[3dviewer]"```


To upgrade this SDK to its latest version, use:

- ```pip install wirepod_vector_sdk --upgrade``` or ```pip3 install wirepod_vector_sdk --upgrade```


If you want to know where the SDK files are installed, use following command:

- Windows:  ```py -c "import anki_vector as _; print(_.__path__)"```
- Linux:    ```python3 -c "import anki_vector as _; print(_.__path__)"```


### SDK Configuration

To authenticate a bot with the SDK (works when bot is connected to wire-pod):

- Windows:  **```py -m anki_vector.configure```**
- Linux:    **```python3 -m anki_vector.configure```**

### Log Level

In order to change the log level to other then default value of `INFO`, set the `VECTOR_LOG_LEVEL` enviroment variable:

Allowed values are:
```
CRITICAL	= 50
FATAL 		= CRITICAL
ERROR 		= 40
WARNING 	= 30
WARN 		= WARNING
INFO 		= 20
DEBUG 		= 10
```

Example:

- Windows: ```SET VECTOR_LOG_LEVEL=DEBUG```
- Lunux:   ```VECTOR_LOG_LEVEL="DEBUG"```


### Documentation

You can generate a local copy of the SDK documetation by
following the instructions in the `docs` folder of this project.

Learn more about Vector: https://www.anki.com/en-us/vector

Learn more about how Vector works: [Vector Bible](https://github.com/GooeyChickenman/victor/blob/master/documentation/Vector-TRM.pdf)

Learn more about the SDK: https://developer.anki.com/

SDK documentation: https://developer.anki.com/vector/docs/index.html

Forums: https://forums.anki.com/


## Privacy Policy and Terms and Conditions

Use of Vector and the Vector SDK is subject to Anki's [Privacy Policy](https://www.anki.com/en-us/company/privacy) and [Terms and Conditions](https://www.anki.com/en-us/company/terms-and-conditions).
