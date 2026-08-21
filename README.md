# Mi primer repositorio

Este es un proyecto de práctica para aprender Git y GitHub.

HOLA QUE PASA SI LO ACTUALIZA

DE NUEVO

practica y mas practica

PASOS PARA ACTUALIZAR EN GIT:

git status

git add .

git commit -m "Describe aqui que cambiaste"

git push

Paso 1: Ubícate en la carpeta del proyecto

cd ruta\a\tu\proyecto-laravel
Paso 2: Inicializar git en esa carpeta

git init
Paso 3: Crear un archivo .gitignore — MUY importante en Laravel
Antes de agregar nada, necesitas decirle a Git qué carpetas/archivos no debe subir (dependencias pesadas, credenciales, cachés). Laravel genera uno por defecto, pero si no lo tienes, debe incluir al menos:


/vendor
/node_modules
.env
/storage/*.key
/public/hot
/public/storage
.phpunit.result.cache
vendor/ y node_modules/ son carpetas gigantes que se regeneran con composer install / npm install, no se suben.
.env contiene contraseñas y claves — nunca debe subirse a GitHub.
Paso 4: Ver qué va a incluirse

git status
Revisa que NO aparezcan vendor/, node_modules/ ni .env en la lista. Si aparecen, significa que el .gitignore no está bien puesto o no se guardó antes del add.

Paso 5: Agregar y hacer el primer commit

git add .
git commit -m "Version inicial del proyecto Laravel"
Paso 6: Crear el repositorio en GitHub
Igual que la vez pasada: entra a github.com/new, ponle nombre, no marques ninguna opción de inicialización (README, .gitignore, licencia) porque ya tienes contenido local.

Paso 7: Conectar y subir

git remote add origin https://github.com/tu-usuario/nombre-repo.git
git branch -M main
git push -u origin main
Paso 8: Verificar en GitHub
Entra al repo y confirma que solo se subió el código fuente — no vendor/ ni .env.

Dato clave para Laravel: si tu proyecto ya tenía tiempo corriendo y nunca se subió a Git, es muy probable que .env o vendor/ ya se hayan colado en commits anteriores si no pusiste el .gitignore a tiempo. ¿Es un proyecto nuevo desde cero o ya tiene código con el que quieres empezar a practicar esto?
