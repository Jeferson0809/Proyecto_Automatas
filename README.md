# 📧 Clasificador de Correos Spam con Autómata No Determinista (NFA)

Este proyecto implementa un sistema simple de clasificación de correos electrónicos utilizando un **autómata no determinista (NFA)**. La solución detecta la presencia de palabras clave asociadas con spam y estima la probabilidad de que un correo sea no deseado.

---

## 🧠 Descripción del Proyecto

El objetivo es identificar correos electrónicos spam analizando su contenido textual. Esto se logra reconociendo palabras comúnmente utilizadas en mensajes de spam, como "Gano", "Gratis", "Oferta", entre otras.

El sistema clasifica el correo como:
- 📈 **Alta probabilidad de spam**: si contiene varias palabras clave.
- 📉 **Baja probabilidad de spam**: si contiene pocas o ninguna palabra clave.

---

## ⚙️ Estrategia de Solución

1. **Preprocesamiento del mensaje:**
   - Conversión a minúsculas.
   - Eliminación de signos de puntuación y tildes.
   - División del texto en palabras.

2. **Construcción del autómata NFA:**
   - El alfabeto contiene solo letras del abecedario.
   - Cada palabra clave define un conjunto de transiciones.
   - Si el mensaje permite llegar a un estado de aceptación → se detecta spam.

3. **Clasificación:**
   - Se calcula cuántas palabras clave se encuentran en el mensaje.
   - Cuantas más se encuentren, mayor será la probabilidad de spam.

---

## 📚 Diccionario de Palabras Spam

> Palabras base usadas por el autómata:

Seleccionado, Gano, Ganado, Gratis, Gratuito, Dinero, Duplica,
Consíguelo, Conseguido, Regalo, Regalamos, Oferta, Obsequio,
Obsequiamos, Empieza, Elegido, Felicitaciones, Promoción,
Increíble, Urgente

---

## 🔬 Pruebas del Sistema

Se probaron cuatro correos:

- **Ejemplos Spam**:
  - "¡Felicitaciones, has sido elegido... Oferta especial... promoción limitada..."
  - "¡Urgente! Ha sido seleccionado... Obsequiamos celulares..."

- **Ejemplos No Spam**:
  - Correo académico con notas.
  - Correo de agradecimiento y novedades para socios.

**Resultado:**  
✔️ El sistema clasificó correctamente los correos spam y no spam con base en las palabras clave detectadas.

---

## 🧪 Limitaciones

- Solo detecta palabras explícitas presentes en el diccionario.
- No identifica sinónimos, palabras con errores ortográficos ni contexto semántico.
- Puede evolucionarse con aprendizaje automático o modelos de lenguaje.

---

## 👨‍💻 Autores

- **Nicolás Quintero Sierra** — `2220090`  
- **Jeferson Jair Acevedo Sarmiento** — `2221790`

---

## 📖 Bibliografía

- [Lista definitiva de palabras spam – Benchmark Email](https://www.benchmarkemail.com/es/blog/la-lista-definitiva-de-palabras-de-activacion-de-spam-en-emails/)
