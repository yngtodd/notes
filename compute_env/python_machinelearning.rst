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
Here are some notable libraries that should come installed with Anaconda:

* Numpy: linear algebra and arrays (One of my favorite libraries)
* Scikit-Learn: a collection of machine learning algorithms
* Pandas: tabular data storage; used frequently in places like Kaggle competitions
* Scipy: scientific computing and optimization

There are a ton of other libraries out there. If there is something you would like to use 
Python for, chances are someone has some code to help you out with that.

*Machine Learning*

Machine learning (ML) is the bread and butter of what I do. There are tons of resources out there, but there is nothing like trying your hands at using these algorithms. For that, I 
highly recommend checking out Kaggle_, a site that hosts machine learning competitions, often
with some big prizes. I would start by checking out the Titanic_ competition, where you build 
a model to predict survival on the Titanic. You can find a lot of code examples in each 
competition's ```kernels``` section. Checkout the Titanic kernels_. There are tons of helpful
people that walkthrough how they train their ML models for these particular competitions. Often
you can also find details on preparing the data provided in the competitions to be used by the
ML algorithms. 

Another good starting place would be the MNIST_ competition, where you use ML models to learn 
how to recognize hand written digits. This is a great place to start with computer vision 
algorithms.

*Deep Learning*

Inevitably, you will come across neural networks and deep learning. These are the most sought 
after ML algorithms right now, and have been applied to all sorts of domains with incredible success recently. These algorithms are now regularly used in fundamental science, search engines, recommendation systems, and many more applications. You will see a lot of debate about
which deep learning library is the best. Often this comes down to two libraries: Tensorflow_ (designed by Google), and Pytorch_ (designed by Facebook). If you ask me, I would say go with Pytorch. It's design is much more sane, and is much more fun to use. 

*Version Control and UNIX*

Though you can get by without using version control and without diving deep into the UNIX
environment, having some familiarity with these topics is incredibly helpful. Version control
helps us to maintain organization and sanity when writing code. It allows us to test new ideas while maintaining versions of our work. GitHub_ is definitely worth checking out. This is where I keep all of my work, both for work and personal use. UNIX is family of operating systems, of which MacOS is a part. You definitely do not need to do a deep dive into UNIX and the UNIX 
philosophy, but it is useful to learn the fundamentals of the command line if you are not 
familiar with it. You may already know all of this, forgive me if you do. If you aren't super 
familiar with the command line, here is a pretty good tutorial_.

*Notes*

There is a ton of information out there, and it can be pretty crazy to wade through. Hopefully this doesn't seem like some crazy dense forest that you can get lost in. Or maybe it does, just hopefully in a good way. Let me know if you have any questions. There are tons of other resources out there that I can point you to if you want to dig into some of these topics!

.. _Anaconda: https://www.anaconda.com/download/#macos
.. _here: https://www.anaconda.com/download/#macos
.. _Kaggle: https://www.kaggle.com
.. _Titanic: https://www.kaggle.com/c/titanic
.. _kernels: https://www.kaggle.com/c/titanic/kernels
.. _MNIST: https://www.kaggle.com/c/digit-recognizer
.. _Tensorflow: https://www.tensorflow.org/
.. _Pytorch: https://pytorch.org/
.. _GitHub: https://github.com
.. _tutorial: https://www.davidbaumgold.com/tutorials/command-line/
