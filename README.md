# Django

[helloworld Course](http://tryhelloworld.co.kr/courses/%EC%9E%A5%EA%B3%A0%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%9C-%EC%9B%B9%EC%82%AC%EC%9D%B4%ED%8A%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0)

* **설치** `pip install django`
* **프로젝트 생성** `django-admin startproject <프로젝트이름>`
* **서버 실행** `python manage.py runserver`
* **앱 생성** `python manage.py startapp <앱이름>`
* **라우터** `urls.py` `include(앱이름)`
* **모델 생성** `models.py` `class <모델명>(models.Model)`
* **모델 마이그레이션**
  1. `settings.py` `INSTALLED_APPS에 앱 추가`
  2. **스키마 생성** `python manage.py makemigrations`
  3. **DB 생성** `python manage.py migrate`
* **admin 사용자 생성** `python manage.py createsuperuser`
* **model regist** `admin.py` `admin.site.register(모델명)`
* **모델 모두 불러오기** `<모델명>.objects.all()`
* **python 쉘** `python manage.py shell`
* **템플릿 불러오기**
  1. `context = {'candidates':candidates}`
  2. `render(request, 'elections/index.html', context)`
  3. `{% for candidate in candidates %}` `{% endfor %}`
  4. `{{candidate.name}}`

```
from . import views
from .models import <모델명>
{% csrf_token %}
url(r'^areas/(?P<area>[가-힇]+)/results$', views.results)
HttpResponseRedirect()
```
