# ubu-datascience-webapp

# ubu-datascience-webapp

```sh
python -m pip install pipenv --user
pipenv install django
pipenv shell
django-admin startproject webapp
cd webapp
python manage.py startapp myapp
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```


-------------------------------------------------------------------------------

clone 

https://github.com/wichit2s/ubu-datascience-webapp

download pipenv
python -m pip install pipenv


use path python or Anaconda3
pipenv --python c:\Users\science\Anaconda3\python.exe

pipenv shell


cd wabapp 
python manage.py migrate

pipenv install numpy
python -m pip install numpy

where ipython
ipyhon 

import numpy 
numpy.__version__

import numpy as np
np.__version__

v = np.ndarray([1,0,0,0,1,0,1,0,0])
w = np.ndarray([1,0,1,0,1,0,1,0,1])
v.data
v.shape
w.shape
