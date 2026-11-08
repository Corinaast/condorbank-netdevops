# 🖧 Proyecto portable de GNS3

`ProyectoSemestral_NetDevOps.gns3project` es el proyecto completo: topología, configuraciones de arranque, VPCS y definiciones de los contenedores Docker.

## Requisitos

| Componente | Imagen / versión |
|---|---|
| GNS3 | 2.2.57 o superior |
| Router IOU | `i86bi_linux-adventerprisek9-ms.155-2.T.bin` |
| Switch multicapa IOU | `i86bi-linux-l2-adventerprisek9-15.2a.bin` |
| Servidores | Docker `gns3/alpinet:latest` |
| Hosts | VPCS |

## Importar

1. **File → Import portable project**.
2. Selecciona el archivo `.gns3project`.
3. Comprueba que las imágenes IOU y Docker tengan exactamente los nombres indicados.
4. Arranca todos los nodos y espera la convergencia (1–2 minutos).
5. Abre las consolas de los equipos y ejecuta las verificaciones del [README principal](../README.md).

## Credenciales de laboratorio

- Usuario: `admin`
- Contraseña / `enable secret`: `CondorBank2026!`

> Las credenciales originales del laboratorio fueron reemplazadas antes de publicar el proyecto. Cámbialas si lo reutilizas fuera de un entorno aislado.
