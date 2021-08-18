Setup the postgres
> docker-compose . up -d


username is : postgres
password is : Log@123

To connect to postgres
```
docker exec -it logger-pgres bash

psql -U postgres -p 5432 -W

```

execute queries
```
CREATE TABLE businesslogs_mock(
	id SERIAL PRIMARY KEY,
	user_name VARCHAR (255),
	message VARCHAR (500),
	class VARCHAR (255),
	priority VARCHAR (255),
	log_date timestamp without time zone
);


INSERT INTO businesslogs_mock (user_name,message,log_date)
VALUES ('user5','card successfully added :user5','2021-08-22');

```