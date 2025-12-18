#General Description
Updating hydra files to adhere with non-allowance of mutable default and module import system in python 3.11 and higher

##Necessity
1) mutable default removal for dataclass in python 3.11
2)  find_module() deprecated in [this PEP](https://peps.python.org/pep-0451/#api-changes) (under Other API Changes) was removed in python 3.12. Therefore making changes per section 'Other API Changes'.

##What to do?
Copy it into editable install directory once hydra is installed. For example in Colab, if the python version is 3.12:
1) Copy hydra/conf/__init__.py into /usr/local/lib/python3.12/dist-packages/hydra/conf/__init__.py
   `cp hydra/conf/__init__.py /usr/local/lib/python3.12/dist-packages/hydra/conf/__init__.py`
3) Copy hydra/core/plugins.py' to /usr/local/lib/python3.12/dist-packages/hydra/core/plugins.py
   `cp hydra/core/plugins.py /usr/local/lib/python3.12/dist-packages/hydra/core/plugins.py`
