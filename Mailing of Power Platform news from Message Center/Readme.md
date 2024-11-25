Una parte importante para estar al día de todos los cambios a nivel de producto Power Platform, que son muchos y frecuentes :D, es revisar a menudo la consola de M365 Message Center: https://admin.microsoft.com/Adminportal/Home#/MessageCenter
Para tener aceso a esta información se requiere de al menos un rol de Azure Power Platform Admin

Esta solución revisa cada día si hay novedades sobre la Power Platform y nos envia la entrada por correo.

# Requisitos
- Aplicación de Azure
  -   Permisos sobre la API de "Graph ServiceMessage.Read.All" y marcado el Grant admin
  -   Secreto generado y guardado en Key Vault
-   Sobre este Key Vault deben tener rol ey Vault Secrets User el usuario que ejecugte el flow y la identidad Dataverse

Mas info:
https://learn.microsoft.com/en-us/power-apps/maker/data-platform/environmentvariables-azure-key-vault-secrets#create-a-power-automate-flow-to-test-the-environment-variable-secret

# Instrucciones
1. Descargar la solución de este repo.
2. Importar en nuestro entorno
3. Configurar las 2 conexiones de Dataverse y Office 365 Outlook
4. En este paso, dejar el campo en vacío, mas adelante configurás tu variable de entorno con tus Key Vault.
![image](https://github.com/user-attachments/assets/3dd54164-fd7a-4618-b015-ccd08d240186)
5. Abrir la solución y editar la variable de entorno:
   ![image](https://github.com/user-attachments/assets/0eb2b946-efd1-49d2-99f3-92bfa5061440)

7. Añadir los datos de vuestro entorno y guardar:

   ![image](https://github.com/user-attachments/assets/ffc7d5ce-fecc-4fc0-bc28-645720e7d565)
8. Por último quedaría editar el flow y meter tus datos en las 3 variables existentes: destinatarios del correo, Client ID de la aplicación de Azure y Tenant ID
![image](https://github.com/user-attachments/assets/52b17c0d-9f5d-4da6-a972-4e683bd9907e)
9. Ahora ya tienes el flujo configurado estarás al día de todas las novedades de la Power Platform y cuando se implementarán en tu tenant.
