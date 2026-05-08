# recipeshare-qa
Testing manual sobre plataforma RecipeShare— JIRA + Zephyr | Técnicas ISTQB

# RecipeShare — QA Testing Project

> Proyecto de testing manual aplicando estándar ISTQB  
> sobre una plataforma web real de recetas.

**Sitio:** https://tusrecetas.lovable.app/  
**QA:** Enoc Isaac Ipanaque Rodas  
**Herramientas:** JIRA · Zephyr Essential · Técnicas ISTQB

---

## Contexto del Proyecto

Se recibieron las especificaciones del producto en un 
documento PDF con historias de usuario y criterios de 
aceptación. A partir de esas specs, se diseñaron los 
casos de prueba desde cero aplicando técnicas de caja 
negra del estándar ISTQB — sin guía previa de qué probar.

---

## Estructura del Repositorio

recipeshare-qa/
│
├── docs/
│   └── especificaciones.md       # HU y criterios de aceptación
│
├── test-plan/
│   └── plan-de-pruebas.md        # Plan del Sprint 1
│
├── test-cases/                   # TC por historia de usuario
│   ├── AUTH-01-registro.md
│   ├── AUTH-02-login.md
│   ├── AUTH-03-logout.md
│   ├── PROF-02-editar-perfil.md
│   ├── REC-01-crear-receta.md
│   ├── REC-02-ver-detalle.md
│   └── REC-03-editar-receta.md
│
├── bug-reports/                  # Defectos reportados
│   ├── BUG-001-registro-password.md
│   └── BUG-002-recordarme.md
│
└── reports/
└── informe-ejecucion-sprint1.md

---

## Cobertura Sprint 1 — Core del Sistema

| Historia | Épica | TC | Técnica ISTQB |
|---|---|---|---|
| AUTH-01 Registro | EP-A Autenticación | 7 | EP + BVA |
| AUTH-02 Login | EP-A Autenticación | 6 | Tabla de Decisión |
| AUTH-03 Logout | EP-A Autenticación | 3 | Exploratoria |
| PROF-02 Editar Perfil | EP-B Perfil | 9 | EP + BVA |
| REC-01 Crear Receta | EP-C Recetas | 12 | EP + BVA |
| REC-02 Ver Detalle | EP-C Recetas | 3 | Exploratoria |
| REC-03 Editar Receta | EP-C Recetas | 4 | Exploratoria |
| **Total** | | **44** | |

---

## Resultados de Ejecución

| Estado | Cantidad | Porcentaje |
|---|---|---|
| ✅ Passed | 35 | 79.5% |
| ❌ Failed | 8 | 18.2% |
| 🔵 Blocked | 1 | 2.3% |

---

## Bugs Reportados

| ID | Título | Severidad | Historia |
|---|---|---|---|
| [BUG-001](bug-reports/BUG-001-registro-password.md) | Registro permite password < 8 chars | Alta | AUTH-01 |
| [BUG-002](bug-reports/BUG-002-recordarme.md) | Recordarme no implementado | Alta | AUTH-02 |

---

## Criterio de Priorización

Se priorizó por riesgo: el core del sistema son 
autenticación y gestión de recetas. Sin esas 
funcionalidades el resto no tiene valor funcional. 
Las épicas restantes se cubren en Sprint 2.

---

## Próximo Paso — Automatización

- [ ] API Testing con **Rest Assured + Java**
- [ ] UI Testing con **Selenium + Cucumber (BDD)**
- [ ] Mock tests para TC con estado Failed

---

## Contacto

[LinkedIn](https://linkedin.com/in/enoc-isaac-ipanaque-rodas-b3729a283)
