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
many popular Python libraries ready to use. 

.. _Anaconda:
