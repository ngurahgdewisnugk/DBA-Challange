## Challenge: Create a server container 

![image](https://github.com/user-attachments/assets/b47d9e3a-64fe-4307-b494-7c7fba84f528)

1. Create A new RDBMS container with PostgreSQL
   ```
   docker run --name TestPostgreSQL -p 5402:5432 -e POSTGRES_PASSWORD=JktB@li234 -d postgres
   ```
   ![image](https://github.com/user-attachments/assets/0eae6fca-5c1c-4215-bc24-dfe85dc1dc48)
2. view all running containers
   ```
   docker ps
   ```
   ![image](https://github.com/user-attachments/assets/941e29c4-c871-4237-a068-5a180215c961)
3. view all containers regardless of status
   ```
   docker ps -a 
   ```
   ![image](https://github.com/user-attachments/assets/b149f3ac-1104-4ed4-b67f-0dc0fc4060c1)
4. stop a container
   ```
   docker stop <container_name>
   ```
   ![image](https://github.com/user-attachments/assets/95ec2675-4af9-441a-8572-81284cfb1574)
   ![image](https://github.com/user-attachments/assets/239865ad-a43f-485c-889c-f5a5e2de3161)
5. start a container
   ```
   docker start <container_name>
   ```
   ![image](https://github.com/user-attachments/assets/a32a7f04-356c-4c11-b2c3-8f5c5fe7b148)
6. remove a container
   ```
   docker rm <container_name>
   ```
   ![image](https://github.com/user-attachments/assets/da623682-93e3-4817-b096-6087389dd1c5)
