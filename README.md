Some usefull pg commands (just to help)
```
docker-compose run client
export PGPASSWORD=admin
for host in pg1 pg2 pg3; do echo "Host: ${host}"; psql -h ${host} -U admin postgres -c 'SELECT * FROM pg_is_in_recovery();'; done
leader=pg2
psql -h ${leader} -U admin postgres
for host in pg1 pg2 pg3; do echo "Host: ${host}"; psql -h ${host} -U admin postgres -c 'SELECT * FROM foo;'; done
```
