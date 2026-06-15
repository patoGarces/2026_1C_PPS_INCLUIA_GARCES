![Logo Institucional](https://github.com/JonatanBogadoUNLZ/PPS-Jonatan-Bogado/blob/9952aac097aca83a1aadfc26679fc7ec57369d82/LOGO%20AZUL%20HORIZONTAL%20-%20fondo%20transparente.png)

<h1 align="center">
  INCLU-IA – Desarrollo Frontend para Sistema de Subtitulado en Tiempo Real
</h1>

<p align="center">
  <b>Práctica Profesional Supervisada – Ingeniería Mecatrónica</b><br>
  <b>Universidad Nacional de Lomas de Zamora – Facultad de Ingeniería</b>
</p>

<br>

**Tipo:** Práctica Profesional Supervisada (PPS)  
**Año académico:** 2026 – 1° Cuatrimestre  
**Carrera:** Ingeniería Mecatrónica  
**Materia:** Prácticas Profesionales Supervisadas  
**Docente:** Cristian Lukaszewicz  
**Autor:** Patricio Garcés

---

## Índice

* [Introducción](#introducción)
* [Resumen del proyecto](#resumen-del-proyecto)
* [Problema abordado](#problema-abordado)
* [Solución desarrollada](#solución-desarrollada)
* [Alcance de esta PPS](#alcance-de-esta-pps)
* [Estado actual](#estado-actual)
* [Descripción técnica](#descripción-técnica)
* [Arquitectura del sistema](#arquitectura-del-sistema)
* [Instrucciones de uso](#instrucciones-de-uso)
* [Tecnologías utilizadas](#tecnologías-utilizadas)
* [Evidencias y pruebas](#evidencias-y-pruebas)
* [Autor](#autor)
* [Licencia](#licencia)

---

## Introducción

INCLU-IA es un sistema de subtitulado en tiempo real orientado a mejorar la accesibilidad dentro del aula para estudiantes con sordera o hipoacusia.

El proyecto utiliza una Raspberry Pi para capturar audio desde un micrófono inalámbrico, procesarlo mediante motores de reconocimiento de voz y distribuir los subtítulos generados a través de una aplicación web accesible desde dispositivos conectados a una red local.

Esta Práctica Profesional Supervisada estuvo enfocada en el desarrollo y mejora del frontend web del sistema, trabajando sobre aspectos de usabilidad, accesibilidad, compatibilidad multiplataforma y experiencia de usuario para la visualización de subtítulos en tiempo real.

---

## Resumen del proyecto

INCLU-IA es una solución de subtitulado en tiempo real orientada a mejorar la accesibilidad dentro del aula para estudiantes con sordera o hipoacusia.

El sistema captura audio mediante un micrófono inalámbrico, procesa la voz utilizando motores de reconocimiento automático y distribuye los subtítulos generados a través de una aplicación web accesible desde dispositivos conectados a una red local.

Esta Práctica Profesional Supervisada estuvo enfocada en el desarrollo y mejora del frontend web encargado de presentar dichos subtítulos de forma clara, accesible y multiplataforma.

---

## Problema abordado

En contextos educativos, los estudiantes con dificultades auditivas requieren herramientas que les permitan acceder al contenido oral de una clase en tiempo real.

Las soluciones existentes suelen depender de servicios externos, conexión permanente a Internet o interfaces poco adaptadas para distintos dispositivos, lo que limita su utilización dentro del aula.

La falta de herramientas accesibles impacta directamente en la inclusión y en la posibilidad de seguir el desarrollo normal de una clase.

---

## Solución desarrollada

Se desarrolló una interfaz web responsive capaz de recibir y mostrar subtítulos en tiempo real generados por el sistema INCLU-IA.

Las principales funcionalidades incorporadas fueron:

* Visualización instantánea de subtítulos.
* Historial de transcripciones.
* Ajuste de tamaño de letra.
* Modo de alto contraste.
* Modo OLED para pantallas AMOLED.
* Persistencia de preferencias del usuario.
* Compatibilidad con dispositivos móviles, tablets y computadoras.
* Soporte para instalación como Progressive Web App (PWA).

La comunicación con el backend se realiza mediante Socket.IO, permitiendo la actualización de los subtítulos con baja latencia.

---

## Alcance de esta PPS

### Incluye

* Desarrollo y mantenimiento del frontend web.
* Integración con el backend mediante Socket.IO.
* Implementación de funciones de accesibilidad.
* Adaptación responsive para dispositivos móviles.
* Incorporación de soporte PWA.
* Validación en múltiples navegadores y sistemas operativos.

### No incluye

* Captura de audio.
* Procesamiento de voz.
* Entrenamiento o configuración de modelos de reconocimiento.
* Desarrollo del backend de transcripción.
* Infraestructura de red del sistema.

---

## Estado actual

🟢 **MVP funcional**

Actualmente el sistema permite:

* Visualizar subtítulos en tiempo real.
* Consultar el historial de transcripciones.
* Personalizar la experiencia de lectura.
* Instalar la aplicación como PWA.
* Utilizar la interfaz desde Android, iOS, Windows y macOS.

Próximamente se prevé realizar validaciones en entornos educativos reales y continuar optimizando la experiencia de usuario para escenarios de uso prolongado.

---

## Descripción técnica

El frontend fue desarrollado utilizando HTML, CSS y JavaScript, comunicándose con el backend mediante Socket.IO para recibir eventos de subtitulado en tiempo real.

Durante el desarrollo se trabajó principalmente sobre tres ejes.

### Experiencia de usuario

Se realizaron modificaciones orientadas a priorizar la lectura de subtítulos:

* Reorganización del layout.
* Optimización del espacio útil en pantalla.
* Reubicación de controles dentro de un menú desplegable.
* Mejora de la visualización del historial.
* Presentación de instrucciones claras para la conexión inicial.

### Accesibilidad

Se incorporaron distintas opciones de visualización.

#### Tamaño de letra configurable

Permite adaptar la lectura a las necesidades de cada usuario.

#### Alto contraste

Mejora la legibilidad en condiciones de iluminación adversas.

#### Modo OLED

Se implementó un esquema visual con fondo completamente negro orientado a pantallas OLED y AMOLED, mejorando el confort visual durante usos prolongados.

#### Persistencia de preferencias

Las configuraciones seleccionadas permanecen almacenadas localmente entre sesiones.

### Integración y pruebas

Se realizaron tareas de validación y corrección relacionadas con:

* Comunicación mediante Socket.IO.
* Simulación local para pruebas.
* Compatibilidad entre navegadores.
* Compatibilidad entre sistemas operativos.

### Conversión a PWA

Se incorporaron las capacidades necesarias para permitir la instalación de la aplicación como Progressive Web App.

Las tareas incluyeron:

* Implementación de Web App Manifest.
* Incorporación de iconografía específica.
* Registro de Service Workers.
* Configuración para Android e iOS.
* Gestión de recursos estáticos.

---

## Arquitectura del sistema

### Entradas

* Audio capturado mediante micrófono inalámbrico.
* Eventos Socket.IO generados por el backend.

### Procesamiento

* Raspberry Pi.
* Motor de reconocimiento de voz.
* Backend Flask + Flask-SocketIO.

### Salidas

* Subtítulos en tiempo real.
* Historial de transcripciones.

### Interfaz

* Aplicación web responsive.
* Compatible con teléfonos móviles, tablets y computadoras.

---

## Instrucciones de uso

### Requisitos previos

* Navegador compatible con JavaScript.
* Conexión a la red WiFi generada por INCLU-IA.

### Puesta en marcha

1. Conectarse a la red WiFi del sistema.
2. Abrir la URL indicada por el dispositivo.
3. Esperar la conexión automática con el backend.
4. Comenzar a visualizar los subtítulos.

### Uso

#### Configuración

Desde el menú superior es posible:

* Modificar tamaño de letra.
* Activar alto contraste.
* Activar modo OLED.

#### Historial

Los subtítulos generados permanecen disponibles en el historial para facilitar su consulta posterior.

---

## Tecnologías utilizadas

| Categoría                          | Tecnología                         |
| ---------------------------------- | ---------------------------------- |
| Backend utilizado para integración | Python, Flask, Flask-SocketIO      |
| Frontend                           | HTML5, CSS3, JavaScript            |
| Comunicación                       | Socket.IO                          |
| Aplicación Web                     | Progressive Web App (PWA)          |
| Plataforma objetivo                | Raspberry Pi                       |
| IA utilizada por el sistema        | Whisper / Faster-Whisper (backend) |

---

## Evidencias y pruebas

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

### Material adjunto sugerido

* Captura de funcionamiento en Android.
* Captura de funcionamiento en iOS.
* Captura de funcionamiento en Windows.
* Captura de funcionamiento en macOS.
* Video corto de instalación como PWA en Android.
* Captura del menú de accesibilidad.
* Captura del modo OLED.
* Captura del modo de alto contraste.

---

## Autor

**Patricio Garcés**
Ingeniería Mecatrónica – Facultad de Ingeniería – Universidad Nacional de Lomas de Zamora

---

## Licencia

Uso académico.

---

