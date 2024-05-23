# DJANGO SHELL

## GETTING STARTED

```bash
python manage.py shell
```

## ALL OBJECTS

```python
from notes.models import Note
Note.objects.all()
```

## FILTER OBJECTS

```python
Note.objects.filter(title__contains='django')
```

## CREATE OBJECT

```python
from django.contrib.auth.models import User
me = User.objects.get(username='admin')
Note.objects.create(author=me, title='Django ORM', content='Django ORM is easy to use.')
```

## UPDATE OBJECT

```python
note = Note.objects.get(title='Django ORM')
note.title = 'Django ORM Tutorial'
note.save()
```

## DELETE OBJECT

```python
note = Note.objects.get(title='Django ORM Tutorial')
note.delete()
```

## RELATED OBJECTS

```python
note = Note.objects.get(title='Django ORM')
note.author
```


## ORDERING OBJECTS

```python
Note.objects.order_by('created_date')
# OR REVERSE ORDER
Note.objects.order_by('-created_date')
```


