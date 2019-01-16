=================================
Python and Machine Learning Setup
=================================

Some notes on getting setup for machine learning with Python.


*Python Distribution*

Though I am not sure about Windows, MacOS does ship with a version of
Python baked in. Most people refer to this as system Python. You can
check to see what version of Python your computer has by opening the 
Terminal application and running the following:

*Check to see what Python version you have:*

.. code-block:: console

    python --version

*Check where that version of Python lives:*

.. code-block:: console

    which python

If you have not installed another version of Python, and you are running
MacOS, then you are likely running `Python 2.7`. While there are still
some people using `2.7`, this version of Python is old and is around mainly
for people who haven't migrated all of their work to the newer versions of 
the programming language. 

We are going to want to run `Python 3`, and we are going to want a way to 
get access to all of the open source projects out there. For this, I would 
recommend using Anaconda_, a distribution of Python that comes ready with 
many popular Python libraries ready to use. This distribution is essentially
a new version of Python (currently Python 3.7), many libraries that are regularly
used by Python programers, and a package manager that keeps all our installed 
libraries sorted. You can download the Anaconda distribution by following the link
here_. You can also download it straight from the command line with the following:

.. code-block:: console

    wget -c https://repo.continuum.io/archive/Anaconda3-2018.12-MacOSX-x86_64.sh
    bash Anaconda3-2018.12-MacOSX-x86_64.sh

This will download the most recent version of Anaconda (Python 3.7) and then start
the install process. Follow the prompts for the install process. At some point, 
Anaconda will ask you if you want to install at a certain default location. This 
should be :code:`/Users/<username>/anaconda3`. Anaconda should then ask if you would
like to save the this location to your :code:`~/.bashrc`. This is definitely a good idea,
it will help point you to the right location of your new Python install. Once that is 
all setup, restart your terminal and check on Python again:

*Check to see what Python version you have:*

.. code-block:: console

    python --version

*Check where that version of Python lives:*

.. code-block:: console

    which python

You should now see that you are running Python 3.7 and that it is installed at 
:code:`/Users/<username>/anaconda3` (if you kept all the defaults at install).

You can then run a Python interpreter by running the following:

.. code-block:: console

    ipython

Test to see if you can then import and use one of the libraries installed with 
Anaconda:

.. code-block:: python

    import numpy as np

    random_array = np.random.randn(5)
    print(f'My random array: {random_array}')

If all of that works, you are in business! What the above code is doing is first 
loading a linear algebra library, numpy, and aliasing it as :code:`np`. We are then 
initializing an array of five elements with random values, and finally printing out 
the contents of that array. When you are done using the :code:`ipython` Python 
interpreter, you can close it with :code:`quit()`.

The Anaconda distribution comes with a lot of Python libraries. To check out what these
are, run 

.. code-block:: console

    pip list

This will give you a big list of all the libraries you have installed, along with their 
version numbers. If you ever come across some Python package that is not currently installed, 
you can install it with 

.. code-block:: console

    pip install <package-name>

Just replace :code:`package-name` with the name of the package you would like to install.


.. _Anaconda: https://www.anaconda.com/download/#macos
.. _here: https://www.anaconda.com/download/#macos
