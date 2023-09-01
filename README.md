# Prova-2023-9-1
Avaliações do Módulo 7

Dockerhub com as imagens:
- Frontend: https://hub.docker.com/repository/docker/hallzero/frontend-prova/general
- Backend: https://hub.docker.com/repository/docker/hallzero/backend-prova/general

Os dockerfiles também podem ser encontrados respectivamente nas pastas frontend e backend.

Para rodar a aplicação:
- Clone este repositório, se ainda não o fez
- rode o comando:
```bash
docker compose up
```

## Escolha das imagens dos dockerfiles:

Imagem base para o backend: python:3.
Utilizei a imagem do python, especificamente sua versão 3, para rodar com estabilidade o backend. Basicamente, ela copia todos os arquivos dentro da pasta backend, instala as dependências encontradas em requirements.txt e roda o servidor na porta 8000.

Imagem base para o frontend: node-alpine.
Utilizei a imagem do node, especificamente a latest-alpine, pois é relativamente leve e atende à todas as demandas desse projeto. Basicamente, ela copia os arquivos package*.json, instala as dependências contidas nele utilizando o npm e depois roda utilizando Node.js na porta 3000.

## Explicação do Docker-compose

O docker compose basicamente utiliza as imagens dos repositórios no dockerhub como base dos serviços, que da mesma forma expõem as portas 3000 e 8000 para as aplicações e nomeia containers para tal. Neste caso, o container do frontend será "frontend-lindinho" e o backend será "backend-fofinho" 🐱.