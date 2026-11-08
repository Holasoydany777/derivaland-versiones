# Derivaland — versiones

Aquí se publican las versiones del modpack de Coralosis para el Launcher Derivaland.

- `version.json` dice cuál es la última versión y dónde está su zip (en la carpeta `modpack/`, solo se deja la última).
- En el launcher: Ajustes > Enlace de actualizaciones:
  `https://raw.githubusercontent.com/Holasoydany777/derivaland-versiones/main/version.json`
  Con eso, cada versión nueva se instala sola al darle a Jugar.

## Launcher
- `launcher/` tiene el instalador del Launcher Derivaland (solo el último). Desde el 1.6.0 mira este repositorio solo, sin configurar nada.
- `launcher.minimo` en `version.json`: los launchers más viejos que ese (desde el 1.7.0) no dejan jugar hasta actualizarse.

## Launcher de admins
- `launcher-admin/` tiene el instalador del Launcher Derivaland Admin (solo el último); `launcher_admin` en `version.json` dice cuál es.
- Tiene una pestaña Admin para bloquear cuentas, elegir admins, publicar modpacks y launchers, y manejar el servidor por RCON. Todo lo que se hace queda en `registro.json`.
- Para hacer cambios necesita la clave de admin (un token de GitHub con permiso de escritura en este repositorio). Se pone una vez en la pestaña Admin y se guarda cifrada en ese PC.
- `admins` en `version.json`: si tiene a alguien, solo esas cuentas de Minecraft pueden usar el panel. Vacía = cualquiera con la clave.

## Cuentas bloqueadas
- `bloqueados` en `version.json`: cuentas de Minecraft que no pueden usar el launcher (desde el 1.7.0). Van por UUID, así que cambiarse el nombre no sirve.
- Para bloquear a alguien más, se añade `{ "uuid": "...", "nombre": "..." }`. El UUID sale en `https://api.mojang.com/users/profiles/minecraft/NOMBRE`. Para quitarlo, se borra su línea.
- `version.json` también dice cuál es el último launcher, así los launchers se actualizan solos.

## Herramientas (repuesto)
- `herramientas/` tiene copias de yt-dlp, ffmpeg y deno para Windows. El mod de altavoces las usa si no puede descargarlas de su web original (por ejemplo, cuando GitHub da error 504).
