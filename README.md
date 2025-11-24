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

<img width="579" height="480" alt="imagen" src="https://github.com/user-attachments/assets/74cbe371-6928-49c7-b6d9-64acd0db6653" />

<img width="580" height="459" alt="imagen" src="https://github.com/user-attachments/assets/3951e450-143f-4cfa-a5b1-170ac45be55b" />

<img width="590" height="304" alt="imagen" src="https://github.com/user-attachments/assets/734f15b4-15c5-4370-9adf-cd18f673fab1" />

<img width="475" height="536" alt="imagen" src="https://github.com/user-attachments/assets/7f871353-a962-45de-81d2-d493016a6483" />

<img width="431" height="340" alt="imagen" src="https://github.com/user-attachments/assets/152cd247-90fd-486f-b3fc-e73f49624563" />

<img width="638" height="579" alt="imagen" src="https://github.com/user-attachments/assets/9b0b9ef6-072a-47b3-99b4-bf677ebc8e09" />

<img width="1169" height="253" alt="imagen" src="https://github.com/user-attachments/assets/3e62fb7a-1e0e-4ae3-aafc-a411a75682fa" />


---

## ⚙️ Configuración inicial

Introduce los siguientes campos:

- ✅ URL de tu instancia de Odoo  
- ✅ Nombre de la base de datos  
- ✅ (Opcional) Meet de Daily

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
