- **Alumno:** Cristian Raul Horopan
- **Bloque:** B0.P01  Cole  Prestamo de portatiles con Git y Github
- **Fase / ejercicio:** Fase 0.8
- **Fecha de inicio: 22/10/2026
- **Fecha de entrega:** 22/10/2026
---
## Qué se pedía
Se pedía crear desde cero una bóveda en Obsidian y una página web para gestionar el préstamo de portátiles, utilizando Git y GitHub para guardar los cambios. Había que crear tres versiones de la web, comprobar que funcionaban, recuperar la primera versión y volver a la actual
## ⌨Comandos y pasos importantes
- `git --version` — comprueba la versión de Git instalada.
    
- `git config --global user.name` — muestra el nombre configurado para los commits.
    
- `git config --global user.email` — muestra el correo configurado para los commits.
    
- `ssh -T git@github.com` — comprueba la conexión SSH con GitHub.
    
- `pwd` — muestra la carpeta en la que estoy trabajando.
    
- `git init` — crea un repositorio Git local.
    
- `git branch -M main` — establece el nombre de la rama principal como `main`.
    
- `git status` — muestra los archivos nuevos, modificados o preparados.
    
  git remote add origin URL` — conecta el repositorio local con el repositorio de GitHub.
    
- `git remote -v` — muestra las direcciones del repositorio remoto.
    
- `git add .` — prepara todos los archivos que no están ignorados.
    
- `git add ruta` — prepara un archivo concreto para guardarlo en la siguiente versión.
    
- `git diff -- web/index.html` — muestra los cambios realizados en la portada que todavía no se han preparado.
    
- `git diff --cached --stat` — muestra un resumen de los cambios preparados.
    
- `git commit -m "mensaje"` — guarda una versión del proyecto en el historial local.
    
- `git push` — sube los commits al repositorio remoto de GitHub.
    
- `git log --oneline` — muestra el historial de versiones de forma resumida.
    
- `git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4` — comprueba qué regla ignora los vídeos.
    
- `git switch --detach CODIGO_PRIMER_COMMIT` — permite consultar la primera versión guardada.
    
- `git switch main` — vuelve a la rama principal y a la versión actual del proyecto.
## Qué he hecho.

1. He creado una bóveda nueva llamada `Boveda_HTML_Centro` en Obsidian.
    
2. He creado las carpetas `00_Grabaciones`, `01_Proyecto`, `00_Bitacora` y `web`, siguiendo la estructura indicada.
    
3. He preparado el archivo `.gitignore` para excluir los vídeos y otros archivos innecesarios.
    
4. He creado `index.html` con el título «Préstamo de portátiles» y el estado inicial «Equipo 01: disponible».
    
5. He inicializado Git dentro de `01_Proyecto`, he creado la rama `main` y he conectado el proyecto con el repositorio de GitHub mediante SSH.
    
6. He guardado y subido la primera versión de la página web.
    
7. He cambiado el estado del equipo a «reservado para mantenimiento» y he guardado y subido la segunda versión.
    
8. He creado las páginas `normas.html` y `contacto.html`, he añadido una imagen del portátil y he incorporado los enlaces correspondientes en la portada.
    
9. He comprobado los cambios con `git status`, `git diff` y `git diff --cached --stat`. También he revisado que los vídeos estuvieran ignorados por Git.
    
10. He preparado los cuatro archivos de la ampliación y he guardado y subido la tercera versión de la web.
    
11. He consultado el historial con `git log --oneline`, he abierto el primer commit para comprobar la versión inicial y después he vuelto a `main`.
    
12. Finalmente, he comprobado el estado del repositorio y he completado la bitácora con la información de la práctica y el enlace del vídeo.
## Qué me ha fallado y cómo lo he resuelto**. 

En unos minutos del video me lio al buscar el archivo index.html  y me fui a un directorio que no era, volvi con un comando llamado  cd ..  y llege a la carpeta donde estaba index.html
## Respuestas a las preguntas
1. ¿Por qué** `**git init**` **se hizo en** `**01_Proyecto**` **y no en la raíz de la bóveda?**

Porque así Git controla solamente los archivos del proyecto y no toda la bóveda de Obsidian. De esta forma, la configuración de Obsidian y las grabaciones quedan fuera del repositorio.

**2. ¿Qué mostró** `**git status**` **antes de** `**add**`**, después de** `**add**` **y después de** `**commit**`**?**

Antes de `add`, mostró los archivos nuevos o modificados que todavía no estaban preparados. Después de `add`, mostró los archivos seleccionados para el siguiente commit. Después de `commit`, mostró que los cambios estaban guardados y que no quedaban cambios pendientes.

**3. ¿Por qué creaste un repositorio de GitHub propio y lo conectaste con** `**git remote add origin**`**?**

Porque necesitaba tener una copia remota del proyecto para subir las versiones y poder consultarlas desde GitHub. El comando `git remote add origin` guarda la dirección del repositorio remoto para poder enviar los commits con `git push`.

**4. ¿Por qué las páginas nuevas aparecen en** `**git status**` **pero no en** `**git diff -- web/index.html**`**?**

Porque `git status` muestra los archivos nuevos que Git todavía no sigue, mientras que `git diff -- web/index.html` compara los cambios de la portada con su versión preparada. Ese comando no muestra el contenido de otros archivos nuevos.

**5. ¿Cómo has comprobado que los vídeos existen pero no se van a subir?**

He comprobado que los dos archivos MP4 existen en la carpeta `web/videos` y he utilizado `git check-ignore -v` para verificar que la regla `*.mp4` de `.gitignore` los excluye. Después he comprobado que no aparecen entre los archivos preparados ni en GitHub.

**6. ¿Qué muestra** `**git diff --cached --stat**` **después de preparar los cuatro archivos?**

Muestra un resumen de los cambios preparados para el siguiente commit, incluyendo los nombres de los archivos y las estadísticas de las modificaciones. En esta práctica deben aparecer la portada, las normas, el contacto y la imagen.

**7. ¿Qué cambia al visitar el primer commit y qué recuperas al volver a** `**main**`**?**

Al visitar el primer commit, la portada vuelve a mostrar «Equipo 01: disponible» y todavía no aparecen la imagen ni los enlaces nuevos. Al volver a `main`, recupero la versión actual, con el estado de mantenimiento, la imagen, los enlaces y las páginas añadidas. El historial no se borra.

**8. ¿Por qué esta web necesita historial? ¿Qué aportaría GitHub si otro técnico trabajase contigo?**

Necesita un historial para saber qué cambios se han realizado, cuándo se guardaron y poder recuperar una versión anterior si algo falla. GitHub permitiría compartir el proyecto, consultar las versiones y facilitar el trabajo conjunto con otros técnicos.

**9. Si mañana corriges una errata en** `**normas.html**`**, ¿qué pasos repites y cuáles no?**

Primero editaría y guardaría el archivo, comprobaría el resultado en el navegador y revisaría el cambio con `git status` y `git diff`. Después prepararía el archivo con `git add web/normas.html`, guardaría el cambio con `git commit -m "Corregir errata en normas"` y lo subiría con `git push`. No repetiría `git init` ni `git remote add origin`, porque el repositorio y la conexión ya existen.
## Enlaces
- **Vídeo de esta fase: 
- **Playlist:** B0_Prerrequisitos
## Dudas / a repasar
- Repasar la diferencia entre `git add`, `git commit` y `git push`.
    
- Entender mejor la diferencia entre el repositorio local de Git y el remoto de GitHub.
    
- Practicar la lectura de `git status` y las marcas de los archivos preparados y modificados.
    
- Repasar cómo funciona `.gitignore` y por qué no elimina archivos que ya están versionados.