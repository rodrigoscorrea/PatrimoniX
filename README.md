# PatrimoniX

## Como instalar?

Faça o clone do repositório e preencha o .env conforme o .env.example.

### Para desenvolvimento

 Suba os conteineres com o seguinte comando:

```docker compose up --build -d```

Assim irá se criar toda a infraestrutura capaz de rodar a aplicação.

#### Como popular meu banco?

Após todos os containers estarem de pé, faça o comanndo para popular:

```docker exec -it backend_patrimonix npm run populate```

É ideal que o volume do banco de dados esteja zerado antes disso, para não dar o erro de primary key. As tabelas de Ativos, Transações e Usuários serão populadas.

### Apenas para uso

Use o arquivo de compose "docker-compose-with-images.yml" que carrega a última versão da branch main que foi adicionada ao DockerHub. 

Obs.: Não precisa fazer o --build dessa vez.

```docker compose -f .\docker-compose-with-images.yml up -d ```




