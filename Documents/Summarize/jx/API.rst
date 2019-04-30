API for Ground-Airborne Transient Electromagnetic Method System
*****************************************************************

Module Calculation
====================

1.class Convert_msh()
:::::::::::::::::::::::

Convert GiD mesh file.

.. py:function:: def initUI()

    Initialization interface.

    :param initmodel_bt: connect ``def initmodel``
    :type initmodel_bt: QPushButton
    :param mshfile_bt: connect ``def mshfile``
    :type mshfile_bt: QPushButton
    :param mshconvert_bt: connect ``def startconvert``
    :type mshconvert_bt: QPushButton
    :param vbox1: Vertically arranged icons
    :type vbox1: QVBoxLayout
    :param bg1: Radio button rule
    :type bg1: QButtonGroup

.. py:function:: def initmodel()

    Initialization model parameters.

.. py:function:: def mshfile()

    Get the filename from folder tree.

    :return: Absolute path of mesh file
    :rtype: str

.. py:function:: def startconvert()

    Convert GiD mesh file to forward model.

    :param time_para: connect ``def initmodel``
    :type time_para: np.array, ``dtype='i4'`` , ``order='f'``
    :param calc_flag: Convert type
    :type calc_flag: int
    :param calc_lib: GiD2TEM_zn.dll
    :type calc_lib: cdll.library
    :param convert_reply: Completion feedback information
    :type convert_reply: QMessageBox

.. py:function:: def rbclicked()

    Get radio button information

    :return: calc_flag
    :rtype: int

2.class Calc1DFwd()
:::::::::::::::::::::::

3.class Calc1DFwd_p()
:::::::::::::::::::::::

Module Table
===============

1.class TableWindow()
:::::::::::::::::::::::

2.class FilteredTableWidget()
:::::::::::::::::::::::::::::::

Other Module
===============

1.class login()
:::::::::::::::::

MainWindow
===============

1.class class Ui_MainWindow()
:::::::::::::::::::::::::::::::

2.class MyMainWindow()
:::::::::::::::::::::::::
