# Tamper-Monkey-Meet  
Automatiza imputaciones desde Google Meet en Odoo

Script TamperMonkey para registrar automáticamente imputaciones en Odoo a partir del tiempo en llamadas de Google Meet.

📎 **Script para instalar:**

https://raw.githubusercontent.com/FlJesusLorenzo/tamper-monkey-meet/refs/heads/main/main/script.user.js

---

## 🧩 ¿Cómo funciona?

Pasados **5 segundos** desde que entras a una llamada de Google Meet, aparecerá un botón flotante:

<img width="353" height="235" alt="imagen" src="https://github.com/user-attachments/assets/8cf9ea01-a405-4220-90db-e8ff15cf5f13" />

Al pulsarlo, se abrirá un popup de configuración.  
Si vuelves a pulsar en el engranaje, el popup se ocultará.

<img width="617" height="359" alt="imagen" src="https://github.com/user-attachments/assets/301fc815-14b0-46dc-8c41-48d167b4088d" />

---

## ⚙️ Configuración inicial

Introduce los siguientes campos:

- ✅ URL de tu instancia de Odoo  
- ✅ Nombre de la base de datos  
- ✅ (Opcional) Meet de Daily  
- ✅ (Opcional) Meet de Refinamiento  
  > Si Daily y Refinamiento usan el **mismo enlace**, deja vacío el campo de refinamiento.

Tras guardar, si la configuración es incorrecta, el botón aparecerá en **amarillo**:

<img width="79" height="71" alt="imagen" src="https://github.com/user-attachments/assets/8095f18d-3974-4b2a-91ae-0fec4ea6f137" />

---

## 🕓 Imputación personalizada

Después de configurar la herramienta, solo deberás usar la sección de imputación personalizada para seleccionar:

- Proyecto  
- Tarea  
- Descripción  

<img width="613" height="330" alt="imagen" src="https://github.com/user-attachments/assets/30299e87-c43e-4fa7-9b99-03da4ee4c435" />

Al pulsar **Imputar**:

- Se registrará el tiempo trabajado en Odoo  
- El contador se reiniciará para la siguiente imputación  

---

## 🤖 Daily y Refinamiento automáticos

- Al entrar a un Meet configurado para Daily o Refinamiento:
  - Se seleccionarán automáticamente el proyecto, la tarea y el nombre de la reunión como descripción

- Si ambos usan el mismo Meet:
  - La primera imputación será para Daily  
  - Tras pulsar **Imputar**, cambiará automáticamente a Refinamiento

---

## ☎️ Botón de colgar

Al colgar la llamada:

| Comportamiento | Resultado |
|---|---|
Tarea configurada | ✅ Se imputa automáticamente  
Sin tarea configurada | ❌ No se imputa nada  

---

## ⚠️ Consideraciones

| Acción | ¿Se imputa tiempo? |
|-------|--------------------|
Pulsar **Imputar** | ✅ Sí  
Colgar llamada | ✅ Sí (si hay tarea configurada)  
Recargar la página | ❌ No  
Cerrar la pestaña | ❌ No  
