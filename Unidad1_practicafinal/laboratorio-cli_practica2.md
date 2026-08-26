# Laboratorio CLI — Registro de comandos

Este documento reúne las capturas de la práctica de terminal, en orden, con un breve comentario del flujo que se realizó en cada paso.

---

## 1. Navegación entre directorios (`cd`)

![captura1](./imagenes/captura1.png)

Se navega desde `docs` hacia `../src` usando una ruta relativa. El prompt confirma el cambio a `~/laboratorio-cli/src`.

---

## 2. Volver al directorio anterior con `cd -`

![captura2](./imagenes/captura2.png)

Desde `docs`, se usa `cd -` para regresar a `/home/ubuntu/laboratorio-cli/src` (el directorio anterior). Luego `ls` muestra el contenido de `src`: `main.py` y `test.py`.

---

## 3. Revisando el historial de comandos `cd`

![captura3](./imagenes/captura3.png)

Se ejecuta `history | grep 'cd'` para revisar todos los comandos `cd` utilizados durante la sesión, incluyendo rutas absolutas, relativas, `cd -`, `cd ~`, y variaciones con errores tipográficos (`cd..`, `cd:`).

---

## 4. Creando un alias (`alias ll`)

![captura4](./imagenes/captura4.png)

Se define el alias `ll` para el comando `ls -lah --color=auto`, facilitando listados detallados con colores.

---

## 4.1 Probando el alias `ll`

![captura4_1](./imagenes/captura4_1.png)

Al ejecutar `ll` dentro de `docs`, se muestra el listado detallado (`total 0`, permisos, propietario, tamaño y fecha) de los archivos `guia.md` y `notas.md`.

---

## 5. Verificando la definición del alias (`type ll`)

![captura5](./imagenes/captura5.png)

Con `type ll` se confirma que el alias sigue apuntando a `ls lah color=auto`, verificando su configuración actual.

---

## 6. Usando el alias con un argumento (`ll docs`)

![captura6](./imagenes/captura6.png)

Se ejecuta `ll docs` desde el directorio raíz del laboratorio, mostrando el mismo listado detallado del subdirectorio `docs` sin necesidad de entrar en él.

---

## 7. Eliminando el alias (`unalias ll`)

![captura7](./imagenes/captura7.png)

Finalmente, se elimina el alias con `unalias ll`, dejando el shell en su estado original sin el atajo personalizado.

---

### Resumen del flujo
1. Se practicó la navegación con rutas relativas y `cd -`.
2. Se revisó el historial de comandos para auditar la navegación.
3. Se creó, probó, verificó y finalmente eliminó un alias personalizado (`ll`).
