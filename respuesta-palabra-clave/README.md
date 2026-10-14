# Respuesta automática por palabra clave en Instagram

Flujo que convierte un comentario en una conversación: cuando alguien comenta una palabra clave en una publicación, el sistema responde en público, le envía un mensaje privado, crea su ficha en el CRM y avisa al equipo por email.

- **Demo interactiva:** [`index.html`](index.html). Reproduce la lógica del flujo con datos ficticios, en el navegador.
- **Flujo real:** montado en GoHighLevel sobre una cuenta de Instagram de empresa. Probado de principio a fin el 05/10/2026 con una cuenta de prueba: llegaron la respuesta pública, el mensaje privado y el email de aviso. El contacto de prueba se borró después.

## Problema que resuelve

Cuando una publicación pide «comenta X y te lo envío», alguien tiene que estar pendiente para contestar uno a uno. Si tarda horas, el interés se enfría; si se le pasa un comentario, se pierde el contacto.

## Cómo funciona

| Paso | Qué hace | Herramienta |
|---|---|---|
| 1. Disparador | Comentario nuevo en una publicación de la cuenta que contiene la palabra clave | GoHighLevel · disparador de comentarios de Instagram |
| 2. Respuesta pública | Contesta al comentario para que se vea que hay respuesta | GoHighLevel · acción de respuesta a comentario |
| 3. Mensaje privado | Envía a quien comentó el contenido prometido | GoHighLevel · mensaje directo de Instagram |
| 4. Registro | Crea o actualiza el contacto y abre una oportunidad en el embudo | GoHighLevel · CRM |
| 5. Aviso | Email al equipo con el nombre de la cuenta para seguir la conversación | GoHighLevel · email interno |

## Decisiones de diseño

- **Palabra suelta, no fragmento:** en la demo, «ecosistema» no dispara el flujo y no importan mayúsculas ni tildes.
- **Un solo envío por persona:** en la demo, si alguien comenta dos veces, no recibe el mensaje repetido; el nuevo comentario solo se anota en su ficha.
- **El aviso al equipo siempre sale:** si el mensaje privado falla (por ejemplo, porque la persona tiene los mensajes cerrados), el equipo lo sabe y puede escribir a mano.

## Límites

- Instagram solo permite **una respuesta privada por comentario** y en un plazo limitado tras el comentario.
- Hace falta una cuenta profesional de Instagram vinculada a una página de Facebook.
- El flujo no decide nada por la persona: entrega lo prometido y avisa. La conversación posterior la lleva el equipo.

## Privacidad

Ni la demo ni este repositorio contienen datos de personas reales. La demo no guarda ni envía nada: todo ocurre en el navegador.
