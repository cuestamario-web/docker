FROM alpine

# ARG (build)
ARG servicio=web

# ENV (runtime)
ENV servicio=$servicio

# Instalar dependencias
RUN apk add --no-cache nodejs python3

# Carpeta de trabajo
WORKDIR /app

# Copiar según el ARG
COPY ${servicio}/ /app/

# Ejecutar según el ENV
CMD sh -c "if [ \"$servicio\" = \"web\" ]; then node app.js; else python3 app.py; fi"