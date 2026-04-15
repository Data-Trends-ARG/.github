# 🏛️ Manifiesto de Estándares: [Data Trends]

Este repositorio contiene la **ÚNICA VERDAD** sobre cómo se gestiona el código, los datos y la documentación en nuestra consultora. El incumplimiento de estas normas será tratado como negligencia técnica.

---

## 1. Nomenclatura de Repositorios (kebab-case)
No aceptamos espacios, guiones bajos ni mayúsculas. Los repositorios deben seguir este patrón:
`[prefijo]-[cliente]-[proyecto]-[componente]`

| Prefijo | Uso | Ejemplo |
| :--- | :--- | :--- |
| `bi-` | Proyectos de Power BI, Tableau, ETLs. | `bi-acme-ventas-report` |
| `app-` | Desarrollo de software y aplicaciones. | `app-stark-portal-api` |
| `cons-` | Consultoría pura, auditorías y scripts. | `cons-wayne-data-audit` |
| `infra-` | Automatización y DevOps. | `infra-global-docker-tools` |

---

## 2. La Sentencia de Etiquetado Funcional (Topics)
Un repositorio sin etiquetas es un repositorio invisible. Todo proyecto debe tener Topics que respondan a estas cuatro preguntas:

1. **¿Para quién?** (Cliente): `la-lily`, `acme-corp`.
2. **¿Qué área técnica?** (Disciplina): `bi`, `data-analytics`, `software`.
3. **¿Sobre qué trata?** (Dominio): `financiero`, `ventas`, `stock`, `rrhh`.
4. **¿Con qué se hizo?** (Tecnología): `power-bi`, `sql`, `python`, `focus`.

> **Ejemplo:** Para el financiero de La Lily, los topics son: `la-lily`, `bi`, `financiero`, `power-bi`, `sql`.

---

## 3. Power BI & Proyectos de Datos
* **Formato Obligatorio:** Uso exclusivo de proyectos de Power BI (`.pbip`).
* **Git vs. Drive:** Está terminantemente **PROHIBIDO** sincronizar carpetas de Git con Google Drive, OneDrive o Dropbox. La sincronización externa corrompe el índice de Git.
* **Ignorar Basura:** Todo repositorio debe incluir un archivo `.gitignore` para evitar subir archivos temporales, copias locales o caché (`*.pbit`, `**/cache.abf`, etc.).

---

## 4. Estándar de Commits (Conventional Commits)
No aceptamos mensajes mediocres. El historial debe ser una bitácora de ingeniería:
* `feat(area):` Nueva funcionalidad (ej: un nuevo gráfico o tabla).
* `fix(area):` Corrección de un error (ej: corregir medida DAX).
* `docs:` Cambios en documentación o README.
* `perf:` Mejoras de rendimiento en el modelo o en el SQL.

---

## 5. Flujo de Trabajo
1. **Pull Requests:** Nada se mezcla en `main` sin una revisión de otro miembro (aunque seamos tres).
2. **Issues:** Cada tarea nace de un Issue. Si no hay Issue, el trabajo no existe.
3. **Drafts:** Usa *Draft Pull Requests* para trabajo en progreso que requiera visibilidad sin mergear.

---

> "El orden no es una sugerencia, es la base de nuestra escalabilidad."  
> — *El Arquitecto*
