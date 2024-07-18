![Pihole Banner](./img/pihole.png)

# 🕳️ PiHole Docker Container

Este proyecto proporciona una configuración optimizada para ejecutar PiHole dentro de un contenedor Docker. PiHole es un bloqueador de anuncios a nivel de red que actúa como un servidor DNS sinkhole y mejora la experiencia de navegación al eliminar anuncios y rastreadores.

## 📝 Descripción

Este repositorio contiene todo lo necesario para poner en marcha tu propio servidor PiHole utilizando Docker. La configuración está diseñada para ser fácil de usar y personalizar según tus necesidades.

## 📦 Contenido del Repositorio

- **docker-compose.yml**: Archivo de configuración para Docker Compose.
- **scripts/**: Carpeta que contiene scripts útiles para la configuración y mantenimiento del contenedor.
  - **setup.sh**: Script para instalar y configurar PiHole.
- **.env.example**: Archivo de configuración de ejemplo para las variables de entorno.

## 🏃‍♂️ Iniciar el Servidor PiHole

Sigue estos pasos para poner en marcha tu servidor PiHole utilizando Docker Compose:

1. Desde tu terminal, asegúrate de estar en el directorio principal del repositorio clonado:

```sh
cd ruta/a/la/carpeta/pihole-server
```

2. Ejecuta el siguiente comando para iniciar PiHole en segundo plano:

```sh
docker-compose up -d
```

Este comando iniciará el contenedor de PiHole y lo pondrá en funcionamiento.

3. Verifica el estado del servidor para asegurarte de que esté ejecutándose correctamente:

```sh
docker-compose ps
```

Este comando te mostrará el estado del contenedor y confirmará que está en funcionamiento.

## ⚙️ Configuración

A continuación se presenta una tabla con las variables de entorno disponibles en docker-compose.yml que puedes ajustar según tus necesidades en el archivo `.env`:

| Variable      | Valor por defecto | Descripción                                |
| ------------- | ----------------- | ------------------------------------------ |
| `TZ`          | "Europe/Madrid"   | Zona horaria del contenedor.               |
| `WEBPASSWORD` | ""                | Contraseña para la interfaz web de PiHole. |
| `DNS1`        | "1.1.1.1"         | Servidor DNS primario.                     |
| `DNS2`        | "1.0.0.1"         | Servidor DNS secundario.                   |
| `ServerIP`    | "0.0.0.0"         | IP del servidor PiHole.                    |

Para más detalles sobre la configuración de PiHole en Docker, consulta la documentación oficial de PiHole en Docker.

## ➕ Scripts Útiles

En la carpeta scripts, encontrarás varios scripts útiles para la administración de tu servidor PiHole. Por ejemplo, setup.sh puede ser utilizado para instalar y configurar PiHole rápidamente.

## 📜 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

## 👤 Autor

- Nombre: Javier Plaza Sisqués
- GitHub: [JSisques](https://github.com/JSisques)

## 🗃️ Referencias

- Imagen en Docker Hub: [pihole/pihole](pihole/pihole)
- Documentación oficial de PiHole: [https://docs.pi-hole.net/](https://docs.pi-hole.net/)
- Repositorio original: [https://github.com/pi-hole/pi-hole](https://github.com/pi-hole/pi-hole)
