# 🗒️ Registro de Trabajo en Clase - Taller 5

## 📆 Fecha de la sesión
13 de septiembre de 2026.

## 👥 Integrantes presentes
- Mao Suárez
- Nicolas Clavijo

## 🧠 Actividades realizadas en clase

- Se revisó la [guía paso a paso de STRIDE](guia_paso_a_paso_stride.md) y el visual interactivo [`modelado-de-amenazas.html`](modelado-de-amenazas.html), enfocándose en el flujo de ejemplo de EdukIT (acceso de estudiantes a cursos y materiales).
- Se dibujó a mano el DFD del flujo de EdukIT (estudiante → autenticación → BD de usuarios → módulo de cursos → almacén de contenido) siguiendo el ejemplo de la guía, y se discutió por qué el límite de confianza se traza entre el estudiante y el backend, no dentro del backend.
- Se aplicaron las 6 categorías STRIDE sobre los 5 elementos del DFD (P1, P2, D1, D2 y los flujos F1-F6), formulando una amenaza por categoría tal como aparece en el Paso 3 de la guía, y se completaron impacto, probabilidad, nivel de riesgo, mitigación, responsable y estado para llegar a la tabla de 12 columnas.
- Se priorizaron las 6 amenazas por nivel de riesgo (T4 e T1 quedaron como "Alto", empatando con el orden que trae la guía).
- Se levantó el ambiente de OWASP Juice Shop en local (`docker run --rm -p 3000:3000 bkimminich/juice-shop`) y se completó el reto 1 (login bypass por inyección SQL con `' OR 1=1--` en el campo de correo): se confirmó el acceso como administrador sin conocer la contraseña real. Se documentó como una fila adicional (T7) en la tabla de clase, relacionada con la amenaza de Spoofing (T1) ya identificada sobre el sistema de autenticación.

## 🧩 Boceto inicial del modelo

DFD de EdukIT dibujado en clase (idéntico al de la guía, sección 3, Paso 1): Estudiante → [F1: credenciales] → P1 (Autenticación) → [F2] → D1 (BD Usuarios); P1 → [F3: token] → Estudiante → [F4: solicita curso + token] → P2 (Módulo de Cursos) → [F5] → D2 (Almacén de Contenido); P2 → [F6: contenido] → Estudiante. Límite de confianza entre el Estudiante (externo) y el backend de EdukIT.

## 🔁 Tareas definidas para complementar el taller

| Tarea asignada | Responsable | Fecha estimada |
|----------------|-------------|----------------|
| Por definir | Por definir | Por definir |

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del taller 5 en el curso AREM - Universidad de La Sabana._
