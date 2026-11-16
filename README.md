[README.md](https://github.com/user-attachments/files/34899706/README.md)
# Stream Station for Linux

Español: [README.es.md](README.es.md)

A service and graphical editor for the **Redragon Ragnaros SS-552** (USB `0200:3001`): 10 keys with screens, 4 knobs and an
800×128 px touch strip. An independent project made for Linux (tested on KDE Plasma).

> Not affiliated with Redragon and contains no code from other drivers. "Redragon" and "Ragnaros" are trademarks of their owners.

## Features
- **Keys:** icon + action. Actions from a list, installed applications, keyboard shortcuts, programs, files, multi-actions,
  pages and layers.
- **Knobs:** turn right, turn left and press, with templates (volume, brightness, pages, media).
- **Touch strip:** one canvas showing metrics, text, images or animated GIFs; each touch zone runs an action, and you can
  change page or scene by swiping.
- **Scenes:** key layouts that switch by themselves depending on the application or game in front, with a default scene,
  ordering, duplication and import/export.
- **Device:** serial number, brightness and a custom start-up logo.
- **System:** screen off when idle, standby with a wake-up key, following the session lock, volume and microphone, media,
  lock and suspend.
- **Interface:** light, dark or system theme; 20 languages; updates from GitHub and start with the computer.

## Install (only touches your user)
```bash
./install.sh --apply                                   # program, icon and menu entry
systemctl --user enable --now streamstation.service    # the service, with your session
```
USB access needs a `udev` rule (`udev/70-streamstation.rules`); it needs administrator rights once and the installer prints
the commands. Then open **Stream Station** from the application menu, or run `streamstation ui`.

To uninstall: `./install.sh --uninstall` (your profiles in `~/.config/streamstation/` are kept).

## Dependencies
Python 3.10+, PySide6, Pillow, PyYAML, pyusb (libusb) and python-evdev. Used when present: `wpctl`, `busctl`, `loginctl`,
`systemctl`, `xdg-open`.

## Status
Version 0.1.x, in development. Tested with a single device and on KDE Plasma; other desktops may have limited features
(for example, automatic scene switching per application uses KWin). What has been tested and what is pending is listed in
`FEATURES.md` and `PENDIENTES.md` (in Spanish).

## Third-party material
The manufacturer's icons are not included. Without them the program draws a fallback icon with the action's initial.
The font is the system one.

[README.es.md](https://github.com/user-attachments/files/34899747/README.es.md)
# Stream Station para Linux

English: [README.md](README.md)

Servicio y editor gráfico para el **Redragon Ragnaros SS-552** (USB `0200:3001`): 10 teclas con pantalla, 4 perillas y una
franja táctil de 800×128 px. Proyecto independiente, hecho para Linux (probado en KDE Plasma).

> No está afiliado a Redragon ni usa código de otros controladores. «Redragon» y «Ragnaros» son marcas de sus dueños.

## Qué hace
- **Teclas:** icono + acción. Acciones de una lista, aplicaciones instaladas, atajos de teclado, programas, archivos,
  multi-acciones, páginas y capas.
- **Perillas:** girar a la derecha, a la izquierda y pulsar, con plantillas (volumen, brillo, páginas, multimedia).
- **Franja táctil:** un único lienzo con métricas, texto, imágenes o GIF animados; cada zona táctil ejecuta una acción, y se
  puede cambiar de página o de escena deslizando el dedo.
- **Escenas:** distribuciones de teclas que se activan solas según la aplicación o el juego en primer plano, con escena
  predeterminada, orden, duplicado e importación/exportación.
- **Dispositivo:** número de serie, brillo y logo de arranque propio.
- **Sistema:** apagado de pantalla por inactividad, standby con tecla de despertar, seguir el bloqueo de sesión, volumen y
  micrófono, multimedia, bloqueo y suspensión.
- **Interfaz:** tema claro, oscuro o del sistema; 20 idiomas; actualizaciones desde GitHub y arranque con el equipo.

## Instalar (solo toca tu usuario)
```bash
./install.sh --apply                                   # programa, icono y entrada de menú
systemctl --user enable --now streamstation.service    # el servicio, con tu sesión
```
El acceso al USB necesita una regla `udev` (`udev/70-streamstation.rules`); requiere administrador una vez y el instalador
imprime los comandos. Después abrí **Stream Station** desde el menú de aplicaciones, o con `streamstation ui`.

Para desinstalar: `./install.sh --uninstall` (tus perfiles en `~/.config/streamstation/` se conservan).

## Dependencias
Python 3.10+, PySide6, Pillow, PyYAML, pyusb (libusb) y python-evdev. Se usan si existen: `wpctl`, `busctl`, `loginctl`,
`systemctl`, `xdg-open`.

## Estado
Versión 0.1.x, en desarrollo. Probado con un único equipo y en KDE Plasma; otros escritorios pueden tener funciones limitadas
(por ejemplo, el cambio automático de escena por aplicación usa KWin). Los detalles de lo probado y lo pendiente están en
`FEATURES.md` y `PENDIENTES.md`.

## Material de terceros
Los iconos del fabricante no se incluyen. Sin ellos el programa dibuja un icono de respaldo con la inicial de la acción.
La tipografía es la del sistema.

