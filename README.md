![Logo Institucional](https://github.com/JonatanBogadoUNLZ/PPS-Jonatan-Bogado/blob/9952aac097aca83a1aadfc26679fc7ec57369d82/LOGO%20AZUL%20HORIZONTAL%20-%20fondo%20transparente.png)

# Universidad Nacional de Lomas de Zamora — Facultad de Ingeniería

# INCLU-IA – Desarrollo Frontend para Sistema de Subtitulado en Tiempo Real

**Tipo:** PPS

**Año:** 2026 — **Cuatrimestre:** 1C

**Carrera:** Ingeniería Mecatrónica

**Materia / Curso:** Prácticas Profesionales Supervisadas (PPS)

**Docente / Cátedra:** Cristian Lukaszewicz

**Autor:** Garcés, Patricio

---

# Introducción / Objetivo

## Contexto

INCLU-IA es un proyecto orientado a mejorar la accesibilidad dentro del aula mediante la generación y visualización de subtítulos en tiempo real.

El sistema utiliza una Raspberry Pi como plataforma principal para capturar audio proveniente de un micrófono inalámbrico, procesarlo mediante motores de reconocimiento de voz y distribuir los subtítulos a través de una aplicación web accesible desde dispositivos conectados a una red local.

Dentro del proyecto general, esta PPS estuvo enfocada específicamente en el desarrollo y mejora del frontend web encargado de presentar los subtítulos a los usuarios finales.

## Problema a resolver

Los estudiantes que requieren asistencia mediante subtitulado necesitan acceder a los textos generados por el sistema de manera rápida, clara y desde distintos dispositivos.

La interfaz debía adaptarse a teléfonos móviles, tablets y computadoras, ofreciendo además herramientas de accesibilidad que facilitaran la lectura prolongada de los subtítulos.

## Objetivo general

Desarrollar y optimizar la interfaz web de INCLU-IA para la visualización de subtítulos en tiempo real, priorizando accesibilidad, usabilidad y compatibilidad multiplataforma.

## Objetivos específicos

* Mejorar la experiencia de lectura de subtítulos en tiempo real.
* Implementar herramientas de accesibilidad visual.
* Adaptar la interfaz para dispositivos móviles.
* Incorporar soporte para instalación como Progressive Web App (PWA).
* Validar el funcionamiento en múltiples sistemas operativos y navegadores.
* Integrar correctamente el frontend con el backend mediante Socket.IO.

---

# Índice

* Brief
* Descripción técnica
* Arquitectura del sistema
* Instrucciones de uso
* Tecnologías utilizadas
* Listado de componentes
* Evidencias y pruebas
* Estructura del repositorio
* Autor
* Licencia

---

# Brief

## One-liner

Interfaz web accesible para la visualización de subtítulos generados en tiempo real por el sistema INCLU-IA.

## Elevator pitch

Este proyecto corresponde al desarrollo frontend de INCLU-IA, una solución de subtitulado en tiempo real orientada a estudiantes con sordera o hipoacusia.

La aplicación recibe subtítulos generados por un backend de reconocimiento de voz y los presenta mediante una interfaz optimizada para dispositivos móviles, incorporando herramientas de accesibilidad, compatibilidad multiplataforma y soporte para instalación como aplicación web progresiva (PWA).

Su objetivo es facilitar el acceso al contenido oral de una clase utilizando dispositivos comunes conectados a una red local, sin requerir acceso a Internet.

## Problema

* **Contexto:** Aula educativa.
* **Dolor principal:** Dificultad para acceder en tiempo real al contenido oral de una clase.
* **Impacto:** Menor accesibilidad e inclusión para estudiantes con sordera o hipoacusia.

## Solución propuesta

### Qué hace

* Muestra subtítulos en tiempo real.
* Mantiene historial de transcripciones.
* Permite personalizar la visualización.
* Funciona desde dispositivos móviles.
* Puede instalarse como PWA.

### Cómo lo hace

Audio → Motor de reconocimiento de voz → Backend → Socket.IO → Frontend Web → Usuario

### Valor diferencial

La solución funciona completamente dentro de una red local, sin necesidad de conexión a Internet, permitiendo acceso desde múltiples dispositivos simultáneamente.

## Alcance

### Incluye

* Interfaz responsive para móviles.
* Historial de subtítulos.
* Configuración de tamaño de letra.
* Modos visuales accesibles.
* Integración mediante Socket.IO.
* Instalación como PWA.

### No incluye

* Procesamiento de audio.
* Reconocimiento de voz.
* Infraestructura de red.
* Backend de transcripción.

## Estado del proyecto

* **Madurez:** MVP funcional.
* **Qué funciona actualmente:**

  * Visualización de subtítulos en tiempo real.
  * Historial de transcripciones.
  * Modos de accesibilidad.
  * Instalación como PWA.
  * Compatibilidad multiplataforma.
* **Próximos pasos:**

  * Validaciones en entornos de aula reales.
  * Optimización de experiencia de usuario.
  * Ajustes finales de despliegue.

---

# Descripción técnica

El frontend fue desarrollado utilizando HTML, CSS y JavaScript, comunicándose con el backend mediante Socket.IO para recibir eventos de subtitulado en tiempo real.

Durante el desarrollo se trabajó principalmente sobre tres ejes:

## Experiencia de usuario

Se realizaron modificaciones orientadas a priorizar la lectura de subtítulos:

* Reorganización del layout.
* Optimización del espacio útil en pantalla.
* Reubicación de controles dentro de un menú desplegable.
* Mejora de la visualización del historial.
* Presentación de instrucciones claras para la conexión inicial.

## Accesibilidad

Se incorporaron distintas opciones de visualización:

### Tamaño de letra configurable

Permite adaptar la lectura a las necesidades de cada usuario.

### Alto contraste

Mejora la legibilidad en condiciones de iluminación adversas.

### Modo OLED

Se implementó un esquema visual con fondo completamente negro orientado a pantallas OLED y AMOLED, mejorando el confort visual durante usos prolongados.

### Persistencia de preferencias

Las configuraciones seleccionadas permanecen almacenadas localmente entre sesiones.

## Integración y pruebas

Se realizaron tareas de validación y corrección relacionadas con:

* Comunicación mediante Socket.IO.
* Simulación local para pruebas.
* Compatibilidad entre navegadores.
* Compatibilidad entre sistemas operativos.

## Conversión a PWA

Se incorporaron las capacidades necesarias para permitir la instalación de la aplicación como Progressive Web App.

Las tareas incluyeron:

* Implementación de Web App Manifest.
* Incorporación de iconografía específica.
* Registro de Service Workers.
* Configuración para Android e iOS.
* Gestión de recursos estáticos.

---

# Arquitectura del sistema

## Entradas

* Audio capturado mediante micrófono inalámbrico.
* Eventos Socket.IO generados por el backend.

## Procesamiento

* Raspberry Pi.
* Motor de reconocimiento de voz.
* Backend Flask + Flask-SocketIO.

## Salidas

* Subtítulos en tiempo real.
* Historial de transcripciones.

## Interfaz

* Aplicación web responsive.
* Compatible con teléfonos móviles, tablets y computadoras.

---

# Instrucciones de uso

## Requisitos previos

* Navegador compatible con JavaScript.
* Conexión a la red WiFi generada por INCLU-IA.

## Puesta en marcha

1. Conectarse a la red WiFi del sistema.
2. Abrir la URL indicada por el dispositivo.
3. Esperar la conexión automática con el backend.
4. Comenzar a visualizar los subtítulos.

## Uso

### Configuración

Desde el menú superior es posible:

* Modificar tamaño de letra.
* Activar alto contraste.
* Activar modo OLED.

### Historial

Los subtítulos generados permanecen disponibles en el historial para facilitar su consulta posterior.

---

# Tecnologías utilizadas

| Categoría                          | Tecnología                         |
| ---------------------------------- | ---------------------------------- |
| Backend utilizado para integración | Python, Flask, Flask-SocketIO      |
| Frontend                           | HTML5, CSS3, JavaScript            |
| Comunicación                       | Socket.IO                          |
| Aplicación Web                     | Progressive Web App (PWA)          |
| Plataforma objetivo                | Raspberry Pi                       |
| IA utilizada por el sistema        | Whisper / Faster-Whisper (backend) |

---

# Listado de componentes

| Componente            | Cantidad | Modelo / Especificación   | Función                     |
| --------------------- | -------- | ------------------------- | --------------------------- |
| Raspberry Pi          | 1        | Raspberry Pi 4/5          | Ejecución del sistema       |
| Micrófono inalámbrico | 1        | Según disponibilidad      | Captura de audio            |
| Dispositivo cliente   | N        | Smartphone, tablet o PC   | Visualización de subtítulos |
| Punto de acceso WiFi  | 1        | Integrado en Raspberry Pi | Distribución local          |

---

# Evidencias y pruebas

Durante el desarrollo se realizaron pruebas sobre:

* Android
* iOS
* Windows
* macOS

Las pruebas incluyeron:

* Recepción de subtítulos en tiempo real.
* Persistencia de configuraciones.
* Instalación como PWA.
* Compatibilidad visual.
* Estabilidad de conexión.

Las evidencias de validación incluyen capturas de funcionamiento en Android, iOS, Windows y macOS, además de pruebas de instalación como PWA y verificación de las funcionalidades de accesibilidad implementadas.

---

# Estructura del repositorio

```text
web/
├── templates/
│   └── index.html
│
├── static/
│   ├── app.js
│   ├── styles.css
│   ├── manifest.json
│   ├── serviceWorker.js
│   ├── icon-128.png
│   └── icon-512.png
```

---

# Autor

**Patricio Garcés**
Ingeniería Mecatrónica – Facultad de Ingeniería – UNLZ

---

# Licencia

Uso académico.

---

# About (GitHub)

PPS — INCLU-IA Frontend — FI-UNLZ — 2026 1C — Garcés
