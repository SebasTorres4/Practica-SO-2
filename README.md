# Práctica 2 — Sockets, hilos y comunicación cliente-servidor en Linux

Sistemas Operativos · Universidad Nacional de Colombia · Ingeniería de Sistemas

Un **cliente** de consola y un **servidor** concurrente se comunican por **sockets TCP** desde **dos computadores distintos**. El servidor busca registros en un archivo CSV (sin cargarlo completo en memoria) y atiende a cada cliente conectado con un **hilo POSIX** independiente.

> El documento de entrega es [`LEEME.md`](LEEME.md). Este archivo solo resume cómo está organizado el trabajo.

## Integrantes y reparto

| Usuario de GitHub | Parte principal | Issues |
|---|---|---|
| SebasTorres4 | Acuerdos iniciales, dataset y búsqueda en el CSV | #1, #2 |
| Xedroc422 | Protocolo y servidor (socket de escucha y `accept()`) | #3, #4 |
| angutierrezgi | Hilos de atención y manejo de desconexiones | #5, #6 |
| KevinVerjan | Cliente (menú y conexión), Makefile y estructura | #7, #8 |
| Todos | Prueba en dos computadores, observaciones, LEEME y ensayo de sustentación | #9, #10, #11 |

## Orden de trabajo

1. **#1 Acuerdos iniciales** — nadie programa antes de cerrarlo.
2. En paralelo: **#2** búsqueda, **#3** protocolo, **#8** Makefile.
3. **#4** servidor, **#5** hilos y **#7** cliente (pueden empezar con versiones provisionales).
4. **#6** desconexiones → **#9** prueba entre dos computadores → **#10** observaciones → **#11** LEEME y ensayo.

## Forma de trabajo con Git

- `main` siempre debe compilar. Cada Issue se trabaja en su propia rama (por ejemplo `feature/servidor`) y entra a `main` con un Pull Request que revisa otra persona.
- En el Pull Request se escribe `Closes #N` para cerrar el Issue al unirlo.
- Los ejecutables (`bin/`) y los CSV grandes no se suben (ver `.gitignore`).
