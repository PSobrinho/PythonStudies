# **Analise exploratória e Visualização de dados**

Pedro H. N. Sobrinho (PSobrinho)

Mail: pedrosobrinho.physics@gmail.com

LinkedIn: https://www.linkedin.com/in/pedro-sobrinho-b84879108/

Instagram: https://www.instagram.com/phnsobrinho/?hl=pt-br

O desenvolvimento a aqui apresentado tem como objetivo estudar a análise, exploração e visualização de dados utilizando 
recursos PyDataStack. Sendo os produtos deste estudo abertos para consulta e estudo por terceiros :)

# **Sobre os dados utilizados**

A base de dados original foi obtida no Kaggle: https://www.kaggle.com/orgesleka/used-cars-database. E consiste de dados coletados do Ebay Alemão sobre carros usaos a venda, contendo:

*   dateCrawled : Quando os dados foram coletados;

*   name : "nome" do carro;

*   seller : se o vendedor é um usuário privado, ou revendedor;

*   offerType;

*   price : o preço anunciado para o carro;

*   abtest;

*   vehicleType;

*   yearOfRegistration : ano em que cada carro foi registrado pela primeira vez;

*   gearbox: tipos de caixa de câmbio;

*   powerPS : Potência do carro em cavalos (PS);

*   model;

*   kilometer : quantos quilometros o carro já rodou;

*   monthOfRegistration : em qual mês o carro foi registrado pela primeira vez;

*   fuelType;

*   brand;

*   notRepairedDamage : possíveis problemas não reparados no veículo;

*   dateCreated : a data que o anuncio foi criado;

*   nrOfPictures : numero de fotos no anuncio (devido a erros de coleta, temos muitos cambos com 0).

*   postalCode;

*   lastSeen : a última vez que o anuncio foi visto online pelo mecanismo de coleta.

O arquivo original foi importado para um DB Postgres, por meio do seguinte procedimento:
* Leitura do script SQL 'usedCars.sql' (disponível na página do projeto) via shell para criação da tabela com os campos descritos anteriormente;
* cópia dos dados do arquivo .csv via shell por meio do camando COPY.

Daí foram extraidos, via queries, diferentes dataframes menores com as informações pertinentes para cada ponto da análise. Um arquivo adicional contendo a conexão com o banco de dados e a produção dos datasets esta disponível no arquivo 'sql_db_connection_result_sets.ipynb'. Os arquivos para cada etapa são:

* **Distribuição de veículos com base no ano de registro**: df1_yearcount.csv;
* **Variações de faixa de preço pelo tipo de veículo**: df2_vehicleprice.csv;
* **Contagem total de veículos à venda conforme tipo de veículo**: df3_vehiclecount.csv;
* **Nº de veículos por marcas**: df4_brandcount.csv;
* **Preço médio com base no tipo de veículo, bem como no tipo de caixa de câmbio**: df5_vehicle_gearbox_price.csv;
* **Preço médio do veículo por tipo de combustível e caixa de câmbio**: df6_fueltype_gearbox_price.csv;
* **Potência Média por tipo de veículo e caixa de câmbio**: df7_vehicle_gearbox_price.csv.

