# .github
Muestra cómo trabajamos internamente, cómo nombramos repositorios y cómo gestionamos proyectos.

# 🏛️ Manifiesto de Estándares: [Data Trends]

Este repositorio contiene la **ÚNICA VERDAD** sobre cómo se gestiona el código, los datos y la documentación en nuestra consultora. El incumplimiento de estas normas será tratado como negligencia técnica.

## 1. Nomenclatura de Repositorios (kebab-case)
No aceptamos espacios, guiones bajos ni mayúsculas. Los repositorios deben seguir este patrón:
`[prefijo]-[cliente]-[proyecto]-[componente]`

### Prefijos Autorizados:
| Prefijo | Uso | Ejemplo |
| :--- | :--- | :--- |
| `bi-` | Proyectos de Power BI, Tableau, ETLs. | `bi-acme-ventas-report` |
| `app-` | Desarrollo de software y aplicaciones. | `app-stark-portal-api` |
| `cons-` | Consultoría pura, auditorías y scripts. | `cons-wayne-data-audit` |
| `infra-` | Automatización y DevOps. | `infra-global-docker-tools` |

---

## 2. Power BI & Proyectos de Datos
* **Formato:** Es obligatorio el uso de proyectos de Power BI (`.pbip`).
* **Git vs. Drive:** Está terminantemente **PROHIBIDO** sincronizar carpetas de Git con Google Drive, OneDrive o Dropbox. La sincronización externa corrompe el índice de Git.
* **Ignorar Basura:** Todo repositorio de Power BI debe incluir el `.gitignore` estándar para evitar subir archivos temporales y caché.

---

## 3. Estándar de Commits (Conventional Commits)
Los mensajes de commit deben ser descriptivos. No quiero ver "cambios" o "arreglos".
* `feat(area):` Nueva funcionalidad.
* `fix(area):` Corrección de un error.
* `docs:` Cambios en documentación.
* `perf:` Mejoras de rendimiento en DAX o procesos.

**Ejemplo:** `fix(etl): corregir limpieza de nulos en tabla clientes`

---

## 4. Flujo de Trabajo
1. **Pull Requests:** Nada se mezcla en `main` sin una revisión rápida (aunque seamos tres).
2. **Issues:** Cada tarea debe tener un Issue en GitHub. Si no hay Issue, no hay trabajo oficial.
3. **Drafts:** Si estás trabajando en algo incompleto, abre un *Draft Pull Request*.

---

> "El orden no es una sugerencia, es la base de nuestra escalabilidad."  
> — *El Arquitecto*
