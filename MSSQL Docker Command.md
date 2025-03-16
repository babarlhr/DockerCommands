```
docker volume create sqlserver_data
```

```
docker volume inspect sqlserver_data
```

```
docker volume ls
```

Docker VOLUME IS inside docker WSL filesystem 

```
\\wsl.localhost\
```

```
\\wsl.localhost\docker-desktop
```


```
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=devdb456" ` 
   -e "MSSQL_PID=Express" `
   -p 1433:1433 --name SQLEXPRESS --hostname SQLEXPRESS `
   -v E:\EFFSDBBackup:/var/opt/mssql/backups `
   -v sqlserver_data:/var/opt/mssql `
   -d mcr.microsoft.com/mssql/server:2022-latest
```

   
