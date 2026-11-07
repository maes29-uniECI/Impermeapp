# ImpermeApp

Prototipo de ImpermeApp: reporte de humedades y filtraciones, cotización, agenda y seguimiento del servicio en vivo, con panel para el equipo.

**App publicada:** https://maes29-unieci.github.io/Impermeapp/

## Cómo funciona

| Parte | Dónde vive |
|---|---|
| App (cliente y panel del equipo) | `index.html`, publicada con GitHub Pages |
| Datos en tiempo real | Firebase Firestore (proyecto `impermeapp`) |
| Inicio de sesión | Firebase Authentication, por celular con código SMS |
| Seguridad | `firestore.rules`, publicadas en Firestore → Reglas |

Cada cliente solo ve sus solicitudes, su cuenta y su chat. El equipo ve y administra todo.

## Cuentas para la demo

| Rol | Celular | Código |
|---|---|---|
| Cliente de ejemplo | 300 123 4567 | 123456 |
| Equipo (panel) | 310 555 0000 | 654321 |

Son números de prueba de Firebase: no envían SMS ni tienen costo. El panel se abre desde "Acceso del equipo" en la pantalla de inicio.

## Agregar a alguien al equipo

El celular debe estar en dos lugares, con el formato `+57XXXXXXXXXX`:

1. `index.html`: en la lista `ADMIN_PHONES`.
2. `firestore.rules`: en la función `isAdmin()`. Después de cambiarla, cópiala en Firebase → Firestore → Reglas → Publicar.

## Editar la app

- Desde el navegador: en este repositorio presiona la tecla `.` para abrir el editor, o abre `index.html` y toca el lápiz.
- Con Claude Code en la web (claude.ai/code): conecta GitHub, elige este repositorio y pide los cambios.

Cada cambio guardado en la rama `main` se publica solo en GitHub Pages en uno o dos minutos.
