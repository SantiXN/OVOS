
# Task 1
docker build . -t 2048-game:master
docker run -d -p 8080:8080 --name 2048-game1 2048-game:master
docker run -d -p 8081:8080 --name 2048-game2 2048-game:master

docker stop 2048-game1 && docker rm 2048-game1
docker stop 2048-game2 && docker rm 2048-game2

# Task 2
docker compose up --build -d
docker compose down

# Screencast
https://drive.google.com/drive/folders/1LixzFVLYu2THgHaxypHzTGlgHax1uvsW?usp=sharing