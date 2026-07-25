<img width="1200" height="720" alt="GoogleAntigravity" src="https://github.com/user-attachments/assets/d5d5949f-dabf-4430-8eb6-6b9c48698ddb" />


# Google Antigravity Full-stack Hub

¡Hola y bienvenido al entorno de desarrollo que desafía la gravedad del código! Inspirado en el clásico huevo de pascua de Google, este repositorio es una suite unificada que rompe las barreras tradicionales entre el Frontend, Backend y DevOps. 
Aquí consolido las herramientas esenciales que todo desarrollador Full Stack necesita para evitar que sus proyectos "caigan" ante la frustración, el desorden o la falta de optimización.

## La Suite Antigravedad (Herramientas Esenciales)
Para mantener un ecosistema flotante, fluido y sin fricciones, unificamos el poder de las siguientes tecnologías:

### 1. Frontend Estelar (Capa superficical de Presentación)
* **Framework Principal:** React.js / Next.js para un renderizado veloz que flota sobre el cliente.
* **Estilos Dinámicos:** Tailwind CSS para interfaces responsivas construidas a la velocidad de la luz.
* **Gestión de Estado:** Zustand o Redux Toolkit para mantener los datos alineados sin importar la gravedad del sistema.

### 2. Backend Orbitall (Capa interna de lógica)
* **Entorno de Ejecución:** Node.js con TypeScript para un tipado estricto que evita colisiones catastróficas.
* **Framework de API:** FastAPI o Express.js para rutas de datos aerodinámicas y de alta velocidad.
* **Seguridad:** JWT (JSON Web Tokens) y Helmet para proteger la órbita de accesos no autorizados.

# Google AntiGravity Full-Stack Hub

Este repositorio es una arquitectura de referencia avanzada para la gestión de proyectos Monorrepo Full Stack de nivel empresarial. Inspirado en el concepto conceptual de Google AntiGravity, el objetivo de este ecosistema es unificar las herramientas esenciales del desarrollo de software moderno en un entorno optimizado, minimizando la fricción de configuración, garantizando el tipado estricto de extremo a extremo y automatizando los procesos de integración y despliegue continuo.

---

## Arquitectura del Sistema y Flujo de Datos

El proyecto implementa una topología desacoplada gestionada centralizadamente mediante Turborepo. El núcleo del Backend adopta los principios de Arquitectura Limpia (Clean Architecture) y Desarrollo Guiado por el Dominio (Domain-Driven Design) para aislar rigurosamente la lógica de negocio de los detalles de la infraestructura.

### Diagrama de Interacción de Componentes

    graph TD
    Client [Cliente Web / Next.js SSR] -->|HTTPS / WSS| Gateway[Nginx Reverse Proxy / Cloudflare]
    Gateway -->|Enrutamiento de API| API[API Gateway / NestJS Core Engine]"
    
    subgraph "Backend Core (TypeScript)"
        API -->|Controllers| UseCases[Capa de Casos de Negocio / Domain]
        UseCases -->|Entities & Mappers| Infra[Infraestructura / Repositorios]
    end
    
    Infra -->|Read/Write Split| DB[(PostgreSQL Cluster)]
    Infra -->|Caching & Rate Limiting| Redis[(Redis Cluster)]
    UseCases -->|Publish Events| Broker[RabbitMQ / Event Bus]
    
    Broker -->|Asynchronous Workers| Worker[Background Jobs / Node-Worker]


---

## Ecosistema Tecnológico Unificado

### 1. Capa de Presentación (Frontend)
* **Framework Principal:** *Next.js 15 (App Router) optimizado con React Server Components (RSC) para la reducción del tamaño del paquete en el lado del cliente y una renderización inicial óptima.*
* **Interfaz de Usuario y Estilos:** *Tailwind CSS v4 complementado con Shadcn/ui (basado en primitivos de Radix UI) para garantizar accesibilidad bajo el estándar WAI-ARIA.*
* **Gestión de Estado:** *Zustand para la manipulación de estados globales efímeros en memoria, asistido por Immer para mutaciones seguras de estructuras complejas.*
* **Sincronización de Datos:** *TanStack Query v5 (React Query) para la gestión avanzada de caché, revalidación asíncrona en segundo plano y actualizaciones optimistas.*
* **Validación de Formularios:** *React Hook Form integrado con esquemas de validación estricta en tiempo de ejecución mediante Zod.*

### 2. Capa de Lógica de Negocio (Backend)
* **Entorno de Ejecución:** *Node.js (v22 LTS) operando de forma nativa con TypeScript 5.x bajo configuraciones de tipado estrictas.*
* **Framework de API:** *NestJS para asegurar modularidad, inyección de dependencias y un desacoplamiento efectivo entre componentes de la aplicación.*
* **Capa de Persistencia y ORM:** *Prisma ORM o Drizzle ORM como abstracción de datos con generación automatizada de tipos estáticos en tiempo de compilación.*
* **Mensajería Asíncrona:** *RabbitMQ para la gestión de arquitecturas orientadas a eventos (EDA) y la distribución de tareas pesadas en segundo plano.*

### 3. Persistencia de Datos y Caché
* **Base de Datos Relacional:** PostgreSQL 16 configurado con un pool de conexiones optimizado a través de PgBouncer para soportar alta concurrencia.
* **Memoria Caché y Mensajería Rápida:** Redis Stack para la persistencia de sesiones de usuario, almacenamiento en caché de respuestas HTTP y políticas globales de Rate Limiting.

### 4. Infraestructura y DevOps
* **Contenedores:** Docker y Docker Compose con configuraciones multi-etapa (multi-stage builds) para la optimización y reducción de peso de las imágenes de producción.
* **Integración y Despliegue Continuo (CI/CD):** GitHub Actions encargado de la ejecución automática de pruebas unitarias, análisis estático de código y escaneo de vulnerabilidades.
* **Calidad de Código:** Implementación obligatoria de ESLint, Prettier y Husky para el bloqueo automatizado de confirmaciones (commits) que no cumplan con los estándares definidos.

---

## Estándares de Seguridad Implementados

Para mitigar riesgos informáticos comunes, el sistema incorpora las siguientes directrices de seguridad de forma nativa:

* **Protección de Cabeceras:** Helmet.js configurado para inyectar políticas como Content Security Policy (CSP), X-Content-Type-Options y Strict-Transport-Security (HSTS).
* **Autenticación Stateless:** Flujo de tokens gestionado por JSON Web Tokens (JWT) mediante firmas asimétricas (RS256). Los tokens de acceso se almacenan exclusivamente en memoria, mientras que los tokens de refresco viajan mediante Cookies con directivas HttpOnly, Secure y SameSite=Strict.
* **Mitigación de Ataques de Denegación de Servicio (DDoS):** Limitación de tasa de peticiones parametrizada dinámicamente en la capa de Redis.
* **Prevención de Inyecciones:** Sanitización activa de payloads entrantes y uso estricto de consultas parametrizadas a través del ORM para evitar inyecciones SQL.

---

## Estructura de Directorios del Monorrepo

La distribución del código está diseñada bajo la premisa DRY (Don't Repeat Yourself), organizando las aplicaciones y las librerías compartidas de forma quirúrgica:

```text
google-antigravity-stack/
├── .github/                      # Automatización y Gobernanza del repositorio
│   ├── workflows/
│   │   ├── frontend-ci.yml       # Integración continua de la aplicación Next.js
│   │   ├── backend-ci.yml        # Integración continua del servidor NestJS
│   │   └── security-audit.yml    # Escaneo automatizado de vulnerabilidades
│   └── pull_request_template.md  # Plantilla para la revisión de código
├── apps/                         # Aplicaciones independientes
│   ├── frontend/                 # Aplicación de Cliente
│   │   ├── src/
│   │   │   ├── app/              # Enrutamiento basado en archivos
│   │   │   ├── components/       # Componentes atómicos de la interfaz
│   │   │   ├── hooks/            # Custom hooks y lógica de React Query
│   │   │   └── store/            # Almacenes de estado Zustand
│   │   ├── Dockerfile.dev
│   │   └── Dockerfile.prod
│   └── backend/                  # API Core
│       ├── src/
│       │   ├── modules/          # Encapsulamiento por dominios de negocio
│       │   ├── common/           # Filtros, guards e interceptores globales
│       │   └── main.ts           # Punto de entrada de la API
│       ├── prisma/               # Esquemas y migraciones de base de datos
│       └── Dockerfile.prod
├── packages/                     # Librerías internas y configuraciones compartidas
│   ├── ts-config/                # Base de configuración TypeScript
│   ├── eslint-config/            # Reglas de análisis estático unificadas
│   ├── ui-core/                  # Sistema de diseño y componentes comunes
│   └── database-types/           # Tipados estáticos derivados de la base de datos
├── docker-compose.yml            # Orquestación de infraestructura local
├── turbo.json                    # Canalizaciones de tareas y caché de Turborepo
└── package.json                  # Raíz del espacio de trabajo (Workspace)
```

---

## Instrucciones de Instalación y Despliegue Local

### Requisitos Previos
Es indispensable contar con las siguientes herramientas instaladas en el sistema anfitrión:
* Node.js v22 LTS o superior.
* pnpm v9 o superior (gestor obligatorio para la correcta resolución de dependencias del monorrepo).
* Docker Desktop o Docker Engine v2.20 o superior.

### 1. Clonación del Repositorio
```bash
git clone https://github.com
cd google-antigravity-stack
```

### 2. Instalación de Dependencias
La instalación debe realizarse exclusivamente desde la raíz del monorrepo:
```bash
pnpm install
```

### 3. Configuración de Variables de Entorno
Duplique los archivos de plantilla provistos en sus respectivas rutas:
```bash
cp apps/frontend/.env.example apps/frontend/.env.local
cp apps/backend/.env.example apps/backend/.env
```

### 4. Orquestación de la Infraestructura
Levante los contenedores correspondientes a PostgreSQL, Redis y RabbitMQ en segundo plano:
```bash
docker-compose up -d
```

### 5. Ejecución de Migraciones de Base de Datos
Sincronice el esquema local de la base de datos y genere el cliente de tipos estáticos:
```bash
pnpm --filter backend prisma migrate dev
```

### 6. Inicialización del Entorno de Desarrollo
Inicie el ciclo de ejecución en paralelo para todas las aplicaciones del espacio de trabajo:
```bash
pnpm dev
```
* Acceso al Frontend: http://localhost:3000
* Acceso al API Gateway: http://localhost:8080
* Documentación de la API (Swagger): http://localhost:8080/api/docs

---

## Verificación de Calidad y Suite de Pruebas

El repositorio implementa restricciones automatizadas mediante Git Hooks (Husky). No se permite la consolidación de código que rompa las reglas del linter o falle en las pruebas unitarias.

```bash
# Análisis estático y formateo de sintaxis en todo el monorrepo
pnpm lint

# Ejecución de pruebas unitarias e integrales
pnpm test

# Ejecución de pruebas con reporte detallado de cobertura
pnpm test:coverage

# Compilación de artefactos para validación de tipado en TypeScript
pnpm build
```

---

## Convención de Commits y Modelo de Ramas

Para garantizar la legibilidad del historial y posibilitar la generación automatizada de bitácoras de cambios (Changelogs), este proyecto adopta estrictamente la especificación de Conventional Commits:

* `feat(modulo):` Incorporación de una nueva funcionalidad para el usuario final.


