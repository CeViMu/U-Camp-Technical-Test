# Prueba tecnica para futuros instructores y facilitadores de U Camp

**Objetivo:**  
Construir un Front-End y un Back-End que interactuen con una API externa, esta API será la de **Mercado Libre** 

## Inicio del proyecto  
1) Para comenzar instalaremos la dependencia jest que nos ayudará a crear pruebas de unidad.  
Documentación: https://jestjs.io/docs/api  

2) Instalamos ESLinter, herramienta de código abierto, que nos ayuda a limpiar nuestro código.  
Documentación: https://eslint.org/docs/rules/  

3) Se agregan pruebas automatizadas de Github Actions
- Creamos un arhivo .github/workflows/test.yml y copiamos el siguiente contenido
´´´
name: Run Tests in my project every push on GitHub

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: Run Jest
      uses: stefanoeb/jest-action@1.0.3
´´´
-Hacemos commit de este archivo y lo agregamos al repositorio.