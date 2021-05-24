# Guide-Run-MSSQL-Server-on-M1-Mac
Guide on Running a Local SQL Server on Your M1 Mac

## Instructions

1. Download [Docker for M1 Mac](https://docs.docker.com/docker-for-mac/apple-silicon/)
2. Download [Microsoft Azure SQL](https://hub.docker.com/_/microsoft-azure-sql-edge)
3. Open Docker, then open Terminal and run `docker run -e "ACCEPT_EULA=1" -e "MSSQL_SA_PASSWORD=MyPass@word" -e "MSSQL_PID=Developer" -e "MSSQL_USER=SA" -p 1433:1433 -d --name=sql mcr.microsoft.com/azure-sql-edge`
4. You should see a container running in Docker like in fig. 1
5. In your preferred IDE, set the server/host to `127.0.0.1`, the port to `1433`, and use `SA` for the username and `MyPass@word` for the password
6. Connect to the database fig. 2

fig. 1

<img width="758" alt="Screen Shot 2021-05-23 at 12 52 40 PM" src="https://user-images.githubusercontent.com/51058259/119272946-d7e51c80-bbc5-11eb-9c57-c8cb8dc3fa71.png">

fig. 2

<img width="1078" alt="Screen Shot 2021-05-23 at 12 50 21 PM" src="https://user-images.githubusercontent.com/51058259/119272870-7755df80-bbc5-11eb-9eaa-d33366834165.png">

