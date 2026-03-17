# CIMA Agent — Vercel Deploy

## Archivos
```
cima-vercel/
  api/claude.js        ← proxy seguro a Anthropic API
  public/index.html    ← pantalla de login
  public/app.html      ← agente completo
  vercel.json          ← configuracion de rutas
  package.json
```

## Deploy en Vercel (5 minutos)

### 1. Subir a GitHub
- Crea repo nuevo en github.com → nombre: `cima-agent-v2`
- Sube todos estos archivos

### 2. Conectar a Vercel
- Ve a vercel.com → New Project
- Importa el repo de GitHub
- Framework Preset: **Other**
- Click Deploy

### 3. Configurar variables de entorno
En Vercel → Settings → Environment Variables, añade:

| Variable | Valor |
|----------|-------|
| `ANTHROPIC_API_KEY` | tu key sk-ant-api03-... |
| `CIMA_PASSWORD` | la contraseña que quieras para el equipo |

### 4. Redeploy
Tras añadir las variables → Deployments → Redeploy

### URL final
`https://cima-agent-v2.vercel.app`

Comparte esa URL + la contraseña con el equipo fundador.

## Cambiar contraseña
Settings → Environment Variables → edita `CIMA_PASSWORD` → Redeploy

## Costes
- Vercel: 0€ (plan Hobby)
- Anthropic API: ~2-5€/mes con uso normal
