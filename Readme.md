#Operation 1
## Services used
1. postgresql
2. pgadmin
3. Server (my application)
##Requirements
1. docker
2. docker-compose
3. docker buildx
##Commands
Folder in project - /scripts
1. Service assembly - bash build.sh
2. Start - bash start.sh
3. Stop - bash stop.sh
4. Destruction - bash down.sh
5. Restart - bash restart.sh
6. Receiving a volunteer token - bash volunteer_token_project.sh $1 $2 ($1 - localhost, $2 - 3001)
7. Add data - bash adding_data_project.sh $1 $2 $3 ($1 - localhost, $2 - 3001, $3 - volunteer_token from point 6)
8. Receiving a admin token - bash admin_token_project.sh $1 $2 ($1 - localhost, $2 - 3001)
9. Reading data - bash reading_data_project.sh $1 $2 $3 ($1 - localhost, $2 - 3001, $3 - admin_token from point 8)
##Steps
1. bash build.sh
2. bash start.sh
3. Open browser http://localhost:5050/browser/ (Email - admin@admin.com, Password - root)
4. Create server in pgadmin (Name - pg_serv, Host name - db, Port - 5432, Username - postgres, Password - postgres)
5. bash start.sh
6. bash volunteer_token_project.sh localhost 3001
7. bash adding_data_project.sh localhost 3001 volunteer_token
8. bash admin_token_project.sh localhost 3001
9. bash reading_data_project.sh localhost 3001 admin_token
10. bash stop.sh
