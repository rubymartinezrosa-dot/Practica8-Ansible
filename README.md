# Práctica 8: Automatización de servidores con Ansible y Docker

## Descripción

En esta práctica se utiliza Ansible para automatizar tareas de administración en cinco servidores virtuales Ubuntu, creados mediante Docker.

El objetivo es aprender a configurar varios servidores desde un solo equipo, utilizando playbooks para ejecutar tareas automáticamente.

## Herramientas utilizadas

- Docker y Docker Compose
- Ubuntu mediante WSL
- Ansible
- Git y GitHub

## Tareas automatizadas

1. Actualizar la lista de paquetes de APT.
2. Crear el usuario itla en cada servidor.
3. Crear la carpeta /app.
4. Crear el archivo /app/hola.txt.
5. Instalar cowsay y htop en cada servidor.

## Estructura del proyecto

- Dockerfile
- docker-compose.yml
- inventory.ini
- ansible.cfg
- playbooks/01-actualizar.yml
- playbooks/02-configurar-servidores.yml

## Ejecución

Iniciar los servidores:

    docker compose up -d --build

Comprobar la conexión:

    ansible all -m ping

Ejecutar la actualización:

    ansible-playbook playbooks/01-actualizar.yml

Ejecutar la configuración:

    ansible-playbook playbooks/02-configurar-servidores.yml

## Resultado

Se logró automatizar la actualización y configuración de cinco servidores Ubuntu mediante Ansible y Docker.

## Autora

Ruby Martínez

Instituto Tecnológico de las Américas (ITLA)

