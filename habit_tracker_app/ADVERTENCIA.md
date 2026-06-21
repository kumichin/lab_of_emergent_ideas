# Advertencia sobre visualización de la interfaz (Streamlit)

Este proyecto actualmente presenta un problema de visualización en la interfaz desarrollada con Streamlit.

## Problema detectado

En ciertas secciones de la aplicación, el color del texto no se renderiza correctamente en función del fondo. Esto provoca situaciones como:

- Texto claro sobre fondos claros (invisible o difícil de leer)
- Texto oscuro sobre fondos oscuros (también ilegible en algunos casos)

En algunos casos, el texto solo se vuelve legible al seleccionarlo con el ratón, lo que indica un problema de CSS y/o estilos internos de Streamlit.

## Causa probable

El problema está relacionado con:

- Sobrescritura de estilos CSS globales en Streamlit
- Conflictos entre estilos personalizados y estilos internos del framework
- Limitaciones del control de estilos en componentes nativos de Streamlit

##  Estado actual

Se han intentado diferentes soluciones mediante CSS personalizado, pero el comportamiento sigue siendo inconsistente debido a la forma en la que Streamlit gestiona el renderizado de componentes.

## Impacto

- Afecta a la legibilidad de la interfaz
- Reduce la usabilidad en ciertos temas o combinaciones de color
- Dificulta una experiencia visual consistente

## Posibles soluciones futuras

Se están valorando varias opciones:

- Migración a frameworks con control total del frontend como:
  - Vercel (Next.js)
  - Aplicación web con HTML, CSS y JavaScript puro
  - Otras alternativas con mayor control del DOM

- Rediseño completo del sistema de estilos dentro de Streamlit (como solución intermedia)

## Conclusión

El problema no está en los datos ni en la lógica del sistema, sino en las limitaciones de personalización visual del framework actual.

Se considera una mejora futura la migración a una tecnología con control total del frontend para garantizar una experiencia de usuario consistente y profesional.
