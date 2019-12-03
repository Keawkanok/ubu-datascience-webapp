# ubu-datascience-webapp

ไฟล์ view.py
from django.shortcuts import render
import numpy as np


def convert_to_ndarray(x):
    #y = np.random.random((6,5))
    x = x.replace('[','')
    x = x.replace(']','')
    y = []

    for line in x.split('\n'):
        y.append( list(map(float, line.split())))
    return np.array(y)

# Create your views here.
def matmul(req):
    a = convert_to_ndarray('1 2 3 4 5\n6 7 8 9')        
    b = convert_to_ndarray('1 2 3 4 5\n6 7 8 9')
    c = convert_to_ndarray('1 2 3 4 5\n6 7 8 9')
    if req.method == 'POST':        
        a = convert_to_ndarray(req.POST['A'])
        b = convert_to_ndarray(req.POST['B'])
        c = convert_to_ndarray(req.POST['C'])

    else:
        pass   
    print(a)
    print(type(a))
    return render(req, 'myapp/matmul.html' ,{
        'A': a,
        'B': b,
        'C': c
        

    })
    ไฟล์ templates my matmul.html
    <!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <title>Welcom to Matmul</title>
</head>
<body>
    <h1 style="text-align: center;">Welcom to Matmul</h1>
    <form action="" method="POST">
            {% csrf_token%}
           
        <div style="text-align: center;">    
            <span>Matrix A:</span>
            <textarea name="A" id="" cols="60" rows="6">{{A}} </textarea>
            <span>Matrix B:</span>
            <textarea name="B" id="" cols="60" rows="6">{{B}} </textarea>
        </div> <br><br>
        <div>
            <button type="SUMBMIT">Maltiply</button>
        </div>
        </form>
        <div style="text-align: center;">
            <textarea name="C" id="" cols="60" rows="6">{{C}}</textarea>
        </div>
        <div style="text-align: center;">
            <table border="1">
                {% for r in C %}
                <tr>
                    {% for c in r %}
                    <td>{{c}}</td>
                    {% endfor %}
                </tr>
                {% endfor %}
            </table>
        </div>
</body>
</html>

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
