# Interfaz Móvil Control Pro

Aplicación web móvil de control financiero con tasas de cambio en tiempo real para Venezuela.

## Características

- ✅ Tasas de cambio en tiempo real (BCV, USDT P2P, EUR)
- ✅ Integración con APIs públicas (BCV Today, CriptoYa, DolarApi)
- ✅ Conversión automática a Bolívares (Bs)
- ✅ Interfaz móvil responsiva
- ✅ Dark mode nativo
- ✅ Sin hidratación de React
- ✅ Manejo robusto de errores

## Tecnologías

- Next.js 16.3.3
- React 19
- TypeScript
- Tailwind CSS 4.3.3
- shadcn/ui

## Despliegue en Netlify

### Opción 1: Desde Git (Recomendado)

1. Sube el código a un repositorio Git (GitHub, GitLab, Bitbucket)
2. Ve a [Netlify](https://app.netlify.com)
3. Clic en "Add new site" → "Import an existing project"
4. Conecta tu proveedor de Git
5. Selecciona el repositorio
6. Configura los ajustes de build:
   - **Build command**: `npm run build`
   - **Publish directory**: `.next`
   - **Node version**: `20`
7. Clic en "Deploy site"

### Opción 2: Desde CLI

```bash
# Instala Netlify CLI
npm install -g netlify-cli

# Login en Netlify
netlify login

# Inicializa el proyecto
netlify init

# Deploy a producción
netlify deploy --prod
```

### Opción 3: Drag & Drop

1. Ejecuta el build localmente:
   ```bash
   npm install
   npm run build
   ```

2. Ve a [Netlify](https://app.netlify.com)
3. Clic en "Add new site" → "Deploy manually"
4. Arrastra la carpeta `.next` a la zona de upload

## Configuración de Netlify

El archivo `netlify.toml` incluye:

- **Build command**: `npm run build`
- **Publish directory**: `.next`
- **Node version**: 20
- **Plugin**: `@netlify/plugin-nextjs` (automático)
- **Headers**: Seguridad y cacheo optimizado
- **Environment variables**: Configuradas automáticamente

## Variables de Entorno

No se requieren variables de entorno para esta aplicación.

## Scripts Disponibles

```bash
npm run dev      # Inicia servidor de desarrollo
npm run build    # Build de producción
npm run start    # Inicia servidor de producción
```

## APIs de Tasas de Cambio

La aplicación utiliza las siguientes APIs públicas:

- **BCV Today**: `https://bcv.today/api/v1/rate.json` (BCV y EUR)
- **CriptoYa**: `https://criptoya.com/api/binancep2p/USDT/VES/1` (USDT P2P)
- **DolarApi**: `https://ve.dolarapi.com/v1/dolares` (Fallback)

Todas son gratuitas y no requieren autenticación.

## Estructura del Proyecto

```
├── app/              # App Router de Next.js
├── components/       # Componentes React
│   ├── controlpro/   # Componentes de la app
│   └── ui/          # Componentes shadcn/ui
├── hooks/           # Custom hooks
├── lib/             # Utilidades y servicios
├── public/          # Archivos estáticos
└── netlify.toml     # Configuración de Netlify
```

## Soporte

Para problemas de despliegue, consulta la [documentación de Netlify](https://docs.netlify.com/).
