postgresinit:
	docker run --name postgres-rtc -p 5433:5432 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=password -d postgres

postgres:
	docker exec -it postgres-rtc psql

createdb:
	docker exec -it postgres-rtc createdb --username=root --owner=root go-chat

dropdb:
	docker exec -it postgres-rtc dropdb go-chat

.PHONY: postgresinit postgres createdb dropdb