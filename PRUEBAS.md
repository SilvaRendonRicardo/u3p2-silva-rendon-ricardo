# Pruebas de la práctica u3p1

Cómo comprobar el CRUD en producción:

1. Abre https://u3p1-silva-rendon-ricardo.onrender.com/admin/ e inicia sesión.
2. Ve a https://u3p1-silva-rendon-ricardo.onrender.com/servicios/ y usa "+ Nuevo servicio".
3. Edita un servicio con el enlace "Editar": el formulario aparece con sus datos cargados.
4. Elimina un servicio con "Eliminar": primero se muestra la pantalla de confirmación.
5. Captura un precio de 0: el formulario muestra "El precio debe ser mayor a 0."
6. Abre /servicios/999/editar/ con un id que no existe: responde 404.
