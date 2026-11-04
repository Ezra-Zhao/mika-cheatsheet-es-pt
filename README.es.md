# Mika · Guía rápida en español

Proyecto original: [wangzan101/Mika](https://github.com/wangzan101/Mika) · [Português](README.pt.md)


## Qué es Mika

Un agente de código abierto (Apache-2.0) que vive dentro de tu teléfono Android. Le dices qué necesitas y él abre apps, lee la pantalla, toca, escribe y desplaza en una **pantalla de fondo oculta**, mientras tú sigues usando el teléfono como siempre.

No necesita root ni integraciones con cada app: no usa las API de las aplicaciones, mira la pantalla y busca los botones como lo haría una persona. Y no existe un «servidor de Mika»: lo que dices y lo que hay en tu pantalla va solo al proveedor de modelos que tú configures.

La app ya trae interfaz en español y portugués, así que esta guía no traduce nada: te ahorra los tropiezos de instalación, emparejamiento y permisos que el README en inglés y chino no te cuenta en tu idioma.

## Empieza en tres pasos

1. **Instala**: descarga el APK desde [Releases](https://github.com/wangzan101/Mika/releases/latest) del repositorio original.
2. **Conecta un modelo**: en Ajustes › Modelo elige un proveedor y pega tu clave API, **o** inicia sesión con tu cuenta de ChatGPT, xAI u OpenRouter, sin clave.
3. **Solo si quieres que opere apps**: sigue el asistente «Set up phone control» en Ajustes y empareja la depuración inalámbrica una vez. Si solo quieres chat, web y archivos, sáltate este paso.

Primera prueba razonable: «Pon alarmas mañana a las 9:40 y a las 10:00» o «Revisa el tiempo cada mañana a las 8 y avísame solo si va a llover».

## Qué teléfono necesitas

| Uso | Requisito |
|---|---|
| Chat, web y archivos | Android 11 o posterior |
| Operar apps del teléfono | Android 12 o posterior |
| Recomendado | **Android 14+**: la pantalla de fondo tiene su propio foco y no estorba cuando escribes en la principal |
| Sandbox de Linux (Python, Node, shell) | Solo dispositivos arm64 |

¿Dudas de si tu teléfono llega? En Ajustes › Recovery & repair hay una **autocomprobación de compatibilidad**: 12 comprobaciones en alrededor de un minuto.

## Dos modos: empieza por Ask

| Modo | Comportamiento |
|---|---|
| **Ask** (predeterminado) | Hace todo por su cuenta y te pregunta **solo antes de gastar dinero** (hacer un pedido, pagar) |
| **Autonomous** | Ejecuta sin preguntar nada |

El error de principiante es estrenar Autonomous el primer día. Déjalo en Ask hasta que veas cómo trabaja en tus apps.

## Qué sabe hacer

- **Operar apps**: leer listas e historiales de chat largos, tocar, escribir, compartir texto en apps.
- **Navegar la web**: navegador integrado que mantiene tu sesión iniciada, lee páginas, descarga y sube archivos; si una página lo bloquea, te la pasa a ti.
- **Trabajar sobre lo que estás viendo**: doble toque en la cápsula flotante y le mandas tu pantalla actual («¿cómo respondo a esto?», «apunta esto»).
- **Tareas con horario y condiciones**: «recuérdame mañana a las 9», «haz esto cada viernes».
- **Sandbox de Linux por conversación**: corre Python, Node y shell sobre los archivos que le pases.
- **Recibir órdenes desde tu ordenador**: herramientas de IA en tu PC le pueden encargar tareas por CLI + Skill o por MCP.

## Apps con conocimiento integrado (útiles en Latinoamérica)

Mika funciona con cualquier app, pero trae conocimiento de uso precargado para varias. De las que más se usan en la región hispana y Brasil: **WhatsApp, Telegram, Uber, Uber Eats, Gmail, YouTube e Instagram** (Instagram figura como sitio web).

Detalle honesto: esos archivos de conocimiento están escritos en chino. No te limita: el modelo los lee sin problema y tú le hablas en español o portugués.

## Seguridad y límites, sin letra pequeña escondida

- **Pagos, contraseñas y códigos de verificación**: esas pantallas bloquean la captura, así que Mika no puede leerlas y te devuelve el control a ti. Es por diseño, no un fallo.
- **Términos de servicio**: automatizar apps y sitios de terceros puede ir contra sus condiciones de uso. Juicio propio: para cosas importantes, modo Ask y revisar el resultado.
- **La depuración inalámbrica se apaga sola** al cambiar de Wi-Fi o reiniciar el teléfono. Con tu permiso, Mika la reactiva por él mismo; si aun así no conecta, vuelve a «Set up phone control» y empareja de nuevo.
- **Sin servidor propio**: las claves API y las memorias se guardan cifradas en el teléfono; las conversaciones y registros no salen del dispositivo, y las comprobaciones de actualización solo contactan con GitHub.
- Algunas marcas recortan la depuración inalámbrica del sistema; en ese caso el asistente se puede arrancar desde un ordenador por USB (guía de instalación del repo original).

## Enlaces

- Repositorio: https://github.com/wangzan101/Mika
- Descarga (APK): https://github.com/wangzan101/Mika/releases/latest
- Guía de instalación del control del teléfono: https://github.com/wangzan101/Mika/blob/main/docs/setup-guide.en.md
