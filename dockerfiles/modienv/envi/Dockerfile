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
COPY web/ /app/web/
COPY api/ /app/api/

# Ejecutar según el ENV
CMD sh -c "if [ \"$servicio\" = \"web\" ]; then node web/app.js; else python3 api/app.py; fi"