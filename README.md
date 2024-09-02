# DESAFIO_PPOWER_BI_DIO
## DESAFIO 01
Primeiro desafio de projeto

Optei por diferentes cores nos dash para ficarem mais armoniozas e menos chocantes
optei por fundo escuro para não ficar tão pesado o fundo claro.

### DASHBOARD REFEITO 001

![image](https://github.com/user-attachments/assets/84dba35c-bafc-45a5-881c-808f1f637c46)

### DASHBOARD REFEITO 002

![image](https://github.com/user-attachments/assets/5ac98938-d1f9-4472-815c-0adac25f619f)

### DASHBOARD EFEITO 003

![image](https://github.com/user-attachments/assets/94567870-b243-4c8c-8bb6-b59259f0972b)

## DESAFIO 02

### DASHBOARD EFEITO 001

>[!note]
> optei por trocar o visual de disco por um de colunas porque alguns estudos demonstram que o visual de pizza pode ser mais confuso na validação de proporção dos dados.

![image](https://github.com/user-attachments/assets/4f347110-7fc7-4a11-bb46-d99412c3396a)

## DESAFIO 03

passo 1: configuração do Azure
passo 2: Popular servidor com script fornecido
passo 3: Integrar SQL com Power BI
passo 4: Realizado o passo Transformação do ETL 

![image](https://github.com/user-attachments/assets/2dc11931-3acb-4150-bdb8-b12010bec98b)

![image](https://github.com/user-attachments/assets/faffb4e7-56fe-47e4-b39c-947b4e70b95d)

Fluxo mostra como será o passo a passo para o projeto, além de que será necessário desenhar um relatório do passo a passo do processo.


#### O QUE FAZER?

Primeiramente todos trabalho será realizado em uma base de dados de teste. Em seguida será criado um relatório para verificar as informações.
* Criar instancia na Azure MySQL
* Criar banco de dados com dados disponiveis no git Hub
* Integrar PowerBi com MySQL
* Verificar problemas na Transformação

#### TRANSFORMAR DADOS

* Verificar cabeçalhos e tipos de dados
* Modificar valores monetários para tipos double
* Verificar valores Nulos e análise para remoção
* Os Employer com nulos em Super_snn podem ser gerentes verficiar se existe algum colaborador sem gerentes
* verificar se existe departamentos sem gerentes
* se houver departamento sem gerente, suponha que tenho dados e preencher lacunas
* verificar se existe numero de horas de projetos
* separar colunas complexas

* mesclar consultas employee e departamento para criar uma tabela employee com nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee.
* OBS: Fique atento, essa informação influencia no tipo de junção.
* Neste processo elimine as colunas desnecessárias

* Realizar a junção dos colaborador e respectivos nomes dos gerentes isso pode ser feito com consulta SQL ou pela mescla de tabelas com POWER BI caso utilize SQL, especifique no README a query utilizada no processo.
* Mesclar as colunas de nome e sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores.


##### 1. Criando conta no AZURE
![image](https://github.com/user-attachments/assets/f596b702-9861-4a53-b5d3-7d44a75d45f9)
![image](https://github.com/user-attachments/assets/2b609755-696c-42bf-9c45-981076d29520)

>[!alert]
>Tive algum problema no bash que meu comando travou eu tentei varias vezes sem sucesso

![image](https://github.com/user-attachments/assets/962fd661-7ad1-4452-8c9c-abcd09c2347b)

Após algumas tentativas descobir que o erro estava no protocolo SSL que precisava deabilitar na rede para conseguir a conexão

![image](https://github.com/user-attachments/assets/e6b7eef0-0592-4605-91cf-8611d4b5d5fd)

![image](https://github.com/user-attachments/assets/267b968b-85ff-45dd-954b-aff487a0b235)


Consegui conectar e realizar as querys no sql porém existiu alguns erros nas querys que não executaram pricipalmente no employee deu muito erro 
![image](https://github.com/user-attachments/assets/c9a29f85-fa6d-4b87-aebf-312fccb36c17)

Connectando ao PowerBI

![image](https://github.com/user-attachments/assets/35f4c714-6af8-45e8-a940-24c90ee6af1e)

dados connectados:
1. Verificar cabeçalhos e tipos de dados
![image](https://github.com/user-attachments/assets/4000ea7b-39ef-4dd3-8dc0-031ed08a5d4c)

2. Alterado tipos monetários para double

   ![image](https://github.com/user-attachments/assets/263e2b04-0fc7-46ef-a862-c7015fcd99ee)


3. Modificar valores monetários para tipos double
    ![image](https://github.com/user-attachments/assets/263e2b04-0fc7-46ef-a862-c7015fcd99ee)
   
4. Verificar valores Nulos e análise para remoção
   Somente 1 campo no sn employer estava null
   
5. Os Employer com nulos em Super_snn podem ser gerentes verficiar se existe algum colaborador sem gerentes

   Existe um colaborador sem gerente
  ![image](https://github.com/user-attachments/assets/c88ac784-e514-49d6-a677-7710efa816a4)

6. verificar se existe departamentos sem gerentes

   Não existem departamentos sem geretnes
   ![image](https://github.com/user-attachments/assets/20947ef9-9580-4a98-aac2-00ad74afd2ac)

7. se houver departamento sem gerente, suponha que tenho dados e preencher lacunas
    
8. verificar se existe numero de horas de projetos

    Existem numero de horas em work_on

    ![image](https://github.com/user-attachments/assets/ff52e739-c8a1-4296-8790-761c7279765b)

9. separar colunas complexas

    Colunas complexas como endereço foram separadas
    ![image](https://github.com/user-attachments/assets/aa002d68-a345-4862-9be0-f60cf3c03db7)


10. mesclar consultas employee e departamento para criar uma tabela employee com nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee.

    ![image](https://github.com/user-attachments/assets/800a58f3-2054-46b4-a40f-963044e13d20)


## DESAFIO 004 

### MODELO ESTRELA DE RELACIONAMENTo

Criado query sql para modelo strela no workbanch

![image](https://github.com/user-attachments/assets/c4f09f1a-a53a-4a1d-938d-a787af98989f)

QUERY

```sql

-- Criação do banco de dados
CREATE DATABASE StarSchemaDB;

-- Seleciona o banco de dados para uso
USE StarSchemaDB;

-- Criação das tabelas de dimensão
CREATE TABLE Date (
    DateID INT PRIMARY KEY,
    Date DATE NOT NULL,
    Year INT NOT NULL,
    Month INT NOT NULL,
    Day INT NOT NULL
);

CREATE TABLE Customer (
    CustomerID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100),
    PhoneNumber VARCHAR(15)
);

CREATE TABLE Product (
    ProductID INT PRIMARY KEY,
    ProductName VARCHAR(100) NOT NULL,
    Category VARCHAR(50) NOT NULL,
    Price DECIMAL(10, 2) NOT NULL
);

CREATE TABLE Store (
    StoreID INT PRIMARY KEY,
    StoreName VARCHAR(100) NOT NULL,
    Location VARCHAR(100) NOT NULL
);

CREATE TABLE Employee (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Position VARCHAR(50) NOT NULL
);

-- Criação da tabela de fatos
CREATE TABLE Sales (
    SaleID INT PRIMARY KEY,
    DateID INT,
    CustomerID INT,
    ProductID INT,
    StoreID INT,
    EmployeeID INT,
    Quantity INT NOT NULL,
    TotalAmount DECIMAL(10, 2) NOT NULL,
    FOREIGN KEY (DateID) REFERENCES Date(DateID),
    FOREIGN KEY (CustomerID) REFERENCES Customer(CustomerID),
    FOREIGN KEY (ProductID) REFERENCES Product(ProductID),
    FOREIGN KEY (StoreID) REFERENCES Store(StoreID),
    FOREIGN KEY (EmployeeID) REFERENCES Employee(EmployeeID)
);

```

Modelo relacionamento

![image](https://github.com/user-attachments/assets/9c7d22e9-d00b-4335-b011-858b458cd98d)


## DESAFIO 006 

Atraves da tabela Financial criar novas tabelas conforme o enunciado para produtos etc.

D_PRODUTO

primeiro extair os dados
![image](https://github.com/user-attachments/assets/a9d55029-d3df-4287-8e10-00b457cb3fcc)
Ajustando produtos
![image](https://github.com/user-attachments/assets/8bf3f47a-7231-41eb-92c0-47644e577da2)

Inserindo INDEX

![image](https://github.com/user-attachments/assets/1039f7f4-065b-4d9a-9dbb-d1a017af83f2)

D_DESCONTOS

Deletar colunas

![image](https://github.com/user-attachments/assets/199680aa-0b00-47fa-a5c7-59f48eb335fd)

![image](https://github.com/user-attachments/assets/76381db2-19b2-44e4-b0f2-9838d6d19008)

![image](https://github.com/user-attachments/assets/c21e3dd3-6b7a-416c-96e7-83343def4280)

![image](https://github.com/user-attachments/assets/9a0f119a-36d6-4c05-b814-4cd525d02823)


## DESAFIO 07

Nesse desafio optei por manter a ordem deixada pela instrutora porém decidi alter os fundos e as cores para ficarem mais fácil de ver uma vez que os tons claros cansam a visão.

![image](https://github.com/user-attachments/assets/ec04d466-2cf4-426b-979f-8b960645e932)

![image](https://github.com/user-attachments/assets/f29afc16-a0d3-498f-9804-63e66ad0fdea)

![image](https://github.com/user-attachments/assets/43b6067c-ff9f-4535-b0b3-27b95cac7f3d)



