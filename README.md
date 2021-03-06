## Project description
sc_mainwindow is a pyqt5 custom widget that can be used as the main window. This widget provides a custom frame with a title bar. You can move the window using the title bar and can resize the window by using the frame. It does not depend upon os. Also, you can customize anything.

## Author
SihinaCode Youtube channel.
[click here to visit](https://www.youtube.com/channel/UCOBz3xsHeNWmeq8yTDnc6Og)

## Installation
Use the package manager [pip](https://pip.pypa.io/en/stable/) to install sc_mainwindow.

```bash
pip install sc-mainwindow
```

## Usage
### main window
```python
from PyQt5 import QtWidgets
from sc_mainwindow import MainWindow
import sys

class Main(MainWindow):
    def __init__(self):
        super(Main, self).__init__()
       
if __name__ == "__main__":
        app = QtWidgets.QApplication(sys.argv)
        Form = Main()
        Form.show()
        sys.exit(app.exec_())
```
```python
from PyQt5 import QtWidgets
from sc_mainwindow import MainWindow
#from body import Body               #import your pyqt5 Body class here
import sys

class Main(MainWindow):
    def __init__(self):
        super(Main, self).__init__()
        #window size
        #self.resize(800, 600)   

        #enable/disable the ability to resize the window - default: 1
        #self.resizable = 0     

        #title text - default:untitled          
        #self.setTitleText("title text")  

        #title bar icon
        #self.setIcon("path of image")    

        #transparency of window (0 - 1) - default: 1
        #self.setTransparent(0.9)         

        #enable/disable frame shadow - default: 1
        #self.setFrameShadow(0)           

        #body = Body()
        #self.insertBody(body)

        #self.setTitleBarColor(0, 0, 0)
        #self.setShadowColor(0, 0, 0)
        #self.setBorderColor(0, 0, 0)

        #self.titleBar.hide()
        #self.minimizeButton.hide()
        #self.maximizeButton.hide()
        #self.closeButton.hide()



if __name__ == "__main__":
        app = QtWidgets.QApplication(sys.argv)
        Form = Main()
        Form.show()
        sys.exit(app.exec_())
```
### body
```python
from PyQt5 import QtWidgets, QtCore, QtGui
from bodyUi import Ui_Form                 #your UI class

class Body(QtWidgets.QWidget, Ui_Form):
    def __init__(self):
        super(Body, self).__init__()
        self.setupUi(self)
```

## Support
Visit the SihinaCode YouTube channel for support.
[click here](https://www.youtube.com/channel/UCOBz3xsHeNWmeq8yTDnc6Og)

## License
MIT
