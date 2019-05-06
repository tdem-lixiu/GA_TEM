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

.. py:function:: def initData()

    Initialization 1D forward parameters.

    :param nlayer: ``3``
    :type nlayer: ``int``
    :param res: ``[100, 10, 100]``
    :type res: ``dtype='f8', order='f'``
    :param thickness: ``[20, 10]``
    :type thickness: ``dtype='f8', order='f'``
    :param I0: ``1.0``
    :type I0: ``float64``

.. py:function:: def initUI()

    Initialization interface.

.. py:function:: def rbclicked()

    Get radio button information.

    :param filename: ``d`` , Field
    :type filename: 1
    :param filename: ``f`` , Time derivative of the field
    :type filename: 2

.. py:function:: def savedata()

    Save forward data.

    :param filename: Input file name
    :type filename: str

.. py:function:: def calculate()

    1D GA-TEM forward.

    :param calc_lib: GATEM_Fwd1D.dll
    :type calc_lib: cdll.library
    :param calc_lib.GroundAirTEM1DFwd.argtypes: [c_int, POINTER(c_double), POINTER(c_double),
     c_double, c_int, POINTER(c_double), POINTER(c_double), c_double, c_double, c_double, c_char, POINTER(c_double)]
    :type calc_lib.GroundAirTEM1DFwd.argtypes: list
    :param calc_lib.GroundAirTEM1DFwd.restyper: POINTER(c_double)
    :type calc_lib.GroundAirTEM1DFwd.restype: list
    :param calc_reply: ``Finish``
    :type calc_reply: QMessageBox

.. py:function:: def critical()

    Reply information by QMessageBox.

    :param msgBox: Error Message, Retry/Abort/Ignore
    :type msgBox: QMessageBox

.. py:function:: def logplot()

    Plot forward data in loglog axis.

    :param dbdt: dbdt[:,0], dbdt[:,1]
    :type dbdt: ``np.narray``

3.class Calc1DFwd_p()
:::::::::::::::::::::::

Module Table
===============

1.class TableWindow()
:::::::::::::::::::::::

.. py:function:: def getfilename()

    Get the filename of the data to display in table.

.. py:function:: def saveas()

    Save as function API.

.. py:function:: def save()

    Save function API.

2.class FilteredTableWidget()
:::::::::::::::::::::::::::::::

.. py:function:: def slotSelect()

    The SLOT for which data is selected.

.. py:function:: def on_view_horizontalHeader_sectionClicked()

    Set the header for data.

.. py:function:: def menuClose()

    The operation after set the fileter.

.. py:function:: def loadAll(filename)

    Load all the data in the table.

.. py:function:: def Saveas()

    Save as function

.. py:function:: def Save()

    Save function

.. py:function:: def clearFilter()

    Clear the filtered.

.. py:function:: def filterdata()

    Filtered part of data is not displayed.

Other Module
===============

1.class login()
:::::::::::::::::

.. py:function:: def loginInit()

    Initialization login information.

.. py:function:: def showDialog()

    Display current login information.

MainWindow
===============

1.class class Ui_MainWindow()
:::::::::::::::::::::::::::::::

2.class MyMainWindow()
:::::::::::::::::::::::::
