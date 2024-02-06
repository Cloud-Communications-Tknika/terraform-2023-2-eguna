# terraform-2023-2-eguna



En este ejercicio repasaremos los conceptos vistos hasta ahora y levantaremos una infraestructura mediante Terraform.

Para ello, levantaremos una VPC que contenga una subred pública con acceso a internet. Dentro de esta subred levantaremos una máquina que tenga instalado un sevidor de Apache.

## Enunciado

Desarrolla:

Define la siguiente infraestructura para AWS utilizando Terraform:

* Crea una VPC que contenga las IPs 10.0.0.0/16, y dentro de ella una subred pública con un CIDR 10.0.100.0/24. Esta subred debe tener acceso a internet y desde internet se debe tener acceso a esta subred.
* Dentro de dicha subred debe existir un EC2 al que solo se puede acceder mediante SSH, HTTP y HTTPS (puertos 22, 80 y 443).

Comprueba:

Para comprobar que el ejercicio esta bien, nos conectaremos vía ssh y ejecutaremos:

```bash
sudo apt update && sudo apt install -y apache2
```

Posteriormente entraremos en el navegador, escribiendo la IP del recurso y comprobaremos que aparece la página de inicio de apache.
