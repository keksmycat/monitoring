# Deploy stack

1. Клонировать репозинорий
<p> git clone https://github.com/keksmycat/monitoring.git</p>
   
2. Деплой стека  
<p>   docker stack deploy -c monitoring/docker-compose.yml $Имя_стека</p>

3. Добавить 3 записи в  /var/lib/docker/volumes/($Имя_стека)_prom-configs/_data/prometheus.yml
   
<p> job_name: 'node-exporter'</p>

<p>	static_configs:</p>

<p>		- targets: ['node-exporter:9100']	</p>

   
