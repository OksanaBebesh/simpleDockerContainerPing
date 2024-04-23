docker-compose up --build -d
docker ps
docker exec -it <container1_name> ping <container2_name>

-----------------------------------------------------------

docker run -d --name container1 nginx:alpine
docker run -d --name container2 nginx:alpine

docker network create myNetwork

docker network connect myNetwork container1
docker network connect myNetwork container2

docker exec -ti web1 ping web2