# eva-frontend

Panel de control de **EVA OS** — un solo archivo `index.html`, HTML/CSS/JS vanilla, sin framework ni build step. Deploy en Vercel (auto-deploy desde GitHub).

Consume la API del backend [`eva-os`](https://github.com/flov35/eva-os). La URL del backend se configura desde el botón **⚙ API** del panel (se guarda en `localStorage`); por defecto apunta a `https://eva-os-production.up.railway.app`.

## Secciones

- **Dashboard** — stats generales y controles del orquestador (correr ciclo diario, Strategy Agent, Learning Agent, publicador, Classification Agent).
- **Content DB** — banco de piezas: subir contenido (individual o carrusel, incluyendo UGC patrocinado con datos de marca), filtrar, generar captions, eliminar.
- **Cola** — ver y quitar items de la cola de publicación, publicar lo vencido.
- **Publicaciones** — historial con métricas (likes, reach, saves, shares, engagement).
- **Alertas** — alertas pendientes para Flo, con botón de resolver.
- **Reglas** — reglas activas generadas por el Learning Agent.

## Desarrollo

No hay build step — abrir `index.html` directamente en el navegador, o servirlo con cualquier servidor estático:

```bash
npx serve .
```

## Deploy

Push a `main` dispara el auto-deploy en Vercel.
