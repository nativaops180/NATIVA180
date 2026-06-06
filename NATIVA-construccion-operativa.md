# NATIVA InOps — Construcción Operativa
**Documento vivo** · Actualizado diariamente · nativainops.com

---

## Visión del producto

NATIVA InOps es una plataforma de inteligencia de Customer Success impulsada por IA. Analiza señales de comportamiento, uso y comunicación de los clientes para entregar acciones concretas a los equipos de CS: quién va a cancelar, quién puede crecer, qué hacer hoy.

Opera en dos capas según la madurez del cliente:

---

## Capa 1 — Clientes sin CS propio

**Para quién:** Empresas que no tienen un departamento de Customer Success estructurado y necesitan construirlo desde cero con apoyo externo.

**Propuesta de valor:** NATIVA les da un sistema de CS operativo desde el día uno, sin necesidad de contratar equipo ni construir tecnología propia.

### Flujo operativo Capa 1

```
[Prospecto] 
    ↓ Ve la landing en nativainops.com
    ↓ Hace clic en el formulario (Tally)
[Formulario Tally]
    ↓ Captura: empresa, industria, tamaño, reto principal, herramientas actuales
    ↓ Envía datos automáticamente vía webhook
[Notion — Base de datos]
    ↓ Se crea registro en Companies Database
    ↓ Se llenan: Contacts, Interactions, Signals, Playbooks
[Make / n8n — Automatización]
    ↓ Detecta nuevo registro
    ↓ Envía datos a OpenAI para análisis inicial
[OpenAI — Motor de IA]
    ↓ Analiza señales del cliente
    ↓ Genera: diagnóstico, temperatura de cuenta, acciones recomendadas
[Mar — Human in the Loop]
    ↓ Revisa el output de IA
    ↓ Personaliza y valida
[Entrega al cliente]
    ↓ Blueprint de CS en PDF o Notion
    ↓ Dashboard en Notion o Looker Studio
```

### Stack Capa 1

| Herramienta | Rol | Notas |
|---|---|---|
| **Tally** | Formulario de captura | Link embebido en landing. El cliente no crea cuenta. |
| **Notion** | Base de datos y entrega | Companies DB, Contacts DB, Interactions DB, Signals DB, Playbooks DB |
| **Make / n8n** | Capa de automatización | Conecta Notion ↔ OpenAI. Dispara flujos por eventos. |
| **OpenAI** | Motor de análisis | Genera diagnósticos, clasifica señales, redacta playbooks |
| **Looker Studio** | Dashboard de métricas | Opcional en Fase 1. Se conecta a Notion como fuente. |
| **GitHub Pages** | Landing publicada | nativainops.com — repo: nativaops180/NATIVA180 |

---

## Capa 2 — Clientes con CS propio

**Para quién:** Empresas que ya tienen equipo de Customer Success, CRM activo y datos acumulados, pero no saben qué hacer con esa información ni cómo volverla accionable.

**Propuesta de valor:** NATIVA se conecta a sus herramientas existentes, analiza sus datos con IA y entrega inteligencia que su equipo no tendría capacidad de generar manualmente.

### Flujo operativo Capa 2

```
[Datos del cliente — fuentes existentes]
    HubSpot / Salesforce / Zendesk / WhatsApp Business / Intercom
    ↓ Conexión vía API o conector Make/n8n
[NATIVA — Motor de inteligencia]
    ↓ Ingesta de datos en tiempo real o batch
    ↓ Clasificación de cuentas por señales (comportamiento, uso, tickets, NPS)
    ↓ Modelos de predicción: churn, upsell, salud de cuenta
[Output de IA]
    ↓ "Esta cuenta está en rojo — acción recomendada: llamar hoy"
    ↓ "Esta cuenta está lista para upsell — trigger: renovación en 45 días"
    ↓ "Esta cuenta cancelará en ~60 días — señal: caída de uso del 40%"
[Equipo CS del cliente]
    ↓ Recibe alertas y prioridades en su dashboard
    ↓ Actúa sobre las recomendaciones
    ↓ Retroalimenta el sistema
```

### Stack Capa 2

| Herramienta | Rol |
|---|---|
| **HubSpot / Salesforce** | CRM fuente de datos del cliente |
| **Zendesk / Intercom** | Fuente de tickets y comunicaciones |
| **Make / n8n** | Orquestación de datos entre fuentes y motor NATIVA |
| **OpenAI / Claude** | Análisis de señales y generación de recomendaciones |
| **Dashboard propio** | Entrega de inteligencia al equipo CS del cliente |

---

## Agentes de IA (en construcción)

NATIVA opera con una arquitectura de agentes especializados. Cada agente tiene un rol acotado y trabaja en conjunto.

| Agente | Función | Estado |
|---|---|---|
| **Agente de diagnóstico** | Analiza el formulario inicial y genera el blueprint del cliente | Por definir |
| **Agente de señales** | Monitorea el comportamiento de las cuentas y detecta cambios | Por definir |
| **Agente de playbooks** | Genera las acciones recomendadas según el segmento y señal | Por definir |
| **Agente de QBR** | Redacta reportes de revisión trimestral para el equipo CS | Por definir |
| **Agente de onboarding** | Guía al cliente nuevo durante su primer mes | Por definir |

---

## Modelo de pricing

*Por definir — pendiente sesión dedicada.*

---

## ICP (Ideal Customer Profile)

*Por definir — pendiente sesión dedicada.*

Señales tempranas observadas:
- Empresas buscando activamente "construir inteligencia de CS internamente" (señal de mercado observada por Mar)
- Empresas con CRM activo pero sin capacidad analítica
- Startups B2B en etapa de escala que necesitan retener clientes

---

## Flujo de ventas

*Por definir — pendiente sesión dedicada.*

---

## Métricas clave

*Por definir — pendiente sesión dedicada.*

---

## Infraestructura y dominio

| Elemento | Detalle |
|---|---|
| **Dominio** | nativainops.com |
| **Hosting landing** | GitHub Pages |
| **Repositorio** | github.com/nativaops180/NATIVA180 |
| **Email profesional** | Pendiente — Google Workspace Starter (~$6 USD/mes) recomendado |
| **Backend Fase 1** | Notion (base de datos principal) |
| **Backend Fase 2+** | Por definir según escala |

---

*Última actualización: 2026-06-05*
*Próxima pregunta diaria: mañana a las 10:00 am*
