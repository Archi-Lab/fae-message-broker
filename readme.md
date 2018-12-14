# Kafka Message Broker

Dies ist der Message Broker für das Projekt "GPS-Schuhsohle".
Der Broker wird per Docker gestartet. Hierzu muss der folgendene Befehl ausgeführt werden.
```bash
docker-compose -f ./docker-compose.yml up
```

Zum stoppen des Message Brokers muss der nachstehende Befehl genutzt werden.
```bash
docker-compose -f ./docker-compose.yml down
```

Damit ein beliebiger Service mit dem Messagebroker kommunizieren kann, muss dieser in das Docker-Netzwerk dieses Projekts beitreten. 
Hierzu sollte im Docker-compose des eigenen Projekts das Netzwerk "kafka-broker_backend" für einen Service angegeben und als external konfiguriert werden. 
Nähere Infos unter: [Docker Networking](https://docs.docker.com/compose/networking/) oder in dem Projekt [fae-draussen-ortung](https://github.com/Archi-Lab/fae-draussen-ortung)
