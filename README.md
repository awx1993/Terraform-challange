# Terraform-challange
Terraform challange 1


# Máquina Virtual en Azure con Terraform #

A continuación te presento una implementación completa para crear una máquina virtual en Azure usando Terraform, con todas las características solicitadas:
** Estructura de archivos **

<img width="251" alt="image" src="https://github.com/user-attachments/assets/4a3a7f42-4932-41de-9c7b-9cd42ba08888" />

** Archivos Terraform  **
1. backend.tf (Almacenamiento remoto del estado)
   
<img width="373" alt="image" src="https://github.com/user-attachments/assets/b5a8ca55-b621-453b-a7cf-d1c5ce13306a" />

2. variables.tf (Definición de variables)


   <img width="365" alt="image" src="https://github.com/user-attachments/assets/5347850b-5ec4-4fa3-a20c-04389085d42f" />

3  terraform.tfvars (Valores de las variables)


<img width="388" alt="image" src="https://github.com/user-attachments/assets/7559ab54-4c7f-4bd2-9bc4-bfb52e0c584d" />

4.4. main.tf (Configuración principal)


<img width="310" alt="image" src="https://github.com/user-attachments/assets/a6e87403-605a-474c-94bd-1f285072478b" />

5.outputs.tf (Salidas)

<img width="326" alt="image" src="https://github.com/user-attachments/assets/0c3c23a0-68e1-4add-a4ee-13583f325506" />

# Instrucciones de uso
1.Configuración inicial:
Asegúrate de tener Terraform instalado
Inicia sesión en Azure CLI (az login)

2.Personaliza los valores:
Modifica terraform.tfvars con tus valores específicos
Para contraseñas seguras, considera usar Azure Key Vault o variables de entorno
3.Inicializa Terraform:
terraform init
4.Revisa el plan:
terraform plan
5.Aplica los cambios:
terraform apply

# Recomendaciones de seguridad
1. Para contraseñas:
No almacenes contraseñas en archivos de configuración
Usa Azure Key Vault o variables de entorno:

<img width="328" alt="image" src="https://github.com/user-attachments/assets/ed5b5330-0a41-4ed3-903c-dcf2ba786d7f" />

Luego proporciona el valor mediante:
terraform apply -var="admin_password=$SECURE_PASSWORD"

2.Backend remoto:
Asegúrate de que la cuenta de almacenamiento para el backend exista previamente

Configura el bloqueo en el contenedor de almacenamiento para evitar conflictos

3.Módulos:
Para proyectos más grandes, considera organizar el código en módulos



