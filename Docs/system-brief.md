# System Brief: MangaColor Hub

## 1. El Problema
Los equipos independientes de traducción y coloreo de manga suelen utilizar herramientas dispersas (Discord, Google Drive, Excel) para gestionar sus proyectos. Esto provoca pérdida de archivos, sobrescritura accidental del trabajo, doble asignación de una misma página y cuellos de botella en la revisión del editor.

## 2. Stakeholders
* **Administradores / Editores:** Supervisan la calidad, asignan trabajo y publican el capítulo final.
* **Coloristas / Redibujantes:** Reciben páginas en blanco y negro, las editan y suben el resultado.
* **Traductores:** Extraen el texto original y proporcionan la traducción estructurada.

## 3. Scope vs No-Scope
* **In-Scope (Dentro del alcance):** Gestión de usuarios (roles), asignación de páginas individuales, subida/descarga de imágenes por versión, panel de traducción por página y flujos de aprobación.
* **No-Scope (Fuera del alcance):** Lector de manga integrado para el público general, herramientas de edición de imagen nativas en el navegador y publicación automática en redes sociales.

## 4. Diagrama de Contexto (Mermaid)

```mermaid
graph TD
    A[Colorista / Traductor] -->|Sube archivos y textos| B(MangaColor Hub Core)
    C[Editor / Admin] -->|Asigna tareas y aprueba| B
    B --> D[(Base de Datos: Capítulos y Roles)]
    B --> E[Almacenamiento Cloud: Imágenes]
