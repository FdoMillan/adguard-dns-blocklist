# adguard-dns-blocklist

Lista avanzada de bloqueo DNS optimizada para AdGuard Home, diseñada para filtrado granular de redes sociales, rastreadores y contenido no deseado en redes controladas.

## Descripción

Este proyecto provee listas de dominios organizadas por categorías, listas para importar directamente en AdGuard Home. Su uso es ideal en despliegues donde el tráfico DNS es forzado vía redirección (ejemplo: reglas `nftables` en OpenWrt, modo puente L2).

## Estructura

- `/blocklists/`: Listas clasificadas por tipo de contenido (ej. social, ads, tracking).
- `/custom/`: Dominios específicos personalizados para tu entorno.
- `README.md`: Este documento.

## Instalación

1. Clona o descarga este repositorio.
2. Importa las listas deseadas en la sección **Filtro de DNS** de AdGuard Home.
3. (Opcional) Automatiza la actualización mediante script o integración con GitHub Actions.

## Integración recomendada

- **OpenWrt + nftables**: Redirige todo el tráfico DNS de los clientes objetivo a tu instancia AdGuard Home para aplicar el filtrado.
- Filtra por cliente usando IP, MAC o sets personalizados en tu firewall.

## Ejemplo de uso en AdGuard Home

En la interfaz de AdGuard Home, navega a:
Configuración → Filtros → Agregar filtro → Ruta local o URL del raw de este repositorio.


## Estado del proyecto

En producción en redes con Orange Pi + OpenWrt 24.x en modo puente L2, integrado con reglas personalizadas de nftables.

## Contribuciones

Sugerencias y pull requests son bienvenidos.

---

> Para preguntas técnicas o casos de uso avanzados, abre un issue.
