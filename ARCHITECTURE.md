# Musselli Admin — Arquitectura V1

Musselli Admin es el panel operativo del ecosistema. No contiene el código de las familias: las observa y administra mediante registros y contratos explícitos.

## Funciones objetivo
- estado operativo por familia basado en verificaciones reales, sin estructura legacy `Health`;
- versión conocida;
- última publicación aprobada;
- último backup conocido;
- enlaces rápidos;
- proveedores/planes/costos/renovaciones;
- consumo cuando exista API;
- alertas de seguridad;
- rollback documentado;
- usuarios/actividad/permisos cuando la identidad común esté implementada.

## Principios
- nunca inferir funcionamiento correcto sin comprobación;
- separar código, runtime, datos y proveedores;
- no guardar secretos en GitHub;
- cada acción irreversible requiere trazabilidad;
- caída de una familia no bloquea el panel ni las demás;
- `Health` es una estructura antigua y queda explícitamente excluida del modelo actual.

## Fases
1. Inventario de módulos, versiones, publicación y backups.
2. Verificación de runtime real mediante mecanismos propios de cada familia/infraestructura, no mediante `Health`.
3. Proveedores y costos.
4. Publicación aprobada y rollback.
5. Cuenta Musselli, usuarios y permisos.

Estado actual: inventario estructural preparado; runtime y servicios externos requieren conexión real antes de poder certificarse.
