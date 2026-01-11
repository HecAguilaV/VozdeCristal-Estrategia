# DOCUMENTO 10: ROADMAP TÉCNICO Y ARQUITECTURA DE DESARROLLO

<div align="justify">

**Impulsores:** Yaneth Villegas y Héctor Aguila

> **Nota:** Este documento define la estrategia de implementación técnica ("El Cómo"), separando la investigación científica del desarrollo de producto para mantener orden y escalabilidad.

## 1. Estructura de Repositorios (Workspace)

Para evitar la deuda técnica, el proyecto se divide en tres pilares independientes pero conectados:

### 📂 1. Voz-Cristal-Web (Estrategia y Fachada)
*   **Propósito:** Es la "cara visible" y el cuartel general estratégico.
*   **Contenido:**
    *   Sitio Web Público (`public/index.html`).
    *   **Dossier Confidencial (`docs/`).**
    *   Encuesta y Dashboard de métricas sociales.
*   **Tecnología:** HTML5, TailwindCSS, Vanilla JS.

### 📂 2. Voz-Cristal-ID (Investigación y Ciencia de Datos)
*   **Propósito:** El Laboratorio. Aquí se entrena al "cerebro" (TinyML).
*   **Contenido:**
    *   Generación de **Datos Sintéticos** (scripts Python para simular caídas/taquicardia).
    *   Entrenamiento de modelos (Random Forest/Decision Trees).
    *   Exportación del modelo a C++ (`model.h`).
*   **Tecnología:** Python, Pandas, Scikit-learn, m2cgen.

### 📂 3. Voz-Cristal-Prototipo (Firmware y Hardware)
*   **Propósito:** La Fábrica. Aquí se integra el cerebro en el chip.
*   **Contenido:**
    *   Código fuente del firmware para ESP32/NB-IoT.
    *   Lógica de "Panic Trigger" y gestión de energía.
    *   Simulaciones de hardware.
*   **Tecnología:** C/C++, PlatformIO, Wokwi (Simulador Web).

---

## 2. Estrategia de Desarrollo "Costo Cero" (Fase 1)

Antes de invertir en hardware físico, validaremos la lógica mediante simulación computacional.

### Paso 1: Generación de Datos (Repo: I+D)
Crearemos scripts en Python que generen archivos CSV simulando tres escenarios:
1.  **Reposo/Clase:** Acelerómetro estable, ritmo cardíaco normal.
2.  **Recreo/Juego:** Acelerómetro agitado, ritmo cardíaco alto (pero gradual).
3.  **Evento Crítico:** Acelerómetro con pico de impacto (G-Force) + Taquicardia explosiva (en <3 seg).

### Paso 2: El Modelo (Repo: I+D)
Entrenaremos un clasificador simple (Random Forest) que aprenda a decir: *"Si G-Force > X y HR sube muy rápido = ALERTA"*.
*   **Output:** Un archivo `model.h` que contiene la lógica en C puro.

### Paso 3: La Simulación (Repo: Prototipo)
Usaremos **Wokwi** (simulador online de ESP32) para probar el código C++.
*   Copiaremos el `model.h`.
*   Simularemos las entradas de los sensores moviendo sliders en la web.
*   Verificaremos que el "LED de Alerta" se encienda solo en el escenario de crisis.

---

## 3. Próximos Pasos Sugeridos

1.  **Inicializar Repositorio I+D:** Crear el primer script de datos sintéticos.
2.  **Entrenar Modelo v0.1:** Lograr un 90% de precisión en datos simulados.
3.  **Configurar Wokwi:** Ver el "cerebro" funcionando en un chip virtual.

</div>
