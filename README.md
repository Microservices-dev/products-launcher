1. Clonar el repositorio
2. Asegurate de tener el archivo .env con as las variables de entorno basado en .env.template
3. Ejecutar el comando:

```
docker compose up --build
```

### Pasos para crear los Git Submodules

1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-módulo (no debe de existir en el proyecto)

```
git submodule add <repository_url> <directory_name>
```

4. Añadir los cambios al repositorio (git add, git commit, git push)
   Ej:

```
git add .
git commit -m "Add submodule"
git push
```

5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos

```
git submodule update --init --recursive
```

6. Para actualizar las referencias de los sub-módulos

```
git submodule update --remote
```

## Production

1. Clonar el repositorio
2. Asegurate de tener el archivo .env con as las variables de entorno basado en .env.template
3. Ejecutar el comando de Docker:

```
docker compose -f docker-compose.prod.yml build
```

o correr para levantar en ese momento los contenedores

```
docker compose -f docker-compose.prod.yml up
```

## Importante

Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal.

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.

### Author

![enter image description here](https://avatars1.githubusercontent.com/u/6466769?s=170&v=4)

- **Carlos Enrique Ramírez Flores** - _Backend Development_ - [GitHub](https://github.com/linuxcarl), [GitLab](https://gitlab.com/linux-carl), [Web Site](https://www.carlosramirezflores.com), [Linkedin](https://www.linkedin.com/in/carlos-enrique-ram%C3%ADrez-flores/)

## License

[MIT](https://choosealicense.com/licenses/mit/)
