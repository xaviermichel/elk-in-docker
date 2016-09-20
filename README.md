ELK stack in docker
===================

Just use `docker-compose` to start the ELK stack :
```bash
cd /vagrant
docker-compose up
```

_Note :_ you may have to run `sudo sysctl -w vm.max_map_count=262144` before booting elastic with docker (https://github.com/docker-library/elasticsearch/issues/98#issuecomment-218071315)

And if you wanna inject more logs, you can use logstash tcp handler (on the host) :
```bash
cd /vagrant/logs
cat simple_data_search.log | nc 127.0.0.1 5000
```

And you can open your brower on `127.0.0.1:5691` !

