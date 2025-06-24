# n8n docker Setup

docker volume create n8n_data

docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n

docker exec -it n8n-docker-postgres-1 psql -U xuser -d n8n

docker exec -it n8n-docker-postgres-1 psql -U root -d n8n
