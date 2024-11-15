FROM openjdk:8-jre

#MAINTAINER juliens@microsoft.com

RUN mkdir -p /usr/local/app

WORKDIR /usr/local/app
#copiar el .jar del servicio a la imagen
COPY drop/run.sh /usr/local/app/run.sh
COPY drop/*.jar /usr/local/app/

#cuando lancemos una pila de servicios con Docker, la ip de MongoDB no se puede
#descrubrir al menos que se la pasemos en un archivo de propiedades
COPY drop/application.properties application.properties

EXPOSE 8080

ENTRYPOINT ["sh", "/usr/local/app/run.sh"]