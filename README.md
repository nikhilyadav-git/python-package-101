# python-package-101

#### Why Python  Packaging?
- Package are standard way to to package code for distribution
- Easy to install - pip install *<package_name>*
- Automayed installation of dependencies
- Resure part of codebase anywhere
- Install once and use/call anywhere
- Allows for CI/CD, auomated testing
- Versioning & backwards compatibility

#### Virtual Enviorment
```sh
python -m venv .venv
source .venv/bin/activate
deactivate
```

#### Install Package
- upgrade pip -> __pip3 install pip --upgrade__
- Section 01
    - Create a package
    - create a src folder
    - add a  dunder init inside src
    - add pyproject.toml inside package folder
    - run -> __pip3 install -e .__
    - test package -> switch to python console by typing __python3__ and run 
    ```python
    import ny_pack_1
    ```
    - uninstall package - __pip3 uninstall ny_pack_1__
- Section 02
    - test package -> switch to python console by typing __python3__ and run 
    ```python
    import ny_pack_1
    from ny_pack_1 import print_me
    print_me()
    ```

#### Run Module
```sh
python -m ny_pack_1
```
or 
```sh
python run_print_me.py
```

#### Run Bash Command, Section 2 project.scripts in .toml file
```sh
print_bash_cmd
```

#### Upload To PyPi
- set up token file on your $HOME/.pypirc file
- example format
```sh
[pypi]
  username = __token__
  password = pypi-AgEIcHl.................
```
- upload
```sh
pip3 install build
python3 -m build
pip3 install twine
python3 -m twine upload dist/* --skip-existing
```