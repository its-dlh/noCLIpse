noCLIpse
========

So, you're creating an Android project, but you just hate Eclipse. "It's so finicky and buggy and bloated and awful," you complain. "Well then," I reply, "just use the command line tools." "But typing is haaard," you whine.

Well a solution is now in the making. An intrepid team of barely-employed twenty somethings has come together to create an Android project manager that requires neither Eclipse nor a CLI.

Depends on
----------

* Python 2.4+
* wxPython
* py-androidbuild (see instructions below)

Installing py-androidbuild
--------------------------

noCLIpse depends on a custom version of py-androidbuild forked from [miracle2k's original project](https://github.com/miracle2k/py-androidbuild). If you already have miracle2k's version installed, you may need to remove it in order for our custom module to work.

There are basically two ways of obtaining the custom py-androidbuild module. One is to use the repository reference which exists in the `externals` folder of this project, and the other is to install from [DawsonG's py-androidbuild repository](https://github.com/DawsonG/py-androidbuild) directly using pip. The latter approach is probably the most straightforward if you're running Windows.

###Installing from the externals folder

The py-androidbuild repository is included as a _submodule_ of noCLIpse's git repository. This means that you can pull in all the files from that submodule through the noCLIpse repository, but `git clone` will not do that automatically.

If you are running Linux, the `install_py-androidbuild_linux` shell script should take care of everything for you, including the actual installation of the python module.

If you can't use the shell script (or don't want to), you can run [git's submodule commands](http://www.kernel.org/pub/software/scm/git/docs/git-submodule.html) yourself.
```
git submodule init
git submodule update
```
You would then run `python setup.py install` from the `externals/py-androidbuild` directory according to the [instructions in the Python documentation](http://docs.python.org/install/index.html#the-new-standard-distutils).

###Installing using pip

The [pip installer](www.pip-installer.org) can be used to install the custom py-androidbuild module straight from its repository. All you have to do is run
```
pip install git+git://github.com/DawsonG/py-androidbuild.git
```
and the module is installed for you. More details can be found in [pip's official documentation](http://www.pip-installer.org/en/latest/usage.html#version-control-systems).

Actively developed and tested on
--------------------------------

* Ubuntu 12.04
* Windows 7

Team
-----

* [DLaicH](https://github.com/DLaicH) - project director, lead developer
* [DawsonG](https://github.com/DawsonG) - py-androidbuild backend, Windows-specific fixes, misc development