# CI/CD Pipeline - TechMarket

## Descripción
Este proyecto implementa un pipeline CI/CD utilizando GitHub Actions, basado en plantillas reutilizables para las etapas de build, test y deploy.

## Estructura del proyecto
.github/workflows/
- pipeline.yml
- template_build.yml
- template_test.yml
- template_deploy.yml

## Plantillas

### Build
Encargada de preparar el entorno y simular la construcción del proyecto.

### Test
Ejecuta pruebas simuladas para validar el correcto funcionamiento.

### Deploy
Simula el despliegue en un entorno definido.

## Acciones externas utilizadas

- **actions/checkout@v4**
  Permite clonar el repositorio dentro del runner, facilitando el acceso al código.

- **actions/setup-node@v4**
  Configura el entorno de ejecución Node.js, asegurando compatibilidad.

Estas acciones fueron seleccionadas por su confiabilidad, uso estándar en la industria y compatibilidad con múltiples entornos.

## Parametrización

Las plantillas utilizan parámetros para su reutilización:

- `node_version`: versión de Node.js
- `environment`: entorno de despliegue

Ejemplo de uso:

```yaml
uses: ./.github/workflows/template_build.yml
with:
  node_version: "18"