# Connect oracle through docker 

```Docker command
    docker volume create my_data_volume

    docker run -d \
  --name oracle-db \
  -p 1521:1521 \
  -p 5500:5500 \
  -e ORACLE_PASSWORD=admin123 \
  -v oracle_clg:/opt/oracle/oradata \
  gvenzl/oracle-free:latest

    docker ps

    // Connect sql
    docker exec -it container_name sqlplus system/password@
    docker exec -it oracle-db sqlplus system/admin123@FREEPDB1

    FREEPDB1 - the default Pluggable Database name inside the container


    
```


```SQL Command
conn sys as sysdba
password

conn hr/hr;

grant all privilages to hr;

SHOW USER;

Create user username indentified by password;


```




