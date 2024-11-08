FROM mongo:3.4

#MAINTAINER juliens@microsoft.com

COPY drop/* usr/local/data/db/

#es como Entrypoint, pero CMD se puede sobreescribir con otro comando al ejecutar el contenedor
CMD ["mongod", "--smallfiles", "--rest"]