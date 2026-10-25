# b0-p01 · Casa · Préstamo de portátiles

- **Alumno:** Lautaro Martin
- **Bloque:** B0 — Prerrequisitos
- **Fase / ejercicio:** Fase 0.8 · Práctica 01 · Casa
- **Fecha de inicio:** 17/10/2026
- **Fecha de entrega:** 18/10/2026

---

## 🎯 Qué se pedía

Crear desde cero una bóveda llamada `Boveda_HTML_Casa` con una web de préstamo de portátiles y su propio repositorio Git conectado a GitHub mediante SSH.

Había que crear tres versiones de la web, comprobar el historial de Git, recuperar temporalmente la primera versión y volver a `main`, además de preparar un vídeo completo explicando el proceso.

## ⌨️ Comandos y pasos importantes

- `git --version` — comprobar que Git está instalado.
- `git config --global user.name` — comprobar el nombre configurado para los commits.
- `git config --global user.email` — comprobar el correo configurado para los commits.
- `ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub` — comprobar que existen las claves SSH.
- `ssh -T git@github.com` — comprobar la autenticación con GitHub.
- `pwd` — comprobar que estoy dentro de `01_Proyecto`.
- `git init` — crear el repositorio Git local.
- `git branch -M main` — establecer `main` como rama principal.
- `git status` — consultar el estado del repositorio.
- `git remote add origin ...` — conectar el repositorio local con GitHub.
- `git remote -v` — comprobar el remoto configurado.
- `git add .` — preparar archivos para un commit.
- `git add web/index.html` — preparar un archivo concreto.
- `git diff -- web/index.html` — comprobar los cambios realizados en la portada.
- `git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4` — comprobar que los vídeos están siendo ignorados.
- `git diff --cached --stat` — revisar los archivos preparados para el commit.
- `git commit -m "..."` — guardar una versión del proyecto en Git.
- `git push` — subir los commits a GitHub.
- `git log --oneline` — consultar el historial de commits.
- `git switch --detach f57b885` — consultar la primera versión de la web.
- `git switch main` — volver a la versión actual de la rama principal.

## 🛠️ Qué he hecho

1. Comprobé que Git estaba instalado y que mi nombre, correo y claves SSH estaban configurados.
2. Comprobé que la autenticación SSH con GitHub funcionaba.
3. Creé la bóveda `Boveda_HTML_Casa` fuera de OneDrive.
4. Creé las carpetas `00_Grabaciones`, `01_Proyecto`, `00_Bitacora` y `web`.
5. Creé la bitácora, `.gitignore` y la primera página `index.html`.
6. Inicialicé Git únicamente dentro de `01_Proyecto` y establecí la rama `main`.
7. Creé el repositorio de GitHub `sor-web-prestamo-portatiles-casa` y lo conecté mediante SSH como `origin`.
8. Guardé y subí la primera versión de la web con el equipo disponible.
9. Modifiqué el estado del equipo a reservado para mantenimiento y guardé una segunda versión.
10. Añadí las páginas `normas.html` y `contacto.html`, además de una imagen del portátil.
11. Creé la carpeta de vídeos y añadí dos vídeos locales. Comprobé mediante `git check-ignore` que Git los ignoraba por la regla `*.mp4`.
12. Preparé individualmente los cuatro archivos de la tercera versión: `index.html`, `normas.html`, `contacto.html` e `imagenes/portatil.png`.
13. Guardé y subí la tercera versión a GitHub.
14. Consulté el historial y localicé el primer commit, `f57b885`.
15. Cambié temporalmente al primer commit para comprobar la versión inicial de la web.
16. Volví a la rama `main` y comprobé que la versión actual y todo el historial seguían disponibles.
17. Comprobé finalmente que el repositorio estaba limpio y sincronizado con GitHub.
18. Grabé el vídeo completo de la práctica y lo preparé para subirlo a YouTube como vídeo no listado.

## 🚩 Qué me ha fallado y cómo lo he resuelto

- Al principio tuve un problema al ejecutar SSH porque escribí el comando incorrectamente y apareció:

  `Could not resolve hostname ssh: Name or service not known`

  Revisé el comando y lo ejecuté correctamente.

- Al crear algunos archivos de la web, Windows los estaba tratando como documentos de texto y aparecían con extensión `.txt`. Los renombré para que fueran realmente `.html` y `.gitignore`.

- Al probar inicialmente los enlaces de `normas.html` y `contacto.html`, aparecía `404 Not Found`. Revisé los nombres y las extensiones de los archivos y corregí el problema.

- Al comprobar los vídeos, inicialmente escribí algunas rutas con nombres incorrectos, como `revision-01.mp4.mp4`. Después utilicé las rutas correctas:

  `web/videos/revision-01.mp4`

  `web/videos/revision-02.mp4`

  y comprobé que ambas estaban siendo ignoradas por `.gitignore`.

- En una comprobación de `git status`, los archivos aparecieron en rojo porque todavía no estaban preparados. Esto era normal porque aún no se había ejecutado `git add`.

- En una ocasión pulsé `Ctrl+C` en la terminal. No afectó al repositorio porque no había ninguna operación importante ejecutándose en ese momento.

## 🤔 Respuestas a las preguntas

1. **¿Por qué `git init` se hizo en `01_Proyecto` y no en la raíz de la bóveda?**  
   Porque la bóveda contiene también elementos de organización de Obsidian y las grabaciones. El repositorio debe controlar solamente el proyecto situado dentro de `01_Proyecto`.

2. **¿Qué mostró `git status` antes de `add`, después de `add` y después de `commit`?**  
   Antes de `add` mostró archivos sin seguimiento o modificados. Después de `add` mostró los archivos preparados para el siguiente commit. Después de `commit` el árbol de trabajo quedó limpio.

3. **¿Por qué creé un repositorio de GitHub propio y lo conecté con `git remote add origin`?**  
   Para que este proyecto de casa fuera independiente del proyecto del centro y poder subir sus commits a su propio repositorio remoto.

4. **¿Por qué las páginas nuevas aparecen en `git status` pero no en `git diff -- web/index.html`?**  
   Porque las páginas nuevas todavía no estaban siendo comparadas como modificaciones de `index.html`. Son archivos nuevos y sin seguimiento, mientras que `git diff -- web/index.html` solo compara los cambios de ese archivo concreto.

5. **¿Cómo comprobé que los vídeos existen pero no se van a subir?**  
   Comprobé que estaban físicamente en la carpeta `web/videos` y utilicé `git check-ignore -v` para verificar que la regla `*.mp4` del `.gitignore` los excluía.

6. **¿Qué muestra `git diff --cached --stat` después de preparar los cuatro archivos?**  
   Muestra un resumen de los cuatro archivos preparados para el commit: `index.html`, `normas.html`, `contacto.html` y `imagenes/portatil.png`.

7. **¿Qué cambia al visitar el primer commit y qué recupero al volver a `main`?**  
   Al visitar el primer commit aparece la versión inicial, con el equipo disponible y sin las modificaciones posteriores. Al volver a `main` se recupera la versión actual con el equipo reservado, la imagen y los enlaces.

8. **¿Por qué esta web necesita historial?**  
   Porque la web puede cambiar con el tiempo y el historial permite saber qué versiones se han creado y recuperar una versión anterior si fuera necesario.

9. **¿Qué aportaría GitHub si otro técnico trabajase conmigo?**  
   Permitiría compartir el repositorio, conservar un remoto con el historial y facilitar el trabajo conjunto sobre el proyecto.

10. **Si mañana corrijo una errata en `normas.html`, ¿qué pasos repito y cuáles no?**  
    Editaría el archivo, comprobaría el cambio con `git status` y `git diff`, lo prepararía con `git add`, haría un nuevo `commit` y ejecutaría `git push`. No repetiría `git init` ni `git remote add origin`.

## 🔗 Enlaces

- **Vídeo de esta fase:**Parte 1-(https://youtu.be/b_BVYXxNUQM?si=BV1BSDixpe8JCASl)
- Parte 2-(https://youtu.be/hFeGAqsMQAk?si=cuwzxN_2LGfvNGXr)
- Parte 3-(https://youtu.be/GzQnlyCy63o?si=k4E0NjKYS6_scp8u)
- **Playlist:**(https://youtube.com/playlist?list=PLCwWRGr6Pk_Q&si=pclHsmeAP1zdpKed)]
- **Repositorio GitHub:** https://github.com/Lauta-Martin-SMR/sor-web-prestamo-portatiles-casa

## 💭 Dudas / a repasar

- Repasar la diferencia entre `git add`, `commit` y `push`.
- Repasar la diferencia entre la rama `main` y un commit en estado `detached HEAD`.
- Repasar cómo funciona `.gitignore` y por qué no elimina los archivos que ignora.