LabelImg
========

.. image:: https://img.shields.io/pypi/v/labelimg.svg
        :target: https://pypi.python.org/pypi/labelimg

.. image:: https://img.shields.io/travis/tzutalin/labelImg.svg
        :target: https://travis-ci.org/tzutalin/labelImg

.. image:: /resources/icons/app.png
    :width: 200px
    :align: center

LabelImg is a graphical image annotation tool.

It is written in Python and uses Qt for its graphical interface.

Annotations are saved as XML files in PASCAL VOC format, the format used
by `ImageNet <http://www.image-net.org/>`__.  Besides, it also supports YOLO format

.. image:: https://raw.githubusercontent.com/tzutalin/labelImg/master/demo/labelImage.jpg
     :alt: Demo Image

`Watch a demo video <https://youtu.be/p0nR2YsCY_U>`__

Installation
------------------


Build from source
~~~~~~~~~~~~~~~~~

Linux/Ubuntu/Mac requires at least `Python
2.6 <https://www.python.org/getit/>`__ and has been tested with `PyQt
4.8 <https://www.riverbankcomputing.com/software/pyqt/intro>`__. However, `Python
3 or above <https://www.python.org/getit/>`__ and  `PyQt5 <https://pypi.org/project/PyQt5/>`__ are strongly recommended.


Ubuntu Linux
^^^^^^^^^^^^

Python 3 + Qt5

.. code:: shell

    sudo apt-get install pyqt5-dev-tools
    sudo pip3 install -r requirements/requirements-linux-python3.txt
    make qt5py3
    python3 labelImg.py
    python3 labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]

macOS
^^^^^

Python 3 + Qt5

.. code:: shell

    brew install qt  # Install qt-5.x.x by Homebrew
    brew install libxml2

    or using pip

    pip3 install pyqt5 lxml # Install qt and lxml by pip

    make qt5py3
    python3 labelImg.py
    python3 labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]


Python 3 Virtualenv (Recommended)

Virtualenv can avoid a lot of the QT / Python version issues

.. code:: shell

    brew install python3
    pip3 install pipenv
    pipenv run pip install pyqt5==5.12.1 lxml
    pipenv run make qt5py3
    python3 labelImg.py
    [Optional] rm -rf build dist; python setup.py py2app -A;mv "dist/labelImg.app" /Applications
