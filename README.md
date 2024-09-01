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






