# Plan Maestro de Cambios para Vender Mas (Portafolio)

Fecha: 2026-05-05  
Repositorio: `Andres-valencia-platform`  
Archivo principal: `index.html`

Este documento consolida 5 auditorias: ICP/Oferta, Copy+Prueba Social, UX/CRO mobile-first, SEO+Analitica y Automatizacion+Experimentacion.

## Objetivo

Aumentar conversion de visitas a conversaciones comerciales y reuniones calificadas.

Metas iniciales (4-8 semanas):
- Visitante -> lead: 2.5% a 4%.
- Lead -> reunion: 20% a 35%.
- Respuesta a lead: < 5 minutos.

## Diagnostico Consolidado

1. Mensaje demasiado amplio: no filtra ICP principal.
2. CTA principal con mucha friccion (`mailto`) y sin WhatsApp/agenda/form.
3. Falta de prueba social concreta (resultados medibles).
4. Flujo mobile con friccion (menu/hamburguesa y conversion tardia).
5. Falta oferta empaquetada (alcance, tiempo, precio desde).
6. Falta tracking comercial serio (eventos + embudo).

## Prioridad P0 (Ejecutar esta semana)

## 1) Reenfocar posicionamiento (ICP + resultado)
- Hero orientado a inmobiliarias/pymes con dolor operativo claro.
- Promesa medible + CTA de accion inmediata.

### Copy base recomendado
- Headline: `Digitalizo tu operacion para que vendas mas y pierdas menos tiempo.`
- Subheadline: foco en pasar de Excel/chats/procesos sueltos a sistema con seguimiento y control.
- CTA primario: `Quiero un diagnostico de 20 min`.
- CTA secundario: `Ver PropTech Manager`.

## 2) Reemplazar friccion de contacto
- Quitar dependencia de `mailto` como unica accion.
- Implementar:
  - Boton WhatsApp con mensaje prellenado.
  - Formulario corto (nombre, WhatsApp, negocio, principal problema, urgencia).
  - Boton para agendar llamada (Calendly).

## 3) Oferta comercial visible
- Crear bloque `Planes y precios` para PropTech:
  - Base (desde COP 2.9M)
  - Pro (desde COP 5.9M)
  - Escala (a medida)
- Cada plan: para quien es, que incluye, tiempo estimado.

## 4) Prueba social + objeciones
- Agregar seccion `FAQ + Testimonios` antes de contacto.
- Incluir 2-3 mini casos formato `Antes -> Despues` con numeros.

## 5) Mobile CRO
- Habilitar menu mobile funcional.
- Sticky bar inferior en mobile con:
  - `WhatsApp`
  - `Diagnostico`
- Mantener CTA de contacto visible arriba y en mitad de pagina.

## 6) SEO + Tracking minimo
- Actualizar `title` y `meta description` con intencion transaccional.
- Agregar `canonical`, `robots`, `og:image`.
- Implementar schema: `Person`, `ProfessionalService`, `SoftwareApplication`, `WebSite`.
- Eventos minimos (GA4/PostHog/Plausible):
  - `click_primary_cta`
  - `click_whatsapp`
  - `form_start`
  - `form_submit`
  - `meeting_booked`
  - `scroll_50`, `scroll_90`

## Prioridad P1 (Siguiente sprint)

1. Reordenar secciones para flujo de conversion:
- Hero -> Prueba social -> Problema -> PropTech -> Demos -> FAQ -> Contacto.

2. Mejorar calidad de leads:
- Bloque `Para quien es / no es`.
- Micro-calificacion en formulario.

3. Mejorar pruebas:
- Sustituir testimonios de ejemplo por reales (nombre, cargo, empresa).
- Agregar 2-3 metricas reales por caso.

4. Landing dedicada para PropTech:
- URL especifica orientada a cierre comercial.

## Prioridad P2 (Optimizacion continua)

1. A/B test Hero (dolor vs resultado).
2. A/B test CTA (`Diagnostico` vs `Demo guiada`).
3. Lead magnet BOFU (checklist/guia operativa).
4. Score de lead y atribucion por UTM/canal.

## Plan de 4 Semanas (Ejecucion)

## Semana 1
- Implementar P0 de contacto (WhatsApp + Form + Agenda).
- Reescribir Hero + CTA + oferta principal.
- Activar tracking base.

## Semana 2
- Publicar FAQ/Testimonios + mini casos con resultados.
- Lanzar A/B test #1 (Hero/CTA).

## Semana 3
- Ajustar flujo por datos (clicks, scroll, leads).
- Mejorar secciones que pierden usuarios.

## Semana 4
- A/B test #2 (mecanismo de captura / CTA dual).
- Consolidar version ganadora y documentar baseline.

## Automatizacion de Leads (Minimo viable)

Herramientas sugeridas (inicio rapido):
- Form: Tally/Typeform.
- Agenda: Calendly.
- Automatizacion: Make o n8n.
- CRM: HubSpot Free.
- WhatsApp: WATI/Zoko o Cloud API.
- Analytics: GA4 + GTM + PostHog/Plausible.

Flujo:
1. Lead entra.
2. Crear lead en CRM con UTMs y etapa `Nuevo`.
3. Respuesta inmediata (WA + email).
4. Seguimiento automatico dias 1, 3, 7, 14.
5. Si agenda: mover a `Reunion agendada`.

## KPIs de Exito

Comercial:
- Tasa visita -> lead.
- Tasa lead -> reunion.
- Tasa reunion -> propuesta.
- Tasa propuesta -> cierre.

Producto de funnel:
- CTR CTA Hero.
- Clicks WhatsApp.
- Submit de formulario.
- Scroll a seccion contacto.

Operacion:
- Tiempo de primera respuesta.
- % leads calificados.

## Checklist de Implementacion Inmediata

- [x] Cambiar CTA principal a `Diagnostico 20 min`.
- [~] Implementar WhatsApp + Form + Agenda. (WhatsApp + Form listos, agenda pendiente de herramienta final)
- [x] Crear bloque de planes y precios.
- [x] Agregar FAQ + mini casos y prueba verificable.
- [x] Activar tracking de conversion y embudo base.
- [x] Hacer menu mobile funcional + sticky conversion bar.

## Gate antes de P2

Para pasar a P2 se requiere:
- Baseline de minimo 7 dias con eventos activos (`click_*`, `form_start`, `form_submit`, `scroll_*`).
- Validar que llegan UTMs en formularios.
- Tener al menos 1 testimonio autorizado o 2 casos con resultado medible real.

## Avance P2 (inicio)

- [x] A/B test Hero (dolor vs resultado) activo en `index.html`.
- [x] A/B test CTA (`Diagnostico` vs `Demo guiada`) activo en `index.html`.
- [x] Lead magnet BOFU publicado (`assets/downloads/checklist-digitalizacion-operativa-bofu.md`).
- [x] Score de lead y atribucion por UTM/canal en formularios (`index.html` y `proptech-manager.html`).

## Fuentes (Entregables Agentes)

- `ICP-OFERTA-CAMBIOS.md`
- `docs/copy-conversion-prueba-social.md`
- `docs/ux-cro-mobile-first-audit.md`
- `docs/SEO-COMERCIAL-ANALITICA-PLAN.md`
- `docs/LEADS_AUTOMATIZACION_EXPERIMENTACION_4_SEMANAS.md`
