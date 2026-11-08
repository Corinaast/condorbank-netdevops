# ⚙️ Configuraciones de los equipos

Una configuración por dispositivo, extraída del proyecto GNS3 y renombrada con el `hostname` real.

| Equipo | Sede | Rol | Aspectos relevantes |
|---|---|---|---|
| `R-QUITO.cfg` | Quito | Router de borde / núcleo | OSPFv2 y OSPFv3, ABR de las áreas 1 y 2, WAN en triángulo |
| `MLS1-QUITO.cfg` | Quito | Switch multicapa | SVI, HSRP activo en VLAN 10/30/50, raíz STP de esas VLAN, LACP |
| `MLS2-QUITO.cfg` | Quito | Switch multicapa | SVI, HSRP activo en VLAN 20/40, raíz STP de esas VLAN, LACP |
| `SW1-QUITO.cfg` | Quito | Switch de acceso | Doble conexión LACP hacia MLS1 y MLS2 (Po1/Po2) |
| `SW2-QUITO.cfg` | Quito | Switch de acceso | Troncal hacia los dos switches multicapa |
| `SW3-QUITO.cfg` | Quito | Switch de acceso | Troncal hacia los dos switches multicapa |
| `SW-DMZ.cfg` | Quito | Switch de acceso DMZ | VLAN 50 hacia SRV-WEB y SRV-DNS |
| `R-GYE.cfg` | Guayaquil | Router de borde | OSPF área 1, `area 1 range 10.10.4.0/23`, WAN |
| `MLS-GYE.cfg` | Guayaquil | Switch multicapa | VLAN 110/120/130, SVI y HSRP |
| `MLS2-GYE.cfg` | Guayaquil | Switch multicapa | Segundo equipo de distribución, HSRP |
| `SW1-GYE.cfg` | Guayaquil | Switch de acceso | Segmentos de Guayaquil |
| `R-CUE.cfg` | Cuenca | Router de borde | OSPF área 2, `area 2 range 10.10.6.0/24`, WAN |
| `MLS-CUE.cfg` | Cuenca | Switch multicapa | VLAN 210/220, única puerta de enlace de la sede |
| `SW1-CUE.cfg` | Cuenca | Switch de acceso | Comercial y Wi-Fi clientes |

## 🔐 Credenciales

Las contraseñas originales del laboratorio fueron **reemplazadas** antes de publicar este repositorio por una credencial conocida:

- Usuario: `admin`
- Contraseña / `enable secret`: `CondorBank2026!`

Cámbialas si vas a reutilizar el proyecto fuera de un entorno aislado. El archivo `.gns3project` incluido en `gns3/` ya contiene las mismas credenciales de laboratorio.

## 🧪 Verificación rápida

```text
show vlan brief
show interfaces trunk
show etherchannel summary
show standby brief
show ip ospf neighbor
show ipv6 ospf neighbor
show ip route ospf
show ipv6 route ospf
```
