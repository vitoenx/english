# 📘 Prototipo 003 – Detección y práctica del Pasado Simple

## 🎯 Objetivo

En este tercer prototipo se busca establecer una práctica sistemática de evaluación automatizada del **tiempo verbal "Pasado Simple"**, empleando inteligencia artificial como tutor.

Este prototipo se centra en:

- Desarrollar pruebas personalizadas con múltiples ejercicios de opción múltiple.
- Automatizar la **generación, corrección y retroalimentación** mediante IA.
- Usar técnicas de **fuerza bruta y repetición consciente** para fomentar la internalización del tiempo verbal.
- Detectar errores mediante **etiquetas predefinidas** orientadas a análisis semántico y gramatical para aprendizaje supervisado.
- Realizar una evaluación **dual**: una interpretación cualitativa para humanos (profesores o el propio usuario) y otra orientada a estructuras de **Machine Learning y Dashboards**.

## 📐 Diseño del sistema

1. La IA actúa como tutor para generar sesiones de 15 ejercicios, evaluando distintos casos comunes del presente simple:
   - Afirmaciones, negaciones, preguntas.
   - Tercera persona singular.
   - Uso correcto del verbo base y auxiliares.

2. Cada sesión genera un archivo JSON estructurado y su correspondiente versión en Markdown para análisis humano.

3. Se implementan **12 etiquetas gramaticales** como clasificador de errores frecuentes.

4. La fase actual se enfoca en *detección de errores* (reconocimiento), mientras que en fases posteriores se aplicará producción del lenguaje (respuesta abierta, análisis sintáctico más profundo).

---

## 🔁 Instrucciones de uso

- 📁 Ruta del prompt: `/log/reading/detection_simple_past.md`
- 🧪 Ejecutar el prompt en tu modelo IA preferido (ChatGPT, Grok, Gemini).
- 💾 Guardar los resultados en Markdown o JSON bajo el mismo nombre del prototipo.
- 📊 Los logs pueden procesarse luego con Python o dashboards para visualizar errores frecuentes y progresos.

---

## 🧠 Prompt estándar
Eres un tutor de inglés experto para hispanohablantes. Diseña una sesión de 15 preguntas de opción múltiple para practicar el **Pasado Simple** de manera integral (afirmativo, negativo, preguntas, irregulares, regulares, expresiones temporales, contexto real, errores comunes).

- Nivel: B1
- Mezclar verbos regulares e irregulares.
- Incluir estructuras positivas, negativas y preguntas.
- Incluir oraciones con expresiones temporales (*last week, two days ago, when I was a kid*), y conectores (*but, because*).
- El objetivo es evaluar el dominio general del pasado simple.
- Cuando el usuario responde, genera:

🎯 Salida JSON estructurada:
Incluye:
- `fecha`
- `titulo`
- `nivel_objetivo`
- `nivel_estimado`
- `aciertos`
- `errores` 
- `errores_frecuentes`: etiquetas tipo ML
- `errores_descriptivos`: explicaciones para revisión humana
- `tema`: descripción general
- `observaciones_usuario`

Y además entrega una versión markdown del mismo reporte.

