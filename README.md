# message_boord

Este proyecto es una aplicación web construida con Django para gestionar tareas.

## Estructura del proyecto

- `django_base/`: Configuración principal de Django (settings, urls, wsgi, asgi).
- `tasks/`: Aplicación principal para la gestión de tareas.
  - `models.py`: Define el modelo `Task`.
  - `views.py`: Incluye la vista basada en clase `TaskListView` para mostrar la lista de tareas.
  - `urls.py`: Rutas de la aplicación.
  - `admin.py`: Registro de modelos en el admin.
  - `migrations/`: Migraciones de la base de datos.
- `templates/`: Contiene la plantilla `task_list.html` para mostrar las tareas.
- `db.sqlite3`: Base de datos SQLite.
- `manage.py`: Script de gestión de Django.
- `requeerimients.txt`: Lista de dependencias del proyecto.

## Vista principal

La vista principal es `TaskListView`, que muestra una lista de tareas usando la plantilla `task_list.html`.

```python
# tasks/views.py
class TaskListView(ListView):
    model = Task
    template_name = 'task_list.html'
```

## Instalación

1. Clona el repositorio.
2. Instala las dependencias:
   ```
   pip install -r requeerimients.txt
   ```
3. Realiza las migraciones:
   ```
   python manage.py migrate
   ```
4. Ejecuta el servidor de desarrollo:
   ```
   python manage.py runserver
   ```

## Uso

Accede a la aplicación en `http://localhost:8000/` para ver la lista de tareas.

## Licencia

Este proyecto está bajo la licencia MIT.
