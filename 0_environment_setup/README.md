# Preparación del entorno y requerimientos del proyecto

## 1. Google Cloud: Proyecto y Credenciales
Debemos dirigirnos a [Google Cloud](https://console.cloud.google.com/) y crear un nuevo proyecto con el nombre de nuestra preferencia. Vamos a encontrar en nuestras notificaciones la opción de ingresar a nuestro nuevo proyecto.  
![Nuevo proyecto](./img/new_project.png)

En la pantalla de inicio podemos encontrar nuestro project ID. Esta identificación nos va a ser muy útil en los próximos pasos.

En el panel izquierdo buscamos el submenú de ```IAM & Admin``` y seleccionamos la opción ```Service Accounts```.  
En el borde superior podemos encontrar la opción de ```CREATE SERVICE ACCOUNT```. Definimos el nombre y la descripción del servicio.  
En el punto 2 definimos los siguientes roles: ```Basic > Viewer```, ```Storage Admin```, ```Storage Object Admin```, ```BigQuery Admin```.  
![Roles del servicio](./img/service_permissions.png)

En el menu Actions de nuestra lista de servicios seleccionamos la opción ```Manage Keys```. Luego creamos una Key en formato JSON y la guardamos en esta misma carpeta con el nombre ```iam_service.key.json```.

## 2. Activar APIs
En el panel izquierdo buscamos el submenú de ```APIs & Services``` y seleccionamos la opción ```Library```.  
En el buscador activamos ```Identity and Access Management (IAM) API``` y ```IAM Service Account Credentials API```

## 3. Instalar Google SDK y autenticación
Según tu sistema operativo podés instalar el CLI de Google Cloud desde la [documentación oficial](https://cloud.google.com/sdk/docs/install-sdk).  
Una vez instalado, es necesario crear una variable con nuestra key y loggearnos:
```linux
export GOOGLE_APPLICATION_CREDENTIALS=./0_environment_setup/iam_service.key.json
gcloud auth application-default login
```
Confirmamos con ```y```
![Mensaje de autenticación](./img/sdk_authenticate.png)

En el caso en que estés usando tu sistema operativo normal, se abrirá tu navegador para que confirmes la autenticación con tu cuenta de google. Si estás usando una terminal remota o sin acceso a un sistema operativo, recibirás un link que debes abrir para confirmar la autenticación y también un código que debes colocar en la terminal.

## 4. Instalar Terraform
Según nuestro sistema operativo, seguimos las instrucciones en la [documentación oficial de Terraform](https://developer.hashicorp.com/terraform/downloads).  
De todas maneras, siempre podemos descargar el binario para nuestro SO y agregarlo en una carpeta de nuestra variable PATH