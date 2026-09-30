# Tickets del Departamento Legal

Tablero de seguimiento de las solicitudes al Departamento Legal registradas en el Sistema de Tickets de ERC Capital Corp.

**Clasificación: Confidencial.** El repositorio debe permanecer privado y el sitio solo debe publicarse con acceso restringido.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | El tablero. No hace falta tocarlo para actualizar datos. |
| `datos.json` | Los tickets de Legal que muestra el tablero. Es lo único que cambia en cada actualización. |
| `staticwebapp.config.json` | Pide inicio de sesión con cuenta ERC (Microsoft Entra ID) si el sitio se publica en Azure Static Web Apps. |
| `.gitignore` | Evita subir por error las exportaciones originales (.csv / .xlsx). |

## Cómo actualizar

1. Exportar del Sistema de Tickets los tickets cerrados y en espera.
2. Generar un nuevo `datos.json` con el mismo formato.
3. Reemplazar `datos.json` en el repositorio, hacer commit y push.

## Cómo verlo en tu computadora

El tablero lee `datos.json`, así que no abre con doble clic. Desde la carpeta del repositorio ejecuta:

```
python -m http.server 8000
```

y abre `http://localhost:8000` en el navegador.

## Nota

La exportación actual no incluye la descripción de los tickets. Las definiciones y limitaciones de los datos están en la sección "Cómo leer los datos" del tablero.

---
Generado con IA (Claude - ERC AI Workspace) - Confidencial
