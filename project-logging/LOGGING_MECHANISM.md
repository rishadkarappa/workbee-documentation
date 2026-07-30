Logging Mechanism - WorkBee 
ELK + Winston

WorkBee uses a centralized logging architecture to collect logs from all microservices into a single location. Every service writes logs using Winston. Logstash receives these logs, Elasticsearch stores and indexes them, and Kibana provides a web interface to search, filter, and visualize the logs.

This allows to monitor every service without opening multiple terminals.