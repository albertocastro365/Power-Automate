Una buena práctica para un equipo de administración de Power Platform es restringir la creación de nuevos entornos a los usuarios y que soliciten su creación de manera justificada.

Pero sobre los entornos Teams no tenemos esa capacidad de restricción. Los usuarios puede crear entornos Dataverse for Teams directamente desde sus Teams.

Además estos entornos tienen muchas limitaciones y deberían ser sólo usados para soluciones de prueba, personales, nada crítico.

Entonces, ya que no podemos evitar su creación, minimicemos más su capacidad aplicando una DLP de manera automática, para tener al menos controlado ese aspecto.

#Requisitos
- CoE Starter Kit instalado
- DLP configurada

# Instrucciones
1. Descargar el .zip de este repo
2. Importar en vuestro entorno con CoE Starter Kit
3. En la variable vDLPGuid indicar el id de la DLP que queramos asignar de manera automática a este tipo de entornos.
4. En la variable vMailTo indicar el contacto de correo para estar notificaciones de estos nuevos entornos.

![image](https://github.com/albertocastro365/Power-Automate/assets/57954993/6462e6cb-1926-4b53-903a-3edd608a5ebb)


