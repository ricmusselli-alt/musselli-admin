# Musselli Admin — Arquitectura V1

Musselli Admin es el panel operativo del ecosistema. No contiene el código de las familias: las observa y administra mediante contratos.

## Funciones objetivo
- estado por familia;
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
- nunca inferir `ok` sin comprobación;
- separar código, runtime, datos y proveedores;
- no guardar secretos en GitHub;
- cada acción irreversible requiere trazabilidad;
- caída de una familia no bloquea el panel ni las demás.

## Fases
1. Inventario y health metadata.
2. Consulta runtime real.
3. Proveedores y costos.
4. Publicación aprobada y rollback.
5. Cuenta Musselli, usuarios y permisos.

Estado actual: fase 1 preparada; runtime y servicios externos aún requieren conexión real.
