# Deployment Notes

## Portafolio publico
Este repo se publica como sitio estatico.

### Checklist antes de publicar
1. Validar cambios locales con `git status`.
2. Confirmar que `index.html` y `proptech-manager.html` tengan metadatos SEO correctos.
3. Confirmar que `robots.txt` y `sitemap.xml` existan.
4. Verificar que `.vercelignore` limite el deploy a archivos publicos.
5. Probar local con `run-portfolio.cmd` en desktop y mobile.
6. Si se desea webhook de leads, definir `window.AV_LEADS_WEBHOOK` en el HTML o GTM.

### Captura de leads
- El formulario ahora registra tracking + score y abre WhatsApp con el resumen del lead.
- Si se define `window.AV_LEADS_WEBHOOK` (URL HTTPS), se envia tambien el payload JSON por `POST`.
- Sin webhook, el flujo comercial sigue funcionando por WhatsApp.

### GitHub
1. Confirmar estado con `git status`.
2. Hacer commit desde la raiz del repo principal.
3. Empujar a `origin`.

### Vercel
1. La raiz del proyecto es este repo principal.
2. El portafolio no necesita build step.
3. El despliegue puede hacerse con `vercel --prod` o conectando el repo en Vercel para publicar en cada push.
4. El archivo `.vercelignore` deja fuera carpetas internas (`docs`, `av-system`, `studio`, etc.) para no exponerlas al cliente final.

## Sistema local activo
`av-system/` es la carpeta activa para el sistema Python local.

`studio/` queda como referencia legada y no debe tomarse como la fuente principal para nuevos cambios.

### Por que
- El sistema hoy guarda cambios en `av-system/data/businesses.json`.
- Tambien contempla subidas locales de archivos.
- Vercel es excelente para frontends estaticos y funciones serverless, pero esta capa necesita storage duradero para operar bien.

### Que haria falta para desplegarlo bien
- Mover contenido persistente a una base de datos o KV.
- Mover imagenes a Blob o storage equivalente.
- Reemplazar las escrituras locales del filesystem por llamadas a storage duradero.

## Ejecucion local del sistema
```powershell
cd av-system
python app.py
```

Tambien puedes usar desde la raiz:

```text
run-av-system.cmd
```

## Exportacion estatica desde el sistema
```powershell
cd av-system
python export_static.py
```

Tambien puedes usar desde la raiz:

```text
export-av-system.cmd
```
