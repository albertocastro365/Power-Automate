Una parte importante para estar al día de todos los cambios a nivel de producto Power Platform, que son muchos y frecuentes :D, es revisar a menudo la consola de M365 Message Center: https://admin.microsoft.com/Adminportal/Home#/MessageCenter
Para tener aceso a esta información se requiere de al menos un rol de Azure Power Platform Admin

Esta solución revisa cada día si hay novedades sobre la Power Platform y nos envia la entrada por correo.

# Requisitos
- Aplicación de Azure
  -   Permisos sobre la API de "Graph ServiceMessage.Read.All" y marcado el Grant admin
  -   Secreto generado y guardado en Key Vault
-   Sobre este Key Vault deben tener rol "Key Vault Secrets User" el usuario que ejecute el flow.

# Instrucciones
1. Descargar la solución de este repo.
2. Importar en vuestro entorno
3. Configurar las 2 conexiones de Office 365 Outlook y la de Azure Key Vault. Para esta última podés hacerlo via Oauth e indicándo el nombre del Vault:

![image](https://github.com/user-attachments/assets/5de52c74-c04b-4055-b3b7-992d77566906)

⚠️ Aquí por un motivo que desconozco, a fecha 25/11/2024, no permite configurar directamente la conexión de Azure Key Vault durante la importación.
Cómo workaround podéis crear una conexión con este conector como paso previo a la importación. Luego durante la importación ya la reconocerá directamente.

5. Por último quedaría editar el flow y meter tus datos en las 3 variables existentes: destinatarios del correo, Client ID de la aplicación de Azure y Tenant ID; y en la action del Azure Key Vault seleccionar el secreto a recuperar.
![image](https://github.com/user-attachments/assets/48fda8a6-edf5-4b5a-9ff1-468b2cc11b92)

6. Ahora ya tienes el flujo configurado estarás al día de todas las novedades de la Power Platform y cuando se implementarán en tu tenant.
