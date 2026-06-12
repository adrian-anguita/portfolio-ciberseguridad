## Configuración de Red Inicial

### Objetivo

Preparar la infraestructura de red básica del servidor Windows Server 2022 antes de desplegar los servicios de red (DNS, DHCP, Active Directory, etc.).


## Descripción
### Hardware asignado
| Parámetro | Valor |
|---|---|
| Red Adaptador 1 | Red interna (intnet) |
| Red Adaptador 2 | Red externa (NAT) |

### Configuración de Adaptadores de Red

La máquina virtual dispone de dos interfaces de red configuradas en VirtualBox:

### Adaptador 1 - Red Interna (IntNet)
- Modo de red: Internal Network (IntNet).
- Función: comunicación privada entre los equipos del laboratorio.
- Esta red será utilizada por los clientes y servicios internos de la infraestructura.


### Adaptador 2 - NAT
- Modo de red: NAT.
- Función: proporcionar acceso a Internet al servidor.
- Utilizado para la descarga de actualizaciones, software y paquetes necesarios durante la instalación.


## Configuración IP Estática

Se asigna una dirección IP fija a la interfaz de red interna para garantizar que los servicios de infraestructura mantengan siempre la misma dirección.

### Identificación de Interfaces

Para facilitar la administración se renombran las tarjetas de red:

- WAN → Adaptador NAT
- LAN → Adaptador IntNet

### Verificación de Conectividad

Se realizan las siguientes comprobaciones:

- Verificación de la configuración mediante ipconfig /all.
- Comprobación de conectividad local mediante ping.
- Verificación de acceso a Internet a través del adaptador NAT.
- Validación de la comunicación entre máquinas de la red interna.

### Resultado

El servidor queda preparado como base de la infraestructura de red, con conectividad externa e interna correctamente configurada y listo para la instalación de los servicios DNS, DHCP y Active Directory.
