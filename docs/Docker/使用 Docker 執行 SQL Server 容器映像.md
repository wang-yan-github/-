---
layout: post
---

**使用 Docker 執行 SQL Server 容器映像**

docker pull [mcr.microsoft.com/mssql/server:2017-latest](http://mcr.microsoft.com/mssql/server:2017-latest)

docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<YourStrong!Passw0rd>" `

  --name "sql1" -p 1433:1433 `

  -v sql1data:/var/opt/mssql `

  -d [mcr.microsoft.com/mssql/server:2017-latest](http://mcr.microsoft.com/mssql/server:2017-latest)

docker exec -it sql1 /opt/mssql-tools/bin/sqlcmd `

  -S localhost -U SA -P "<YourStrong!Passw0rd>" `

  -Q "ALTER LOGIN SA WITH PASSWORD='<YourNewStrong!Passw0rd>'"

docker exec -it sql1 mkdir /var/opt/mssql/backup

docker cp SDG.mdf sql1:/var/opt/mssql/backup

docker cp SDG_log.LDF sql1:/var/opt/mssql/backup

docker exec -it sql1 /opt/mssql-tools/bin/sqlcmd -S localhost `

  -U SA -P "<YourNewStrong!Passw0rd>" `

  -Q "EXEC sp_attach_db @dbname = 'SDG-ZZD', @filename1 = '/var/opt/mssql/backup/SDG.mdf', @filename2 = '/var/opt/mssql/backup/SDG_log.LDF'"

EXEC sp_attach_db @dbname = 'SDGZZD1', 

@filename1 = 'W:\software\BtSoft\sqlserver\Program Files\Microsoft SQL Server\MSSQL10_50.MSSQLSERVER\MSSQL\DATA\SDGZZD1.mdf', 

@filename2 = 'W:\software\BtSoft\sqlserver\Program Files\Microsoft SQL Server\MSSQL10_50.MSSQLSERVER\MSSQL\DATA\SDGZZD1_log.LDF'