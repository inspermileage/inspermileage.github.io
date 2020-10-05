# Backend do carro
<hr> 



##### **Repositório** : <https://github.com/inspermileage/backend>

<br>

## Sobre o Backend

<p align="justify">  Nosso Backend é responsável por armazenar todos os dados que são enviados do arduino para o nosso [App](https://inspermileage.github.io/App/). Esses dados serão a base para a nossa Dashboard para a equipe, podendo analisar o desempenho do carro durante a corrida e realizar análises de melhorias e procuras de falhas no veículo. 
</p>
###### ** Organização de Pastas**


- schemas: contém os argumentos de entrada e saida (response models) das tabelas em cada rota.
- models: determina o tipo e o nome de cada tabela
- crud: segundo sua sigla, o crud é responsável pela: Create (Criação), Read (Consulta), Update (Atualização) e Delete (Destruição) de cada linha das tabelas.
- api: cria as rotas de cada tabela e 'linka' ela à uma função do crud.
- core: configura a url do database (antigamente PostgreSQL, mas agora não está sendo utilizada pelo fato do Backend salvar no proprio Heroku).
- database: realiza a conexão do database com o Backend.

###### ** Tabelas**

- car: informações básicas do carro, como nome do carro, descrição e data de criação
- track: informações básicas sobre a pista, como nome da pista e descrição
- round: informações sobre a corrida, como a data da corrida, razão (competição, teste ou inspeção), além das Foreign Keys do carro e da pista, informando o carro que irá correr e em qual pista.
- telemetry: tabela responsável por armazenar os dados do carro, como (rpm, velocidade etc).

###### ** Rotas da aplicação**
Com o servidor de FastAPI executando e conectado ao banco de dados, a documentação das rotas é apresentada em: localhost:8000/docs.

A rota base da API é dada por localhost:8000/api/.

###### ** Testes**
Os testes de unidade presentes na pasta /teste podem ser verificados pelo seguinte comando:

- `pipenv run pytest` 

## Dependências

Para realizar essa parte do projeto é necessário instalar:

- Obrigatórios: [Python 3.6 (ou superior)](https://www.python.org/downloads/), pipenv
 (`pip install pipenv`) e [PostgreSQL](https://www.postgresql.org/download/)
- Opcionais: [Docker](https://www.docker.com/products/docker-desktop) e 
[Docker Compose](https://docs.docker.com/compose/install/)


## Executando

### Ambiente virtual
Após instalar os requerimentos obrigatórios, é necessário instalar as dependências do projeto. Para isso execute, no terminal, na pasta *./backend*, onde se 
encontra o arquivo *Pipfile*, o seguinte comando: 
- `pipenv install --dev`

Para utilizar este ambiente, é preciso ativá-lo executando o comando:
- `pipenv shell`

### Ativando
- `pipenv run python main.py` (Certifique-se que o ambiente virtual está sendo utilizado)