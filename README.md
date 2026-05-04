# dashboard

Estructura base propuesta para evolucionar este repositorio como una aplicacion de dashboard mantenible.

## Estructura recomendada

```text
dashboard/
+-- README.md
+-- package.json
+-- .env.example
+-- .gitignore
+-- public/
|   +-- favicon.ico
|   +-- assets/
+-- src/
|   +-- main/
|   |   +-- app/
|   |   +-- config/
|   |   +-- routes/
|   |   +-- bootstrap/
|   +-- features/
|   |   +-- auth/
|   |   +-- dashboard/
|   |   +-- reports/
|   |   +-- users/
|   +-- shared/
|   |   +-- components/
|   |   +-- hooks/
|   |   +-- services/
|   |   +-- utils/
|   |   +-- types/
|   +-- styles/
|       +-- base/
|       +-- components/
|       +-- themes/
+-- tests/
|   +-- unit/
|   +-- integration/
|   +-- e2e/
+-- docs/
|   +-- architecture.md
|   +-- setup.md
|   +-- decisions/
+-- scripts/
|   +-- dev/
|   +-- build/
|   +-- maintenance/
+-- .github/
    +-- workflows/
        +-- ci.yml
        +-- deploy.yml
```

## Que va en cada carpeta

- `public/`: archivos estaticos que se sirven tal cual, como iconos, imagenes o fuentes.
- `src/main/`: punto de entrada de la aplicacion, configuracion global, rutas y arranque.
- `src/features/`: modulos funcionales independientes. Cada feature deberia agrupar sus vistas, componentes, servicios y tests cercanos.
- `src/shared/`: piezas reutilizables por varias features: componentes comunes, utilidades, tipos y servicios compartidos.
- `src/styles/`: estilos globales, variables, temas y estilos de componentes base.
- `tests/`: pruebas separadas por nivel cuando no vivan junto al codigo.
- `docs/`: documentacion tecnica, decisiones de arquitectura y guias de instalacion.
- `scripts/`: comandos auxiliares para desarrollo, builds, migraciones o mantenimiento.
- `.github/workflows/`: automatizaciones de CI/CD.

## Convenciones sugeridas

- Mantener cada feature aislada para reducir dependencias cruzadas.
- Reutilizar codigo desde `src/shared/` solo cuando ya exista una necesidad real.
- Documentar decisiones importantes en `docs/decisions/`.
- Crear `.env.example` con las variables necesarias, sin secretos reales.
- Automatizar checks basicos en CI: lint, tests y build.

## Siguientes pasos

1. Elegir el stack principal del proyecto.
2. Crear los archivos minimos de configuracion.
3. Definir scripts de desarrollo, test y build.
4. Anadir una primera pantalla funcional del dashboard.
5. Configurar CI para validar cada cambio.
