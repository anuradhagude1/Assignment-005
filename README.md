# Assignment-005
Software Architect and Design
Install django by using command pip install django in Terminal.
Start a new project by using command django-admin startproject projetname
Create a new app by using command python manage.py startapp appname
Write view of the app
from django.http import JsonResponse
def index(request):
    res = {
        'Message':"Hello, World!"
    }
    return JsonResponse(res)
Map urls of the app
from django.urls import path
from . import views

urlpatterns = [
    path('',views.index, name="index")
]
Map urls of the app in the project
from django.urls import path
from polls import views

urlpatterns = [
    path('',views.index, name="index"),
    path('admin/', admin.site.urls),
    
]

Run the server by using command python manage.py runserver
it will run on localsever http://127.0.0.1:8000
