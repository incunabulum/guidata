Based on the Qt Python binding module [PyQt4](http://www.riverbankcomputing.co.uk/software/pyqt/intro), **guidata** is a Python library generating graphical user interfaces for easy dataset editing and display. It also provides helpers and application development tools for PyQt4.

The **guidata** library is available for Windows XP/Vista/7, GNU/Linux (official packages are available for [Debian](http://packages.debian.org/fr/sid/python-guidata), [Ubuntu](http://packages.ubuntu.com/search?suite=default&section=all&arch=any&lang=fr&searchon=names&keywords=guidata) and [archlinux](https://aur.archlinux.org/packages.php?ID=47948)) and MacOS X, under the terms of the [CECILL license](http://www.cecill.info/licences/Licence_CeCILL_V2-en.html).

**Documentation** is available [on this page](http://packages.python.org/guidata/) or as a [compiled HTML file](http://guidata.googlecode.com/files/guidatadoc.chm).

You may submit **bug reports** and **feature requests** thanks to the [Issues](http://code.google.com/p/guidata/issues/list) tracker.

### Simple example ###
The main feature of **guidata** is to generate graphical user interfaces for dataset editing. Here is an example with a dialog box creation (see the [documentation](http://packages.python.org/guidata/) for more examples):
```
import guidata
_app = guidata.qapplication() # not required if a QApplication has already been created

import guidata.dataset.datatypes as dt
import guidata.dataset.dataitems as di

class Processing(dt.DataSet):
    """Example"""
    a = di.FloatItem("Parameter #1", default=2.3)
    b = di.IntItem("Parameter #2", min=0, max=10, default=5)
    type = di.ChoiceItem("Processing algorithm",
                         ("type 1", "type 2", "type 3"))

param = Processing()
param.edit()
```
Here is the generated GUI dialog box:

![http://guidata.googlecode.com/files/basic_example_win8.png](http://guidata.googlecode.com/files/basic_example_win8.png)


---

<p align='center'>©2010-2011 CEA - Commissariat à l'Energie Atomique et aux Energies Alternatives</p>