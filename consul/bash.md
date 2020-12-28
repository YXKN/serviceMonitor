docker run -d --expose 9100 --name node-exporter --network sdt --ip 192.168.10.10 quay.io/prometheus/node-exporter
注意添加ip 为了consul 中能发现

docker run -p 8500:8500 -v /home/sdt/zwx/docker/serviceMonitor/consul/config:/consul/config -v /home/sdt/zwx/docker/serviceMonitor/consul/data:/consul/data --name consul --network sdt --ip 192.168.10.100 consul

注意
ip要与consul里面config中一致

docker run -d -p 9090:9090 -v /home/sdt/zwx/docker/serviceMonitor/prometheus.yml:/etc/prometheus/prometheus.yml --name prom --network sdt --ip 192.168.10.11 prom/prometheus
注意添加ip 为了consul 中能发现