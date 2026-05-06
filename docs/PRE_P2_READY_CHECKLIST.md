# PRE P2 Ready Checklist

Fecha: 2026-05-05
Repositorio: Andres-valencia-platform

Objetivo: dejar la web lista para iniciar P2 (A/B testing) aun sin testimonios publicables.

## Estado actual (implementado)

- Prueba social en modo transparente:
  - No se muestran claims no verificados.
  - Se muestra evidencia tecnica y de implementacion.
- Formularios listos para medicion base:
  - Captura de `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `utm_term`.
  - Registro de `form_start` y `form_submit` con datos de calificacion.
- Eventos base activos:
  - Home: `view_home`, `click_*`, `scroll_50`, `scroll_90`, `form_start`, `form_submit`.
  - Landing PropTech: `view_proptech_landing`, `click_*`, `form_start_proptech`, `form_submit_proptech`.

## Pendiente operativo (sin tocar codigo)

1. Publicar preview y revisar links:
   - Home: index.html
   - Landing: proptech-manager.html
2. Confirmar en analitica que llegan eventos del `dataLayer`.
3. Correr baseline minimo 7 dias antes del primer A/B test.

## Baseline recomendado (7 dias)

- Visitas home.
- Visitas landing PropTech.
- Click CTA principal home.
- Click WhatsApp (nav, contacto, sticky).
- Form starts.
- Form submits.
- Scroll 50% y 90%.
- Lead calificado por `tamano_negocio` y `urgencia`.

## Plantilla para prueba social real (llenar al cerrar cada proyecto)

- Cliente/empresa:
- Rol del contacto:
- Punto de partida (antes):
- Solucion implementada:
- Resultado medible (despues):
- Tiempo para ver resultado:
- Testimonio literal autorizado:
- Permiso de publicacion (si/no):
- Link de evidencia (captura, dashboard o demo):

## Regla para pasar a P2

Iniciar P2 solo si:
- Hay al menos 7 dias de baseline limpio.
- Eventos de CTA y formulario estan llegando.
- Hay minimo 1 testimonio autorizado o 2 casos con resultado medible validado.
