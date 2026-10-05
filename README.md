# 🍕 Dejoma Pizzaria — Demo del menú digital

Demostración pública del menú digital por QR de **Dejoma Pizzaria**, para mostrar al cliente la experiencia que tendrán sus comensales.

**👉 Ver la demo:** https://bogotas-tech-solutions.github.io/dejoma-demo/

> ⚠️ **Versión de demostración.** Los precios y tamaños son provisionales hasta que el cliente los confirme. Los pedidos sí llegan al WhatsApp real de la pizzería.

## ✨ Qué se puede probar

- Menú completo de la pizzería (saladas y dulces), con descripciones.
- Cambio de idioma entre **portugués** y **español**.
- Personalización de las pizzas saladas (cebolla y/u orégano).
- Pizza destacada como especialidad de la casa.
- Carrito de pedido con cantidades y total en reales (R$).
- Envío del pedido armado por **WhatsApp**.

Está pensada para verse en el celular, igual que la verá un cliente al escanear el QR.

## 🧩 Cómo funciona

Es **un único archivo `index.html`** sin dependencias ni proceso de compilación, publicado con GitHub Pages.

El menú está **copiado dentro del archivo** (constante `SNAPSHOT`), generado a partir de la respuesta real de la API:

```
GET /api/v1/restaurants/dejoma-pizzaria/catalog?lang={pt-BR|es}
```

Por eso funciona sin un servidor encendido. La contraparte es que **no se actualiza sola**: si cambian los datos del menú en el backend, hay que regenerar este archivo.

## 🔄 Cómo actualizarla

1. Actualizar los datos en el backend (`pizzeria-backend`) y verificar la demo local en `http://localhost:8080/demo.html`.
2. Regenerar `index.html` con el nuevo contenido de la API para ambos idiomas.
3. Subir el archivo nuevo a este repositorio. GitHub Pages lo publica en uno o dos minutos.

## 📌 Pendientes con el cliente

- [ ] Precios reales y tamaños de cada pizza
- [x] Número de WhatsApp completo con código de área (DDD)
- [ ] Confirmar si hay bebidas u otros productos
- [ ] Confirmar si ofrecen *meio a meio*
- [ ] Fotos de las pizzas
- [ ] Revisión de las traducciones al español

## 🗂️ Repositorios del proyecto

| Repositorio | Propósito |
|---|---|
| [pizzeria-backend](https://github.com/bogotas-tech-solutions/pizzeria-backend) | API REST (Spring Boot + PostgreSQL) |
| [pizzeria-frontend](https://github.com/bogotas-tech-solutions/pizzeria-frontend) | Aplicación final (React + Vite + Tailwind) |
| **dejoma-demo** | Esta demo estática y temporal |

Este repositorio es **temporal**: se archivará cuando la aplicación final esté en producción.

## 👥 Equipo

- **Juan Daniel**: desarrollo
- **Santiago (Tato)**: producto, diseño y relación con el cliente

---
© Tato Tech Solutions
