# P2 Experiment Setup

Fecha: 2026-05-05

## Experimentos activos

1. Hero A/B (home)
- `resultado`
- `dolor`

2. CTA A/B (home)
- `diagnostico`
- `demo`

## Como forzar variantes manualmente

- Hero dolor + CTA demo:
  - `/?ab_hero=dolor&ab_cta=demo`
- Hero resultado + CTA diagnostico:
  - `/?ab_hero=resultado&ab_cta=diagnostico`

Las variantes se guardan en `localStorage` con llaves:
- `ab_hero_v1`
- `ab_cta_v1`

## Eventos que deben verse en analitica

- `view_home`
- `ab_variant_assigned`
- `click_primary_cta`
- `click_secondary_cta`
- `click_lead_magnet_download`
- `click_lead_magnet_whatsapp`
- `form_start`
- `form_submit`
- `scroll_50`
- `scroll_90`

Landing PropTech:
- `view_proptech_landing`
- `form_start_proptech`
- `form_submit_proptech`

## Campos clave enviados en submit

- `tamano_negocio`
- `urgencia`
- `interes` (home)
- `lead_score`
- `lead_tier`
- `attribution_channel`
- `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `utm_term`

## Regla de lectura rapida (7 dias)

- Variante ganadora Hero: mayor CTR en `click_primary_cta` y mayor `form_start`.
- Variante ganadora CTA: mayor `form_submit` con mejor mix `lead_tier` (mas `warm/hot`).
- Canal prioritario: mayor conversion a submit por `attribution_channel`.
