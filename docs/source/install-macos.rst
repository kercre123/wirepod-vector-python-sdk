.. _install-macos:

###########################
Installation - macOS / OS X
###########################

This guide provides instructions on installing the Vector SDK for computers running with a macOS operating system.

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

1. Install `Homebrew <https://brew.sh>`_ on your system according to the latest instructions. If you already had brew installed then update it by opening a Terminal window and typing in the following::

    brew update

2. Once Homebrew is installed and updated, type the following into the Terminal window to install the latest version of Python 3::

    brew install python3

The Vector SDK supports Python 3.9 or later.


^^^^^^^^^^^^^^^^
SDK Installation
^^^^^^^^^^^^^^^^

If you have any other Vector SDK installed, uninstall it by running these commands in the Terminal window::

    python3 -m pip uninstall anki_vector
    python3 -m pip uninstall ikkez_vector
    python3 -m pip uninstall cyb3r_vector_sdk

To install the SDK, type the following into the Terminal window::

    python3 -m pip install --user wirepod_vector_sdk

"""""""""""
SDK Upgrade
"""""""""""

To upgrade the SDK from a previous install, enter this command::

    python3 -m pip install --user --upgrade wirepod_vector_sdk

^^^^^^^^^^^^^^^^^^^^^
Vector Authentication
^^^^^^^^^^^^^^^^^^^^^

To authenticate with the robot, type the following into the Terminal window. Note that during this configure step, your password will not show by design as a security precaution::

    python3 -m anki_vector.configure

You will be prompted for your robot's name, ip address and serial number. You will also be asked to provide the IP address of your wire-pod instance. You can have it try to find the instance automatically if that is more convenient.

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

