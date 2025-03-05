## Manual installation
 - Install nodejs locally ()
 - Clone the repo
 - Install dependencies (npm install)
 - Start db locally
    - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
 - Change the .env file and update your db credentials
 - npx prisma generate
 - npx prisma migrate
 - npm run  build
 - npm run start

 ## Docker installation
  - Install docker 
  - Create network - docker network create user_project
  - Start postgres
    - docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
  - Build the image - `docker build --network=host -t user-project .`
  - Start the image - `docker run -e DATABASE_URL=postgresql://postgres:mysecretpassword@postgres:5432/postgres --network user_project -p 3000:3000 user_project .`

  ## Docker Installation 
   - Install docker, docker-compose
   - Run `docker-compose up`
