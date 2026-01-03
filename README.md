# 🛍️ Introducción a Shopify

Proyecto de ejemplo para aprender los conceptos básicos del desarrollo de temas en Shopify. Este repositorio contiene una estructura básica de tema con ejemplos de archivos Liquid, estilos CSS y configuraciones.

## 📋 Tabla de Contenidos

- [Características](#características)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Requisitos Previos](#requisitos-previos)
- [Instalación](#instalación)
- [Uso](#uso)
- [Archivos Principales](#archivos-principales)
- [Recursos de Aprendizaje](#recursos-de-aprendizaje)
- [Contribuir](#contribuir)
- [Licencia](#licencia)

## ✨ Características

- Estructura básica de tema de Shopify
- Sección de encabezado personalizable
- Componente de tarjeta de producto reutilizable
- Estilos CSS con variables CSS personalizadas
- Configuración de plantillas JSON
- Ejemplos de uso de Liquid

## 📁 Estructura del Proyecto

```
introduccion-shopify/
├── assets/
│   └── styles.css          # Estilos globales del tema
├── sections/
│   └── header.liquid       # Sección del encabezado
├── snippets/
│   └── product-card.liquid # Componente de tarjeta de producto
├── templates/
│   └── index.json          # Plantilla de la página principal
├── .gitignore
├── package.json
└── README.md
```

### Descripción de Carpetas

- **`assets/`** - Recursos estáticos (CSS, JavaScript, imágenes)
- **`sections/`** - Secciones modulares del tema que se pueden agregar, remover y reordenar
- **`snippets/`** - Fragmentos de código reutilizables
- **`templates/`** - Plantillas de páginas (formato JSON o Liquid)

## 🔧 Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

- [Node.js](https://nodejs.org/) (versión 14 o superior)
- [Shopify CLI](https://shopify.dev/docs/themes/tools/cli)
- Una cuenta de [Shopify Partners](https://partners.shopify.com/) (gratuita)
- Una tienda de desarrollo de Shopify

## 📦 Instalación

1. **Clona este repositorio:**
   ```bash
   git clone https://github.com/cristianjonhson/introduccion-shopify.git
   cd introduccion-shopify
   ```

2. **Instala las dependencias:**
   ```bash
   npm install
   ```

3. **Instala Shopify CLI** (si aún no lo tienes):
   ```bash
   npm install -g @shopify/cli @shopify/theme
   ```

4. **Autentícate con Shopify:**
   ```bash
   shopify auth login
   ```

5. **Crea o conecta una tienda de desarrollo:**
   
   Si no tienes una tienda de desarrollo, puedes crear una desde tu [cuenta de Shopify Partners](https://partners.shopify.com/):
   - Ve a "Tiendas" → "Agregar tienda" → "Crear tienda de desarrollo"
   - Una vez creada, copia la URL de tu tienda (ej: `mi-tienda-dev.myshopify.com`)

## 🚀 Uso

### Desarrollo Local

Para iniciar el servidor de desarrollo local, necesitas especificar tu tienda:

```bash
shopify theme dev --store=tu-tienda.myshopify.com
```

O puedes configurar la variable de entorno:

```bash
export SHOPIFY_FLAG_STORE=tu-tienda.myshopify.com
shopify theme dev
```

Esto abrirá tu tema en un navegador con recarga en caliente. Los cambios que hagas se reflejarán automáticamente.

### Subir el Tema

Para subir tu tema a Shopify:

```bash
shopify theme push --store=tu-tienda.myshopify.com
```

### Descargar el Tema

Para descargar cambios desde Shopify:

```bash
shopify theme pull --store=tu-tienda.myshopify.com
```

> **Tip:** Para evitar escribir `--store` en cada comando, puedes crear un archivo `.shopify-cli.yml` en la raíz del proyecto con:
> ```yaml
> store: tu-tienda.myshopify.com
> ```

## 📄 Archivos Principales

### `sections/header.liquid`

Sección del encabezado que incluye:
- Logo de la tienda (configurable)
- Menú de navegación
- Enlace al carrito
- Schema para configuración desde el editor de temas

### `snippets/product-card.liquid`

Componente reutilizable que muestra:
- Imagen del producto
- Título del producto
- Precio (con soporte para precios en oferta)

### `assets/styles.css`

Estilos CSS globales con:
- Variables CSS para colores del tema
- Reset básico de estilos
- Clases de utilidad

### `templates/index.json`

Plantilla JSON para la página principal que define:
- Secciones a mostrar
- Configuración de cada sección
- Orden de las secciones

## 📚 Recursos de Aprendizaje

### Documentación Oficial

- [Shopify Theme Development](https://shopify.dev/docs/themes)
- [Liquid Reference](https://shopify.dev/docs/api/liquid)
- [Theme Architecture](https://shopify.dev/docs/themes/architecture)
- [Shopify CLI](https://shopify.dev/docs/themes/tools/cli)

### Tutoriales

- [Shopify Theme Tutorial](https://shopify.dev/docs/themes/getting-started)
- [Build a Shopify Theme from Scratch](https://www.shopify.com/partners/blog/topics/shopify-theme-development)

### Comunidad

- [Shopify Community Forums](https://community.shopify.com/)
- [Shopify Partners Slack](https://shopifypartners.slack.com/)

## 🤝 Contribuir

Las contribuciones son bienvenidas. Si deseas mejorar este proyecto:

1. Haz un Fork del proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

## 👤 Autor

**Cristian Johnson**

- GitHub: [@cristianjonhson](https://github.com/cristianjonhson)

---

⭐ Si este proyecto te resultó útil, considera darle una estrella en GitHub!
