# go-api-sqlserver template

You can connect sqlserver by xorm

## prepare

install mysql
- start local mysql(port is 1435)
- create sqlserver database handerly named `fruit`

```bash
docker run --rm -e ACCEPT_EULA=Y -e MSSQL_SA_PASSWORD=Eland123 -e MSSQL_PID=Developer -p 1435:1433 registry.p2shop.com.cn/mssql-server-linux

```

### run test
```bash
$ cd $GOPATH/src/go-api-sqlserver
$ go test -p 1 -count 1 -v ./...
```

## connect string

```yml
database:
  driver: mssql
  connection: driver={sql server};server=127.0.0.1;user id=sa;password=Eland123;database=fruit;port=1435
```




