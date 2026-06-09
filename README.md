# 🛡️ AccessGuard
### Zero Trust Access Intelligence Platform

AccessGuard es un SaaS multi-tenant de seguridad empresarial que permite a las organizaciones gestionar, auditar y certificar los accesos de sus empleados a recursos críticos, siguiendo principios Zero Trust y estándares como ISO 27001 y SOC2.

---

## 🚀 Demo en vivo
[accessguard.vercel.app](https://accessguard.vercel.app) *(disponible tras el deploy)*

## 📸 Capturas
> Dashboard · Empleados · Permisos · Shadow IT · AI Advisor

---

## ✨ Funcionalidades

- 🏢 **Multi-tenant** — cada empresa tiene sus datos completamente aislados
- 👥 **Gestión de empleados** — CRUD completo con scoring de riesgo
- 🗄️ **Gestión de recursos** — apps, carpetas y sistemas con niveles de sensibilidad
- 🔑 **Gestión de permisos** — asignación empleado↔recurso con niveles de acceso
- 🕵️ **Shadow IT Detector** — algoritmo automático que detecta accesos anómalos
- 🔄 **Recertificación de accesos** — campañas periódicas para aprobar/revocar permisos
- 📋 **Audit Log** — historial completo de actividad con timestamps
- 🤖 **AI Advisor** — chat inteligente con contexto real de la organización (Groq + LLaMA 3)
- 📊 **Dashboard** — métricas en tiempo real y gráficas de permisos por recurso

---

## 🛠️ Stack tecnológico

| Capa | Tecnología |
|---|---|
| Frontend | Next.js 14 · TypeScript · Tailwind CSS |
| Componentes UI | shadcn/ui |
| Gráficos | Recharts |
| Backend | Next.js API Routes |
| Base de datos | Supabase (PostgreSQL) |
| Autenticación | Supabase Auth |
| IA | Groq API · LLaMA 3.3 70B |
| Deploy | Vercel |

---

## 🗄️ Arquitectura

AccessGuard implementa una arquitectura **multi-tenant** donde cada organización tiene sus datos completamente aislados mediante Row Level Security (RLS) en Supabase. Todos los datos están vinculados a un `organization_id` y las políticas RLS garantizan que ninguna empresa pueda acceder a los datos de otra.

---

## ⚙️ Instalación local

```bash
# Clonar el repositorio
git clone https://github.com/SirAlex23/Accessguard.git
cd Accessguard

# Instalar dependencias
npm install

# Configurar variables de entorno
cp .env.example .env.local
# Edita .env.local con tus claves de Supabase y Groq

# Arrancar en desarrollo
npm run dev
```

---

## 🔐 Variables de entorno

```env
NEXT_PUBLIC_SUPABASE_URL=tu_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=tu_anon_key
SUPABASE_SECRET_KEY=tu_service_role_key
GROQ_API_KEY=tu_groq_api_key
```

---

## 👤 Autor

**Alejandro Crespo Correa**
Full Stack Developer · Valencia, Spain
[LinkedIn](https://linkedin.com/in/alejandro-crespo-574958388) · [GitHub](https://github.com/SirAlex23)

---

## 📄 Licencia

MIT