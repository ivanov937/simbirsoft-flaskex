Делал все согласно  файлу Readme.md.
Запустил PyCharm.
Выполнил клонирование flaskex к себе - git clone https://github.com/anfederico/Flaskex
Переместился в директорию Flaskex - cd Flaskex
Установил внешние модули из файла requirements.txt - pip install -r requirements.txt
Запустил приложение - python app.py
Вышла ошибка:
Traceback (most recent call last):
  File "C:\Users\Ivanov\Desktop\111\flaskex-master\Flaskex\app.py", line 4, in <module>
    from scripts import forms
  File "C:\Users\Ivanov\Desktop\111\flaskex-master\Flaskex\scripts\forms.py", line 6, in <module>
    class LoginForm(Form):
  File "C:\Users\Ivanov\Desktop\111\flaskex-master\Flaskex\scripts\forms.py", line 7, in LoginForm
    username = StringField('Username:', validators=[validators.required(), validators.Length(min=1, max=30)])
AttributeError: module 'wtforms.validators' has no attribute 'required'

AttributeError: module 'wtforms.validators' has no attribute 'required' - модуль wtforms.validators не имеет аттрибута required.
Изменил required на DataRequired (https://stackoverflow.com/questions/70362960/python-flask-flask-admin-wtforms-validators-attributeerror)

После следующего запуска локально все открылось -  * Running on http://127.0.0.1:5000

