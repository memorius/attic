Previously:

brew install python3
pip3 install Cython

Maybe needed? Not sure (I previously did 'pip3 install attic', 'pip3 uninstall attic' before installing from source):

pip3 install msgpack-python
pip3 install setuptools


To install: git clean (build, dist etc), and then:

python3 setup.py install


Haven't figured out how to do it cleanly (with uninstall) yet...