### Dump database:
* Dump all (with metadata):
```
docker-compose exec -T postgres-svc pg_dumpall -c -U mymadmin -d mym-db | gzip > dump_`date +%d-%m-%Y"_"%H_%M_%S`.gz
```
* Dump specific db:
```
docker-compose exec -T postgres-svc pg_dump mym-db -c -U mymadmin | gzip > dump_`date +%d-%m-%Y"_"%H_%M_%S`.gz
```
