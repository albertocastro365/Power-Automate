
Tras la implementación de seguridad en el trigger "When a HTTP Request is received": https://powerautomate.microsoft.com/en-us/blog/deeper-control-over-http-invocation-of-flows/ este flow permite de manera sencilla listar todos los flows de nuestro tenant que usan ese trigger para poder avisar a los owners de que habiliten esta nueva seguridad.

# Requisitos
Rol Azure Power Platform Administrator o Global Admin

# Instrucciones
1. Descargar el .zip de este repo
2. Importar en vuestro entorno
3. Indicar el mail que recibirá el listado de flows en la variable 'vDestinatarioMail'


![image](https://github.com/albertocastro365/Power-Automate/assets/57954993/782a8159-92c6-40bb-bca8-c1200aa248b7)
