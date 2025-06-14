---
aliases:
- /es/monitors/faq/how-can-i-setup-an-alert-for-when-a-specific-tag-stops-reporting
further_reading:
- link: /monitors/
  tag: Documentación
  text: Aprender a crear un monitor
- link: /monitors/notify/
  tag: Documentación
  text: Configurar las notificaciones de tu monitor
title: Configurar una alerta para cuando una etiqueta (tag) específica deja de informar
---

En algunos casos, te gustaría saber cuándo desaparece una de tus etiquetas de alguno de tus sistemas. Es posible configurar un [monitor][1] para ese esquema de alerta en Datadog:

1. Configura un [monitor de métricas][2] clásico y determina sobre qué métricas y etiquetas quieres recibir alertas cuando están ausentes.
1. Selecciona una condición de alerta que no pueda activarse nunca. Por ejemplo, `a < -1`, para una métrica positiva como `system.cpu.user`.
1. Activa la opción Notificar si faltan datos, como se muestra en este ejemplo:

{{< img src="monitors/guide/tag_stop_reporting.png" alt="Etiqueta deja de informar" >}}

Tu alerta se activa si la etiqueta deja de informar.

## Referencias adicionales

{{< partial name="whats-next/whats-next.html" >}}

[1]: /es/monitors/
[2]: /es/monitors/types/metric/