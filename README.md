# app_manager
## Runs Python application in a fault-tolerant environment, continually rebooting after unexpected exceptions.


- Uses Python3 standard library packages only
- app_manager.py contains AppManager class


### examples ###

#### running your app in the AppManager is simple
```
import ApplicationClass
from app_manager import AppManager

app = ApplicationClass()
AppManager(app.run)
''' Exceptions will be printed to the console '''
```

#### alternatively, you can pass in your app's logger so that exceptions appear in your log output
```
from application_package import ApplicationClass, logger
from app_manager import AppManager

app = ApplicationClass()
AppManager(app.run, logger = logger)
''' Exceptions will be printed to the console and logged with the supplied logger'''
```