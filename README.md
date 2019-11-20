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

---------------------------------
pipenv shell 
where ipython
ipyhon 
---------------------------------
import numpy 
numpy.__version__

import numpy as np
np.__version__

v = np.ndarray([1,0,0,0,1,0,1,0,0])
w = np.ndarray([1,0,1,0,1,0,1,0,1])
v.data
v.shape
w.shape


In [1]: import numpy
In [2]: import numpy as np
In [3]: np.__version__
Out[3]: '1.17.4'
In [4]: p = [1,2,1]
In [5]: v = [[1,2,1],[2,3,3]]
In [6]: print(v)
[[1, 2, 1], [2, 3, 3]]
In [7]: print(p)
[1, 2, 1]
In [8]: m3 = [
   ...:   [
   ...:     [1,2,1],
   ...:     [2,2,2],
   ...:     [3,3,3]
   ...:   ],
   ...:   [
   ...:     [1,2,1],
   ...:     [2,2,2],
   ...:     [3,3,3]
   ...:   ]
   ...: ]
   ...: 
In [9]: print(m3)
[[[1, 2, 1], [2, 2, 2], [3, 3, 3]], [[1, 2, 1], [2, 2, 2], [3, 3, 3]]]
In [10]: m1 = np.array([1,2,1])
In [11]: type(m1)
Out[11]: numpy.ndarray
In [12]: m1.shape
Out[12]: (3,)


In [80]: import matplotlib.pyplot as plt

In [81]: def f(x): return np.e**x- np.sin(x)

In [82]: x= np.linspace(-100,100,10000,dtype=np.float32)

In [83]: y = f(x)
C:\Users\science\.virtualenvs\ubu-datascience-webapp-nwcO-nrO\Scripts\ipython:1: RuntimeWarning: overflow encountered in power

In [84]: plt.plot(x,y)
Out[84]: [<matplotlib.lines.Line2D at 0x720c3c0a20>]
In [198]: x =y[0,0,...]

In [199]: x[:,0]
Out[199]: array([ 2,  0,  3,  8,  6, 10,  5, 10,  3,  4])

In [200]: x[0,:]
Out[200]: array([ 2,  8,  4,  8,  7, 10,  9,  7,  4,  0])

In [201]: y[0,:]
