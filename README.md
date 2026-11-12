# YZS-HEALTHCORE
## 1. Descripción del proyecto
**YZS HealthCore** es una empresa tecnológica orientada a clínicas privadas.El propósito es diseñar, implantar y mantener la infraestructura informática segura, segmentada y automatizada para almacenar, proteger y facilitar el acceso autorizado a los datos procedentes de plataformas y chips de monitorización de pacientes. 


## 2. Objetivo de la infraestructura
Garantizar una base tecnológica fiable y protegida para el entorno clínico mediante:
* **Aislamiento y seguridad perimetral** mediante la segmentación de redes y el uso de un firewall OPNsense.
* **Despliegue automatizado e idempotente** de los servicios utilizando Ansible, Bash y Docker.
* **Disponibilidad y recuperación** aseguradas mediante monitorización continua (Prometheus y Grafana) y copias de seguridad verificadas (Borg Backup).


## 3. Stack Tecnológico Utilizado
* **Virtualización y Contenedores:** Oracle VirtualBox y Docker Engine.
* **Sistema Operativo:** Debian 13.
* **Servidor Web y Base de Datos:** Apache HTTP Server (con soporte TLS/SSL) y MySQL Community Server.
* **Seguridad y Redes:** OPNsense (Firewall).
* **Automatización y Control de Versiones:** Ansible, Bash y Git.
* **Monitorización y Copias de Seguridad:** Prometheus, Grafana OSS y Borg Backup.


## 4. Estructura del repositorio
* `inventario/`: Contiene los ficheros de hosts (`hosts.ini`) con la distribución de las máquinas virtuales del laboratorio.
* `playbooks/`: Playbook orquestador principal (`site.yml`).
* `roles/`: Módulos de Ansible divididos por componentes (`firewall`, `web_apache`, `bd_mysql`, `docker_servicios`, `monitorizacion`, `backups_borg`, `seguridad_ssh`).
* `variables/`: Archivos de configuración de red y credenciales protegidas con Ansible Vault (`vault.yml`).
* `plantillas/`: Ficheros de configuración en formato Jinja2 para Apache y scripts de respaldo.
* `documentacion/`: Memorias, análisis de requisitos, manuales de identidad y documentación técnica del proyecto.
