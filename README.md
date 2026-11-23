# u3p1-silva-rendon-ricardo

Recuperación de la Unidad 3 · Práctica 1 (Semana 5): **CRUD completo de Servicio con ModelForms**.

Autor: Ricardo Silva Rendón

## Enlaces

- Producción (Render): https://u3p1-silva-rendon-ricardo.onrender.com/servicios/
- Repositorio: https://github.com/SilvaRendonRicardo/u3p1-silva-rendon-ricardo

## Qué incluye

- `ServicioForm` (ModelForm) en `core/forms.py`; el `propietario` lo asigna la vista con `request.user`.
- Validación personalizada `clean_precio`: el precio debe ser mayor a 0.
- Plantilla base `base.html` con Tailwind y formulario reutilizable `servicio_form.html` con `{% csrf_token %}`.
- Vistas Crear, Listar, Editar (con `instance=`) y Eliminar con pantalla de confirmación (solo borra por POST).
- Rutas: `/servicios/`, `/servicios/nuevo/`, `/servicios/<id>/editar/`, `/servicios/<id>/eliminar/`.
- Las vistas usan `@login_required`; por ahora el login es el de `/admin/login/` (`LOGIN_URL`).

## Deploy en Render

- Build Command: `pip install -r requirements.txt && python manage.py collectstatic --noinput && python manage.py migrate`
- Start Command: `gunicorn miproyecto_RSR.wsgi`
- Variables de entorno (9): `DB_NAME`, `DB_USER`, `DB_PASSWORD`, `DB_HOST`, `DB_PORT`, `SECRET_KEY`, `DEBUG`, `ALLOWED_HOSTS`, `CSRF_TRUSTED_ORIGINS`.
- Base de datos MySQL en Aiven; el archivo `.env` no se sube a GitHub.
