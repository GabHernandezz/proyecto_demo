Pasos:

# 1. Crear carpeta de trabajo
mkdir proyecto_demo
cd proyecto_demo

# 2. Inicializar git
git init

# 3. Crear archivo principal
echo "print('Hola Ingeniería de Software II')" > app.py

# 4. Agregar y registrar cambios
git add .
git commit -m "Versión inicial del proyecto"

Verificar estado:

git log --oneline


Parte 2 – Crear rama de desarrollo

git checkout -b dev
echo "print('Módulo de login agregado')" > login.py
git add login.py
git commit -m "Agregado módulo de login"

Simular trabajo colaborativo:

Crear otra rama test

Modificar app.py con un print adicional.

Hacer merge de ambas ramas a main.

git checkout main
git merge dev
git merge test

Si hay conflictos, resolverlos manualmente editando el archivo y usando:

git add .
git commit -m "Conflictos resueltos"


Parte 3: Subir el proyecto a GitHub

Crear un nuevo repositorio vacío en GitHub.

Conectarlo:

git remote add origin https://github.com/usuario/proyecto_demo.git
git branch -M main
git push -u origin main

3. Verificar que el repositorio aparezca en línea.

4. Crear un README.md y hacer un commit desde GitHub para probar sincronización.


4. Despliegue local o simulado

Crear etiqueta:

git tag -a v1.0 -m "Versión estable del proyecto"
git push origin v1.0

2. Probar el proyecto:

python app.py

Esto simula un release (entrega oficial)