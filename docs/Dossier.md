<div align="center">

![Logo Voz de Cristal](../../Voz de Cristal - WEB/public/assets/img/logoVC.png)

# **Dossier Técnico y Estratégico**
## Proyecto Voz de Cristal

**Versión:** Oficial
**Fecha:** Enero 2026

---

### **Confidencialidad y Uso Estratégico**
Este documento contiene información técnica, estratégica y social de uso reservado. Su difusión debe realizarse únicamente en contextos institucionales, bajo la supervisión de los Impulsores.

---

</div>

# Índice
1. [Resumen Ejecutivo](#documento-00-resumen-ejecutivo)
2. [Marco Conceptual](#documento-01-marco-conceptual)
3. [Especificación Técnica](#documento-02-especificación-técnica-de-arquitectura)
4. [Protocolo Social](#documento-03-protocolo-de-gestión-social)
5. [Métricas y Viabilidad](#documento-04-informe-preliminar-de-métricas-y-viabilidad)
6. [Carta de Intención](#documento-05-carta-abierta-de-intención)
7. [Ficha de Componentes](#documento-06-ficha-técnica-de-componentes-propuesta-mvp)
8. [Arquitectura Lógica](#documento-07-arquitectura-lógica-y-flujo-de-datos)
9. [Análisis FODA](#documento-08-análisis-foda-estratégico)
10. [Compendio de Fuentes](#documento-09-compendio-de-referencias-y-fuentes)

---

<!-- Resumen Ejecutivo -->

<div align="justify">

# DOCUMENTO 00: RESUMEN EJECUTIVO

**Impulsores:**
- Yaneth Villegas – Impulsora
- Héctor Águila – Impulsor

**Génesis del Proyecto (La Verdad)**
Voz de Cristal no nace de una estadística, sino de dos cicatrices. Nace de nosotros, unos tíos que vieron cómo el sistema falló. Vimos cómo los protocolos de "protección" llegaban tarde, cuando el daño en nuestros sobrinos ya estaba hecho. Entendimos a la fuerza que, a puertas cerradas, los niños están solos. Y nos prometimos que, si el sistema es sordo y ciego, nosotros construiríamos los oídos y los ojos que faltan.

## Problema
En Chile y el mundo, existen brechas de seguridad críticas. La realidad es dolorosa: muchas veces, la vulnerabilidad de niños, niñas y adolescentes no proviene de extraños, sino de sus propios entornos de confianza, e incluso de quienes deberían protegerlos. El sistema actual es ciego ante lo que ocurre a puertas cerradas.

## Solución Propuesta (Caballo de Troya)
Voz de Cristal es un dispositivo "silencioso por defecto" camuflado como accesorio escolar.
- **Públicamente:** Es una herramienta de "Autonomía y Seguridad Escolar" (lateralidad, evitar extravíos). esta narrativa permite su entrada en los colegios y hogares sin resistencia.
- **Realmente:** Es un sistema de detección temprana de vulneración que utiliza TinyML para identificar patrones físicos de riesgo (taquicardia + fuerza G) y activar una alerta con evidencia forense encriptada.

## Invitación
El proyecto está abierto a la colaboración de instituciones, empresas, municipios, académicos y profesionales de todas las áreas. No se busca financiamiento directo ni créditos personales, sino sumar capacidades para llevar esta solución a quienes más la necesitan.

</div>

---

<!-- Marco Conceptual -->

<div align="justify">

# DOCUMENTO 01: MARCO CONCEPTUAL

**Impulsores:** Yaneth Villegas y Héctor Aguila

## 1. El Significado: Voz de Cristal

### Transparencia y Seguridad Integral
Representa la claridad de los datos y la pureza de la infancia que queremos proteger. La narrativa pública es de seguridad y autonomía, mientras que la misión real es proteger a quienes no pueden defenderse.

### Fragilidad Resiliente
La infancia es un cristal que parece romperse, pero bajo este sistema, ese "estallido" se convierte en una alerta sónica y digital imposible de ignorar. El dispositivo se camufla como accesorio escolar para evitar estigmatización y proteger la discreción.

## 2. La Misión Real

El proyecto aborda la **"Seguridad por Omisión"**: la protección de los niños en entornos donde la supervisión humana falla o no existe.

> **Estrategia Caballo de Troya:** Voz de Cristal se presenta públicamente como herramienta de autonomía y seguridad escolar, pero en este dossier técnico aclaramos su función real como sistema de detección temprana de vulneración mediante IA ética.

</div>

---

<!-- Especificación Técnica -->

<div align="justify">

# DOCUMENTO 02: ARQUITECTURA TÉCNICA PROPUESTA

**Impulsores:** Yaneth Villegas y Héctor Aguila

## 1. Hardware (The Edge)

### Microcontrolador & Comunicación
**Propuesta:** SoC con soporte NB-IoT/LTE-M (ej. Simcom o Quectel).
- **Justificación:** Transmisión "Deep Coverage" (sótanos/interiores) y alta eficiencia energética.
- **Camuflaje:** Integrado en pulsera escolar o bijouterie para pasar desapercibido.

### Sensores de Gatillo (Trigger)
- **Acelerómetro:** Detecta impactos, caídas o zarandeos violentos.
- **Sensor PPG:** Monitoreo de picos de frecuencia cardíaca (estrés agudo/miedo).

### TinyML (IA en el borde)
El dispositivo no transmite todo el tiempo. Un algoritmo local procesa los datos de los sensores y SOLO activa la alerta si detecta la coincidencia de patrones de riesgo (Golpe + Taquicardia).

## 2. Seguridad y Privacidad
- **Encriptación:** AES-256 para toda la data.
- **Sin Streaming:** No se transmite audio ni video constante. Solo evidencias puntuales bajo alerta confirmada.

</div>

---

<!-- Protocolo Social -->

<div align="justify">

# DOCUMENTO 03: PROTOCOLO DE GESTIÓN SOCIAL

**Impulsores:** Yaneth Villegas y Héctor Aguila

## 1. Protocolo de Seguridad y Discreción

El sistema **no envía alertas al teléfono de los padres por defecto** si existe una denuncia previa o si se configura el "Modo Riesgo Intrafamiliar". Esta medida responde a la realidad de que la mayoría de los riesgos ocurren en el entorno familiar o escolar. La alerta se dirige a:
*   Central de Emergencias Policiales.
*   Red de Apoyo Validada (Educadores/Familiares externos).

## 2. Diseño Centrado en el Niño

El rol social garantiza que el hardware **no sea estigmatizante**. El dispositivo se presenta como accesorio escolar (pulsera de lateralidad o bijouterie educativa).
- **Objetivo:** Evitar que el agresor o entorno sospeche de la presencia de tecnología de rastreo o alerta.

> **Estrategia Caballo de Troya:** La narrativa pública es de seguridad y autonomía escolar, mientras que la función real del sistema es la protección integral y la detección temprana de riesgos.

</div>

---

<!-- Métricas -->

<div align="justify">

# DOCUMENTO 04: INFORME PRELIMINAR DE MÉTRICAS Y VIABILIDAD

**Impulsores:** Yaneth Villegas y Héctor Aguila

> **Nota:** Este informe se basa en proyecciones de mercado (2024-2025) y referencias técnicas industriales. Las cifras definitivas se ajustarán en la etapa de prototipado.

## 1. Validación Social y Necesidad
- **Percepción de Seguridad:** Existe un consenso en la comunidad sobre la utilidad de incorporar tecnología asistencial en los útiles escolares.
- **Brechas de Supervisión:** La evidencia institucional apunta a la urgencia de herramientas que acompañen a los niños cuando la supervisión directa no es posible.

## 2. Viabilidad Económica (Proyección)
- **Hardware:** Estimaciones basadas en componentes industriales estándar (NB-IoT/LTE-M) disponibles en proveedores globales (LCSC/Alibaba), optimizados para volumen.
- **Modelo Institucional:** La entrega como "kit escolar" facilita la economía de escala.

## 3. Rentabilidad Social y Ahorro Estatal
Si bien no podemos evitar el primer acto de vulneración, Voz de Cristal permite **detener la cronicidad** del abuso.
- **Costo de Reparación:** Un niño vulnerado crónicamente implica un gasto estatal enorme (juicios, terapias de por vida).
- **Costo de Prevención:** La detección temprana corta el ciclo de abuso. *Invertir en detección es infinitamente más barato que financiar décadas de reparación.*

</div>

---

<!-- Carta de Intención -->

<div align="justify">

# DOCUMENTO 05: CARTA ABIERTA DE INTENCIÓN

**A quien corresponda:**

Por medio de la presente, los impulsores del proyecto **Voz de Cristal**, Yaneth y Héctor, extienden una invitación abierta a cualquier institución, autoridad, empresa o profesional que desee sumarse a la misión de **proteger a la infancia de la vulneración silenciosa, utilizando la seguridad escolar como vehículo estratégico.**

Esta iniciativa nace de una motivación personal y social profunda. No buscamos créditos personales, fama ni beneficios económicos. Nuestro único objetivo es entregar una base fundacional robusta para que esta solución exista.

**Nuestra Postura:**
Si se nos permite liderar o acompañar este proceso, nos sentiríamos profundamente honrados. Pero si nuestro rol debe limitarse a entregar la idea para que otros con más recursos la lleven a cabo, lo aceptamos con humildad. **Nos conformamos con saber que esta opción de salvar vidas existe y está operativa, sin importar quién se lleve el crédito.**

En esta etapa, no solicitamos financiamiento, sino la apertura de redes técnicas, sociales y legales para validar y fortalecer esta arquitectura.

**Firmado:**
*   **Yaneth Villegas** - Impulsora
*   **Héctor Águila** - Impulsor

</div>

---

<!-- Componentes -->

<div align="justify">

# DOCUMENTO 06: FICHA TÉCNICA DE COMPONENTES (PROPUESTA MVP)

**Impulsores:** Yaneth Villegas y Héctor Aguila

> **Nota:** Esta selección de componentes es una propuesta teórica asistida por inteligencia artificial para validar viabilidad.

## 1. Unidad de Procesamiento
*   **Módulo NB-IoT:** Ej. SIM7080G. Para cobertura profunda y bajo consumo.
*   **MCU:** ESP32-S3 o nRF52840 (TinyML capaz).

## 2. Sensores
*   **Acelerómetro:** Detección de caídas/forcejeos.
*   **PPG:** Ritmo cardíaco.

## 3. Interfaz y Alerta
*   **Antena FPC:** Integrada.
*   **Micrófono MEMS:** Activación exclusiva por evento crítico.
    > **Nota de Privacidad:** El micrófono NO es para escucha activa. Se activa **solo durante la emergencia** (alerta confirmada) para capturar "ráfagas de audio" de evidencia (15s).

</div>

---

<!-- Arquitectura Lógica -->

<div align="justify">

# DOCUMENTO 07: ARQUITECTURA LÓGICA Y FLUJO DE DATOS

**Impulsores:** Yaneth Villegas y Héctor Aguila

## 1. Visión General: "La Tubería Segura"
El dispositivo funciona como un "submarino" que solo emerge (transmite) bajo condiciones de riesgo.

## 2. Definición del Edge
- **Estado Normal (Heartbeat):** Ping de "estoy vivo" cada 60-120 min.
- **Estado de Alerta (Panic Mode):** $$ Trigger = (HR > Umbral) + (GForce > Umbral) $$
    - **Acción:** Despierta micrófono, captura 15s de audio ambiente, encripta y envía asíncronamente.

## 3. Rol Telco
- **APN Privado:** Sin acceso a internet público (Google/Facebook bloqueados).
- **IMEI Whitelisting:** Solo dispositivos registrados.

## 4. Privacidad de Datos
| Tipo de Dato          | Encriptación          | Acceso                               |
| :-------------------- | :-------------------- | :----------------------------------- |
| **Identidad**         | SHA-256               | Orden Judicial                       |
| **Evidencia (Audio)** | AES-256 (Llave Doble) | Custodia Digital (Fiscal + Servidor) |

</div>

---

<!-- FODA -->

<div align="justify">

# DOCUMENTO 08: ANÁLISIS FODA (ESTRATÉGICO)

**Impulsores:** Yaneth Villegas y Héctor Aguila

## Fortalezas
- **Estrategia Caballo de Troya:** Narrativa de seguridad escolar que protege la función de detección.
- **Base ética genuina:** Motivada por experiencias reales ("Génesis").
- **Arquitectura "Silenciosa por Defecto":** Privacidad total.
- **Desapego del Ego:** Documentación lista para ser transferida.

## Debilidades (Llamado a la Acción)
- **Recursos:** Falta capital para prototipado masivo.
- **Legal:** Se requiere validar el protocolo de evidencia de audio.

## Amenazas
- **Exposición Mediática Sensacionalista:** Prensa que "destape" el secreto y alerte a los agresores.
- **Replicación No Ética:** Copias del dispositivo para espionaje ("Pulseras tóxicas") que manchen la reputación de la herramienta.
- **Ingeniería Inversa:** Agresores descubriendo el truco.

</div>

---

<!-- Fuentes -->

<div align="justify">

# DOCUMENTO 09: COMPENDIO DE REFERENCIAS Y FUENTES

**Impulsores:** Yaneth Villegas y Héctor Aguila

> **Nota del Equipo Impulsor:** Este compendio reúne las bases teóricas y técnicas que inspiraron el desarrollo conceptual. Invitamos a la comunidad experta a validarlo y ampliarlo.

## 1. Fuentes Públicas
- **UNICEF / Defensoría de la Niñez:** Informes sobre violencia y seguridad escolar.

## 2. Fuentes Técnicas
- **GSMA:** Guías de despliegue NB-IoT.
- **Proveedores (LCSC/Alibaba/Digikey):** Referencias de costos de hardware.

</div>
