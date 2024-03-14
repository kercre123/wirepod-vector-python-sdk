.. _install-windows:

######################
Installation - Windows
######################

This guide provides instructions on installing the Vector SDK for computers running with a Windows operating system.

^^^^^^^^^^^^^
Prerequisites
^^^^^^^^^^^^^

* Vector is powered on.
* Vector has been set up with wire-pod.
* Vector is connected to the same network as your computer.
* You can see Vector's eyes on his screen.


^^^^^^^^^^^^^^^^^^^
Python Installation
^^^^^^^^^^^^^^^^^^^

Download the `Python 3.9 (or later) executable file from Python.org <https://www.python.org/downloads/windows/>`_ and
run it on your computer.

.. important:: Be sure to tick the "Add Python 3.X to PATH" checkbox on the Setup screen. Then tap "Install Now" and complete the Python installation.

^^^^^^^^^^^^^^^^
SDK Installation
^^^^^^^^^^^^^^^^

If you have any other Vector SDK installed, uninstall it by running these commands in the Terminal window::

    py -m pip uninstall anki_vector
    py -m pip uninstall ikkez_vector
    py -m pip uninstall cyb3r_vector_sdk

To install the SDK, type the following into the Command Prompt window::

    py -m pip install --user wirepod_vector_sdk

.. note:: If you encounter an error during SDK installation, you may need to upgrade your pip install. Try ``python -m pip install --upgrade pip`` or ``py -3 -m pip install --upgrade pip``

.. note:: If you encounter an error during SDK installation, you may need to upgrade your Python Setuptools. Try ``py -3 -m pip install --upgrade setuptools``

"""""""""""
SDK Upgrade
"""""""""""

To upgrade the SDK from a previous install, enter this command::

    py -m pip install --user --upgrade wirepod_vector_sdk

^^^^^^^^^^^^^^^^^^^^^
Vector Authentication
^^^^^^^^^^^^^^^^^^^^^

.. important:: If you are installing the SDK on the same machine your wire-pod instance is running on, there is no need to do this. The bot will be automatically configured.

If the SDK machine and the wire-pod machine are different, then to authenticate with the robot, type the following into the Command Prompt window::

    py -m anki_vector.configure

You will be prompted for your robot's name, ip address and serial number. You will also be asked for your wire-pod instance's IP address. You can have it try to find your instance automatically, but it doesn't tend to work well on Windows.

You will see "SUCCESS!" when this script successfully completes.

.. note:: By running the ``anki_vector.configure`` executable submodule, you will be asked to provide your wire-pod instance IP address (you can also have the script automatically try to find the wire-pod instance), and the script will automatically download an authentication token and certificate to your computer that will grant you access to the robot and his capabilities (such as camera and audio) as well as data stored on the robot (such as faces and photos).

  The downloaded access token is equivalent to your account credentials. It will be stored in your user directory (~/.anki_vector) along with a robot identity certificate and other useful data for establishing a connection. Do not share your access token.

.. warning:: These credentials give full access to your robot, including camera stream, audio stream and data. Do not share these credentials.

^^^^^^^^^^^^^^^
Troubleshooting
^^^^^^^^^^^^^^^

Please see the :doc:`Troubleshooting </troubleshooting>` page for tips, or visit the `Unofficial DDL Discord <https://discord.gg/Hs4QuhDush>`_ to ask questions, find solutions, or for general discussion.

----

Anki, modified by kercre123
