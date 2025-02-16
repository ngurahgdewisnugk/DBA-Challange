# Challange : Create a Database 
![image](https://github.com/user-attachments/assets/7139c854-4dbb-422a-a73b-f463bffc8819)
1. Create A New Container
   ```
   docker run --name kineteco -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=NgurahWisnu134" -p 1411:1433 -d mcr.microsoft.com/mssql/server:2019-latest
   ```
   ![image](https://github.com/user-attachments/assets/6ad1cc20-c3ed-42a6-b818-24b2405d9f9d)

2. Connect To Microsoft SQL Database with **Dbeaver**
   ![image](https://github.com/user-attachments/assets/7329d68c-f509-460e-8c9d-b7514328112a)
3. Open Sql Script Editor
   ![image](https://github.com/user-attachments/assets/a293bec8-784e-4ab1-9c0b-0d379a9f1ac2)
4. Create the Database Query
   ```
   CREATE DATABASE KinetEco;
   ```
   ![image](https://github.com/user-attachments/assets/03b1a34c-181d-460b-a3ce-d55649c5d61d)
