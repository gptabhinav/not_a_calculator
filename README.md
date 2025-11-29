### how to create python bindings for cpp projects

```bash

# setup env and install dependencies
source -m venv .venv
.venv/bin/activate
pip install -r requirements.txt

# create a python module which creates an extension to the code in example.cpp
c++ -O3 -Wall -shared -std=c++11 -fPIC -I/home/ag10706/miniconda3/include/python3.13 -I/home/ag10706/git/experiments_with_python_bindings/.venv/lib/python3.13/site-packages/pybind11/include example.cpp -o example.cpython-313-x86_64-linux-gnu.so

# test it!
python main.py
```
