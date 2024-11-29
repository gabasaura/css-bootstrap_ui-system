# Arquitectura CSS Propuesta: Modular + Componente-Primero

Este proyecto utiliza una estructura diseñada específicamente para proyectos grandes, que requieren componentes personalizados y extensos. La arquitectura combina principios de **Atomic Design**, **ITCSS**, y personalización avanzada de **Bootstrap**, permitiendo escalabilidad, mantenibilidad y claridad en el desarrollo.

---

## Estructura de Carpetas

El proyecto organiza los estilos de manera modular y jerárquica, como se muestra a continuación:

# Estructura de CSS 📂

```plaintext
resources/
 ├── css/
 │   ├── abstracts/    # Variables, mixins, funciones (base de todo)
 │   │   ├── _variables.scss
 │   │   ├── _mixins.scss
 │   │   ├── _functions.scss
 │   ├── base/         # Estilos base del proyecto
 │   │   ├── _reset.scss      # Reseteo de estilos (opcional)
 │   │   ├── _typography.scss # Tipografía global
 │   │   ├── _utilities.scss  # Clases utilitarias
 │   ├── bootstrap/    # Personalizaciones de Bootstrap
 │   │   ├── _overrides.scss  # Sobreescrituras generales de Bootstrap
 │   │   ├── _custom.scss     # Nuevas clases o componentes
 │   ├── components/   # Componentes específicos del proyecto
 │   │   ├── buttons.scss     # Botones personalizados
 │   │   ├── navbar.scss      # Barra de navegación
 │   │   ├── modal.scss       # Modales personalizados
 │   │   ├── cards.scss       # Tarjetas
 │   ├── layouts/      # Estructura global de páginas
 │   │   ├── header.scss
 │   │   ├── footer.scss
 │   │   ├── sidebar.scss
 │   ├── pages/        # Estilos específicos para vistas o páginas
 │   │   ├── home.scss
 │   │   ├── dashboard.scss
 │   │   ├── profile.scss
 │   └── app.scss      # Punto de entrada para importar todo
```
---

### Descripción de Carpetas y Archivos

- **`abstracts/`**: Contiene las herramientas fundamentales del proyecto como variables, mixins y funciones, que son reutilizables en todo el proyecto.
- **`base/`**: Define los estilos base del proyecto, como el reseteo de estilos, tipografía global y clases utilitarias.
- **`bootstrap/`**: Maneja las personalizaciones de Bootstrap, incluyendo sobreescrituras y nuevos componentes basados en el framework.
- **`components/`**: Almacena los estilos de componentes específicos como botones, modales, tarjetas, etc.
- **`layouts/`**: Diseña la estructura global del proyecto, incluyendo encabezados, pies de página y barras laterales.
- **`pages/`**: Define estilos específicos para vistas o páginas del proyecto, como inicio, dashboard o perfil.
- **`app.scss`**: Archivo principal que importa y combina todos los estilos en un único punto de entrada.

---

## Ventajas de esta Arquitectura

1. **Escalabilidad**: Diseñada para proyectos grandes, permite añadir nuevos componentes o vistas sin afectar la estructura existente.
2. **Modularidad**: Cada parte del proyecto está separada, lo que facilita su mantenimiento.
3. **Reutilización**: Los archivos en `abstracts/` aseguran consistencia al reutilizar variables y mixins en todo el proyecto.
4. **Personalización de Bootstrap**: Permite adaptarse a las necesidades específicas del proyecto sin perder la potencia del framework.

---

## Cómo Empezar

1. **Compila los Estilos**: Asegúrate de compilar `app.scss` utilizando una herramienta como [Sass](https://sass-lang.com/) o un bundler como [Vite](https://vitejs.dev/).
2. **Configura Bootstrap**: Importa las personalizaciones en `bootstrap/_overrides.scss` y añade las clases necesarias en `bootstrap/_custom.scss`.
3. **Sigue la Convención**: Organiza los nuevos estilos según esta estructura para garantizar claridad y consistencia.

---

### Recursos Recomendados

- [Guía Oficial de Sass](https://sass-lang.com/guide)
- [Bootstrap Customization](https://getbootstrap.com/docs/5.0/customize/)
- [Atomic Design](https://bradfrost.com/blog/post/atomic-web-design/)
- [ITCSS](https://itcss.io/)

---

¡Esperamos que disfrutes trabajando con esta arquitectura! 🚀

