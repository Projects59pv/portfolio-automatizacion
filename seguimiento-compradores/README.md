# Seguimiento de compradores para un agente inmobiliario

Mini CRM que sustituye la hoja compartida donde un agente apunta a sus compradores e inquilinos. Responde a una pregunta: **¿a quién tengo que llamar hoy?**

- **Demo:** [`index.html`](index.html). Se abre con datos de ejemplo inventados.

## Qué hace

| Función | Detalle |
|---|---|
| Alta y edición | Nombre, teléfono, compra o alquiler, inmueble o zona, presupuesto, estado, próxima acción con fecha y notas |
| Estados | Nuevo, Contactado, Visita agendada, Visitado, Oferta, Cerrado, Descartado |
| Resumen del día | Cuántos contactos tienen la próxima acción atrasada, cuántos tocan hoy y cuántos llevan 7 días o más sin contacto. Cada cifra filtra la lista |
| Búsqueda y filtros | Por texto (nombre, zona, notas) y por estado. Por defecto solo se ven los activos |
| Mensaje de seguimiento | Texto según el estado del contacto, editable, con botón de copiar y enlace directo a WhatsApp si hay teléfono |
| «Contactado hoy» | Registra el contacto y lo saca de la lista de fríos |
| Exportar | CSV separado por punto y coma, con BOM, para abrirlo directamente en Excel en español |

## Decisiones

- **Sin servidor ni cuentas:** los datos se guardan en el almacenamiento local del navegador. Si el navegador lo bloquea, la demo sigue funcionando en memoria.
- **Ordenada por la próxima fecha:** lo primero que se ve es lo que toca antes.
- **Lo cerrado y lo descartado no estorban:** salen de la lista y de los contadores, pero se pueden ver filtrando por estado.

## Cómo sería la versión real

Los contactos entrarían solos desde los portales inmobiliarios o el formulario de la web, los datos estarían en una base compartida por el equipo y el resumen de «para hoy» llegaría por email cada mañana.

## Privacidad

Los datos de ejemplo son inventados y los teléfonos no existen. Nada sale del navegador.
