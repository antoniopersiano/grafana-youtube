# grafana-youtube

RUN Grafana and Prometheus with docker-compose on Linux

1. Create a folder to run docker .yaml file in - mkdir grafana-docker-compose
2. Create volumes folder in /grafana-docker-compose/ 
mkdir /home/antonio/grafana-docker-compose/volumes/
mkdir /home/antonio/grafana-docker-compose/volumes/prometheus-config
mkdir /home/antonio/grafana-docker-compose/volumes/prometheus-data

3. Create a .yml file for prometheus
touch /home/antonio/grafana-docker-compose/volumes/prometheus-config/prometheus.yml

4. Change ownership
chown -R 65534:65534 /home/antonio/grafana-docker-compose/volumes/prometheus-data
chown -R 65534:65534 /home/antonio/grafana-docker-compose/volumes/prometheus-config
chmod -R 775 /home/antonio/grafana-docker-compose/volumes/prometheus-data
chmod -R 775 /home/antonio/grafana-docker-compose/volumes/prometheus-config

5. In your root docker folder download docker-compose.yaml from github
6. in docker root folder where you have the docker-compose.yaml run "docker-compose up" if you can load grafana and prometheus then you can now run it in daemon mode ie "docker-compose -d up" 
