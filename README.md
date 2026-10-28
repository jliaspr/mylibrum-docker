# mylibrum-docker

Sistema de bibliotecas Librum com backend em Java/Spring Boot, frontend em Angular e banco PostgreSQL, reunidos para execução com Docker Compose.

## Executar

Com o Docker em execução:

```powershell
git clone https://github.com/jliaspr/mylibrum-docker.git
cd mylibrum-docker
docker compose -f BACK/mylibrum/docker-compose.yml up -d --build
```

- Frontend: http://localhost:4200
- Backend: http://localhost:8080
- Swagger: http://localhost:8080/swagger-ui/index.html
- PostgreSQL: localhost:5433

O banco mantém os dados em um volume Docker. As portas e credenciais de desenvolvimento podem ser ajustadas pelas variáveis definidas em `BACK/mylibrum/docker-compose.yml`.

Para parar os serviços:

```powershell
docker compose -f BACK/mylibrum/docker-compose.yml down
```

## Estrutura

- `BACK/mylibrum`: API, migrations, testes e configuração do Docker Compose.
- `FRONT/Librum`: aplicação Angular e configuração do Nginx.
- `BACK/README.md`: documentação da API, permissões e usuários de teste.

Os serviços usam configurações de desenvolvimento. Defina suas próprias credenciais e a variável `JWT_SECRET` antes de executar em produção.
