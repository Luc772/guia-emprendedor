# Guía del Emprendedor — Financiamiento para Pymes del Biobío

Plataforma interactiva de una sola página (HTML/CSS/JS puro, sin backend ni dependencias de build) que resume la guía de financiamiento para Pymes: crédito privado, la CAE, fondos públicos (SERCOTEC/CORFO) y un simulador de ruta de decisión.

No requiere correo, login ni servidor: es 100% estática, ideal para GitHub Pages.

## 🌐 Ver en vivo

Una vez publicada, la plataforma quedará disponible en:

```
https://<tu-usuario>.github.io/<nombre-del-repo>/
```

## 🚀 Cómo publicarla en GitHub Pages

1. **Crea un repositorio nuevo** en GitHub (público), por ejemplo `guia-emprendedor-biobio`.
2. **Sube el archivo `index.html`** a la raíz del repositorio (puedes arrastrarlo directo en la interfaz web de GitHub, o vía git):
   ```bash
   git init
   git add index.html README.md
   git commit -m "Primera versión de la plataforma"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/<nombre-del-repo>.git
   git push -u origin main
   ```
3. Entra a **Settings → Pages** dentro del repositorio.
4. En **Source**, selecciona la rama `main` y la carpeta `/ (root)`.
5. Guarda. GitHub te entregará la URL pública en 1–2 minutos.

No hay que instalar nada más: no usa Node, no usa build step, no usa variables de entorno ni claves.

## 📁 Estructura

```
.
├── index.html   ← toda la plataforma (HTML + CSS + JS en un solo archivo)
└── README.md
```

## ✏️ Cómo editar el contenido

Todo el contenido vive dentro de `index.html`:

| Quiero cambiar... | Dónde buscar |
|---|---|
| Textos de cada sección | Bloques `<section class="panel" id="...">` |
| Preguntas del simulador de ruta | Objeto `tree` dentro del `<script>` |
| Resultados recomendados | Objeto `results` dentro del `<script>` |
| Términos del glosario | Arreglo `terms` dentro del `<script>` |
| Ítems de la lista de control | Arreglo `checks` dentro del `<script>` |
| Colores y tipografía | Bloque `:root { ... }` al inicio del `<style>` |

No se necesita recompilar nada: guarda el archivo y recarga la página.

## 🔒 Privacidad

La plataforma no recolecta datos, no usa cookies ni analíticas, y no requiere que el usuario ingrese correo ni información personal.

## 📄 Licencia

Contenido educativo de uso libre, basado en la guía original de financiamiento para Pymes de la Región del Biobío.
