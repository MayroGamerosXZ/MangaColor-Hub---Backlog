# Requerimientos y Backlog

**🔗 Enlace al Tablero Trello:** [Inserta tu link de Trello aquí]

## Priorización del MVP (Rationale)
El Producto Mínimo Viable (MVP) se ha definido centrándose exclusivamente en resolver el cuello de botella crítico: la colisión de trabajo y la pérdida de archivos. Por ello, las historias "Must" garantizan que el flujo central funcione: un administrador asigna una página, el colorista la trabaja y la sube, y el traductor anota el texto. Sin estas tres piezas funcionando en conjunto, el sistema no ofrece valor sobre una simple carpeta compartida. Las aprobaciones, progresos e historiales (Should/Could) mejoran la experiencia, pero no bloquean la producción básica del capítulo.

## Historias de Usuario (MoSCoW)
1. **(Must)** Asignación de páginas a coloristas.
2. **(Must)** Subida de páginas terminadas.
3. **(Must)** Ingreso de texto traducido por panel.
4. **(Should)** Aprobación/Rechazo de páginas con comentarios.
5. **(Should)** Visualización del porcentaje de avance.
6. **(Could)** Historial de versiones de imágenes.
7. **(Could)** Alertas de capítulo completado.
8. **(Won't)** Integración automática con redes sociales.

## Criterios de Aceptación BDD (Given/When/Then)

**Historia 1 (Must): Asignar página a colorista**
* **Given** que el administrador está en la vista del capítulo y la página 5 está en estado "Pendiente",
* **When** el administrador selecciona al colorista "Mayro" en el menú desplegable y hace clic en "Asignar",
* **Then** la página 5 cambia a estado "Asignada", el nombre del colorista se muestra en la tarjeta y el sistema bloquea la asignación a otros usuarios.

**Historia 2 (Must): Subir página terminada**
* **Given** que el colorista tiene asignada la página 5 y se encuentra en su panel de trabajo,
* **When** el colorista adjunta un archivo .PNG y presiona el botón "Enviar para revisión",
* **Then** el estado de la página cambia a "En Revisión", el archivo queda almacenado de forma segura y el editor es notificado.
