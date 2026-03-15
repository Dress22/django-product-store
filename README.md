# django-product-store

Aplicación web simple desarrollada con Django que permite listar productos y simular una compra mediante confirmación.  
Proyecto realizado como práctica académica para aplicar conceptos de desarrollo web con Python y Django.

# Tecnologías utilizadas

- Python
- Django
- SQLite
- HTML
- CSS

# Funcionalidades

- Visualización de productos disponibles
- Confirmación de compra de un producto
- Eliminación del producto tras confirmar la compra
- Administración de productos desde Django Admin
- Persistencia de datos mediante base de datos SQLite

# Modelo de datos

El sistema utiliza un modelo principal:

Product

Campos del modelo:

- name → nombre del producto
- description → descripción opcional
- price → precio del producto
- image → imagen opcional del producto

# Flujo de la aplicación

1. El usuario accede a la página principal (`/`) y se muestran los productos disponibles.
2. Al presionar **Comprar**, se accede a una página de confirmación.
3. Si el usuario confirma la compra:
   - el producto se elimina de la base de datos
   - el sistema redirige nuevamente al listado de productos.

## Estructura del proyecto

django-product-store/

product_store/ → configuración principal del proyecto Django  
store/ → aplicación encargada de manejar productos  
templates/ → plantillas HTML  
static/ → archivos estáticos (CSS, imágenes)

Archivos principales:

manage.py → utilidad para ejecutar comandos Django  
models.py → definición del modelo Product  
views.py → lógica de las vistas  
urls.py → ruteo de la aplicación

# Instalación y ejecución

1. Clonar el repositorio:

   ```git clone https://github.com/tu-usuario/django-product-store.git```

2. Navegar al directorio del proyecto:

   ```cd django-product-store```

3. Crear y activar un entorno virtual:

   ```python -m venv venv source venv/bin/activate```  
   # En Windows: ```venv\Scripts\activate```

4. Instalar dependencias:

   ```pip install -r requirements.txt```

5. Realizar migraciones:

   ```python manage.py migrate ```

6. Crear un superusuario:

```python manage.py createsuperuser```

7. Iniciar el servidor de desarrollo:
   
   ```python manage.py runserver```
  
8. Acceder a la aplicación en tu navegador:

   ```http://127.0.0.1:8000/```

# Propósito del proyecto

Este proyecto fue desarrollado con fines educativos para practicar:

- arquitectura básica de Django
- modelos y persistencia de datos
- rutas y vistas
- uso de templates
- flujo básico de una aplicación web