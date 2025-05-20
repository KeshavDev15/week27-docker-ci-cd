## Manual Installation
-Install Nodejs locally()
-Clone the repo
-Install dependencies(npm install)
-Start the DB locally
    -docker run -p 5432:5432 -e POSTGRES_PASSWORD=hello -d postgres
    -go to neon.tech and create a new database
-Change the database url in .env file
-npx prisma generate
-npx prisma migrate dev
-npm run build
-npm run start

## Docker Installation
-Install Docker
-Create a network - `docker network create user_project`
-Start Postgres
    -docker run --network user_project --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=hello -d postgres
-Build the docker image - `docker build --network=host -t user-project .`
-Run the docker image - `docker run -e DATABASE_URL=postgresql://postgres:hello@postgres:5432/postgres --network user_project -p 3000:3000 user-project`

## Docker-compose Installation
-Install Docker , Docker-compose
-Run `docker-compose up`

