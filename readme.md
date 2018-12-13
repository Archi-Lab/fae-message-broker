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

Damit ein belieber Service mit dem Messagebroker kommunizieren kann muss dieser in das Docker-Netzwerk beitreten. 
Hierzu sollte im Docker-compose das Netzwerk "backend" für einen Service angegeben werden. 
Nähere Infos unter: [Docker Networking](https://docs.docker.com/compose/networking/)