---
cloud: experience-cloud
solution-title: Información y asistencia
solution-hub-url: https://helpx.adobe.com/support/experience-manager/6-4.html
solution-icon: assets/experience-cloud-logo-24.png
getting-started-title: Introducción
getting-started-url: https://docs.adobe.com/content/help/en/livefyre/implementation/c-getting-started/implementation-process/c-implementation-process.html
tutorials-title: Tutoriales
tutorials-url: https://helpx.adobe.com/experience-manager/kt/index/aem-6-4-videos.html
mini-toc-levels: '2'
git-repo: https://github.com/AdobeDocs/livefyre.en
translation-type: tm+mt
source-git-commit: 170fa6b446345d5e2e272294a3267d1ebbb0cd09

---


# Metadatos para uso interno

The metadata.md file includes repo-level metadata that passes through to user guide TOC.md files in the repo. If you want to change metadata.md content for any user guide, do so in any TOC.md file.

| metadatos | lo que hace |
|--- |--- |
| solution-title | Used in article header as link |
| solution-hub-url | Abre la página del concentrador de ayuda |
| solution-icon | Muestra el icono de solución junto al título de la solución. Not yet implemented |
| getting-started-url | Vínculo a la página de introducción de ayuda |
| tutorials-url | Link to video tutorials--either helpx tutorials or KT tutorials |
| mini-toc-levels | Determines the number of heading levels that appear in right rail. el valor predeterminado es 2 |
| git-repo | Specifies the location of the master repo for internal use |

In TOC.md file

| metadata | lo que hace |
|--- |--- |
| user-guide-title | Se utiliza en el encabezado del artículo como vínculo |
| user-guide-url | Abre la página del concentrador de ayuda |
