Previously installed deps:

brew install python3
pip3 install Cython


Possibly needed deps? Not sure (I previously did 'pip3 install attic', 'pip3 uninstall attic' before installing from source):

pip3 install msgpack-python
pip3 install setuptools


Optional deps: to use 'attic mount', need FUSE (fuse4x), plus llfuse python module:

brew install fuse4x

...then follow these instructions from brew Caveats to install the kernel extension:

  - If it's already installed (/Library/Extensions/fuse4x.kext) and you're upgrading:
    - if there's any fuse filesystems mounted ('mount -t fuse4x' will show them), unmount
    - sudo kextunload -b org.fuse4x.kext.fuse4x
    - Presumably? 'sudo rm -r /Library/Extensions/fuse4x.kext'
  - Install new extension:
    sudo /bin/cp -rfX /usr/local/Cellar/fuse4x-kext/0.9.2/Library/Extensions/fuse4x.kext /Library/Extensions
    sudo chmod +s /Library/Extensions/fuse4x.kext/Support/load_fuse4x

pip3 install llfuse


To install attic from this git repository: git clean (build, dist etc), and then:

python3 setup.py install


Haven't figured out how to do it cleanly (with uninstall) yet...