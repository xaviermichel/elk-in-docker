Docker ELK stack
================

Just use docker-compose to start the ELK stack :
```bash
cd /vagrant
docker-compose up
```

And if you wanna inject more logs, you can use logstash tcp handler (on the host) :
```bash
cd /vagrant/tests_logs
cat simple_data_search.log | nc 127.0.0.1 5000
```
