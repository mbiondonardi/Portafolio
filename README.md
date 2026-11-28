# Portafolio de Proyectos · Martín Biondo Nardi

Estudiante avanzado de **Ingeniería en Sistemas de Información (UTN FRC)** con foco en **Desarrollo Full Stack**, **Arquitectura Backend / Microservicios** e **Inteligencia Artificial Aplicada (RAG y Agentes)**.

Este repositorio reúne mis proyectos principales en un único índice de acceso rápido. Cada proyecto cuenta con su propio repositorio limpio, documentación técnica e instrucciones de ejecución local.

---

## 🛠️ Stack Tecnológico

- **Backend & Arquitectura:** Java 21 (Spring Boot, Spring Cloud Gateway, Resilience4j), Python (FastAPI, Tkinter, Pytest), Node.js (Express, Sequelize), PostgreSQL, MySQL, SQLite, Keycloak (OAuth2/OIDC), Docker & Docker Compose, OpenAPI / Swagger
- **Frontend & 3D:** React (18/19), Vite, Tailwind CSS, Bootstrap, Zustand, Three.js, Web Audio API, Streamlit
- **IA Generativa & Datos:** LangChain, LangGraph (`StateGraph`, `langgraph-supervisor`), Google Gemini API, ChromaDB, HuggingFace Embeddings, RAG híbrido, Pydantic, Pandas, Altair
- **Buenas Prácticas:** Arquitectura en capas, Microservicios, Patrones de Diseño (DAO, Singleton, Factory Method, Observer, State), Testing automatizado, Accesibilidad Web (WCAG AA)

---

## 🚀 Proyectos Destacados

### 1. Desarrollo Web & Full Stack

#### [Ugoke Kinesiología · Demo Local + Plan de Capacitación](https://github.com/mbiondonardi/ugoke-kinesiologia-demo)
Versión demostrativa ejecutable localmente (con datos 100 % ficticios y modo mock de integraciones externas) de la plataforma web full-stack de gestión para clínicas de kinesiología, integrando además el portal interactivo de capacitación para pacientes.
- **Destacado:** Roles diferenciados (Kinesiólogo / Paciente), autenticación JWT + cifrado AES-256, agenda por sucursales, gestión clínica, planificaciones multi-día con exportación a PDF/QR y seed automático listo para probar en dos comandos.
- **Stack:** `React 19` · `Vite` · `Zustand` · `Node.js` · `Express 5` · `Sequelize` · `SQLite / MySQL` · `JWT`

#### [Ugoke · Portal de Capacitación para Pacientes](https://github.com/mbiondonardi/ugoke-training-portal)
Portal web interactivo y accesible diseñado bajo criterios **WCAG AA** para capacitar a pacientes adultos y adultos mayores en el uso autónomo de su plataforma de rehabilitación domiciliaria.
- **Destacado:** 4 módulos guiados, simulador clínico de 9 casos, audio-guías (podcasts + Web Speech API), **modo dislexia (`OpenDyslexic`)**, alto contraste, escalado tipográfico, navegación completa por teclado y panel analítico de seguimiento (`#/reportes`) con exportación a CSV.
- **Stack:** `React 18` · `Vite 6` · `Tailwind CSS` · `Web Speech API` · `Node.js`

---

### 2. Backend, Microservicios & Arquitectura de Software

#### [Sistema de Logística de Contenedores · Microservicios](https://github.com/mbiondonardi/logistics-microservices-spring)
Plataforma backend distribuida para gestión integral de transporte terrestre de contenedores: clientes, tarifas, flota, depósitos, cotización de múltiples rutas alternativas y seguimiento de tramos.
- **Destacado:** API Gateway + 3 microservicios (`ms-clientes-tarifas`, `ms-flota-depositos`, `ms-solicitudes-rutas`), seguridad OAuth2/OIDC con **Keycloak 26** y Service Accounts, **Circuit Breakers (Resilience4j)**, cálculo de rutas alternativas con **OSRM** y depósitos intermedios (con fallback Haversine), Swagger UI agregado y despliegue completo vía Docker Compose.
- **Stack:** `Java 21` · `Spring Boot 3.3` · `Spring Cloud Gateway` · `Keycloak 26` · `PostgreSQL 16` · `OSRM` · `Docker Compose` · `OpenAPI 3`

#### [Sistema Integrado de Ventas, Logística e Inventario + Analítica Gerencial](https://github.com/mbiondonardi/retail-inventory-pos-python)
Aplicación de escritorio de gestión comercial y logística para una red minorista (Centro de Distribución + 5 sucursales) con arquitectura en capas, patrones de diseño y módulo completo de Business Intelligence gerencial.
- **Destacado:** Segregación de stock en 4 estados, trazabilidad logística con máquina de estados y triggers SQLite, POS polimórfico, base histórica precargada de **9 meses / 3 trimestres**, **5 Reportes Gerenciales** (benchmarking, tendencias MoM/QoQ, Pareto ABC, Fill Rate / Lead Time P90, rotación y DOH) + **5 Informes Operativos** exportables a **Excel (`.xlsx`), PDF y CSV**, respaldado por **195 pruebas automatizadas**.
- **Stack:** `Python` · `Tkinter / ttk` · `SQLite (3FN)` · `OpenPyXL` · `PyMuPDF` · `Pytest`

---

### 3. Inteligencia Artificial & Agentes

#### [LangChain & LangGraph Agents Portfolio](https://github.com/mbiondonardi/langchain-langgraph-agents)
Colección de **5 aplicaciones completas de IA Generativa y Agentes** que abarcan desde salidas estructuradas hasta sistemas RAG híbridos, memoria persistente y arquitecturas multiagente:
1. **SOC Multi-Agent System:** supervisor en LangGraph coordinando 3 agentes ReAct (`alert_analyzer`, `threat_analyzer`, `notification_agent`) integrados con VirusTotal, Tavily y Gmail + servidor webhook FastAPI y dashboard Streamlit.
2. **Helpdesk 2.0 (LangGraph):** `StateGraph` con RAG, puntuación de confianza, checkpointing en SQLite y flujo *Human-in-the-Loop* (`interrupt_before`).
3. **Multi-User Memory Chat:** chatbot con perfiles y memoria dual (historial en SQLite + memoria semántica transversal en ChromaDB).
4. **Legal RAG Assistant:** asistente sobre contratos PDF con `MultiQueryRetriever`, MMR y `EnsembleRetriever` híbrido.
5. **CV Analyzer:** evaluación estructurada con Pydantic y exportación de reportes en JSON y PDF.
- **Stack:** `Python` · `LangChain` · `LangGraph` · `Google Gemini` · `ChromaDB` · `HuggingFace Embeddings` · `FastAPI` · `Streamlit` · `Pydantic`

---

### 4. Entornos 3D & Simulación

#### [Operación Juguetes · Juego 3D en Primera Persona](https://github.com/mbiondonardi/operacion-juguetes-3d)
Videojuego 3D de sigilo en primera persona para navegador con estética cartoon y arquitectura modular sin frameworks externos.
- **Destacado:** Casa explorable de 5 niveles con múltiples rutas de infiltración, IA de enemigos con máquina de estados, visión/audición y pathfinding BFS, ciclo Día/Noche con cortes de luz, audio espacial 3D y música adaptativa con **Web Audio API**, niveles de dificultad y persistencia de récords.
- **Stack:** `JavaScript (ES Modules)` · `Three.js` · `Web Audio API` · `Vite`

#### [Simulador de Colas · i-Fix](https://github.com/mbiondonardi/ifix-queue-simulator)
Simulador interactivo de eventos discretos que modela un taller de servicio técnico bajo un esquema de **colas con prioridad e interrupción (*preemptive-resume*)** y política de cierre diario.
- **Destacado:** Parámetros estadísticos configurables (distribuciones exponencial, uniforme y Bernoulli), vector de estado evento por evento con trazabilidad de números aleatorios, KPIs operativos y gráficos interactivos.
- **Stack:** `Python` · `Streamlit` · `Pandas` · `Altair`

---

## 📋 Resumen Rápido

| Proyecto | Área | Tecnologías principales | Repositorio |
| :--- | :--- | :--- | :--- |
| **Ugoke Kinesiología Demo** | Full Stack | React 19, Node.js, Express, Sequelize, SQLite | [Ver código](https://github.com/mbiondonardi/ugoke-kinesiologia-demo) |
| **Ugoke Training Portal** | Frontend / Accesibilidad | React 18, Vite, Tailwind CSS, WCAG AA | [Ver código](https://github.com/mbiondonardi/ugoke-training-portal) |
| **Logistics Microservices** | Backend / Distribuido | Java 21, Spring Boot, Gateway, Keycloak, Docker | [Ver código](https://github.com/mbiondonardi/logistics-microservices-spring) |
| **Retail Inventory & POS** | Software / BI | Python, Tkinter, SQLite, OpenPyXL, Pytest | [Ver código](https://github.com/mbiondonardi/retail-inventory-pos-python) |
| **LangChain & LangGraph Agents** | IA Generativa / Agentes | Python, LangGraph, Gemini, ChromaDB, FastAPI | [Ver código](https://github.com/mbiondonardi/langchain-langgraph-agents) |
| **Operación Juguetes 3D** | 3D / GameDev | JavaScript, Three.js, Web Audio API, Vite | [Ver código](https://github.com/mbiondonardi/operacion-juguetes-3d) |
| **Simulador de Colas i-Fix** | Simulación / Datos | Python, Streamlit, Pandas, Altair | [Ver código](https://github.com/mbiondonardi/ifix-queue-simulator) |

---

## 📫 Contacto

- **GitHub:** [@mbiondonardi](https://github.com/mbiondonardi)
- **Email:** [martinbiondonardi@gmail.com](mailto:martinbiondonardi@gmail.com)
