# Azure AI Search

#### Desafio:
O desafio propoe que seja criada uma pesquisa que funcione juntamente com um serviço de inteligência artificial para identificar palavras chave, sentimentos, utilizando também o serviço de armazenamento do azure.

- Passo 01: Dentro do portal da Azure, é necessário criar um novo recurso de Azure AI Search, para o nosso caso de uso, o plano Basic já funciona bem
- Passo 02: Dentro do portal da Azure, é necessário criar um novo recurso de Azure AI Service
- Passo 03: Dentro do portal da Azure, é necessário criar um storage, para armazenar os dados que iremos usar nas ferramentas de IA que foram criadas no passo 01 e 02
- Passo 04: Após a criação do recurso de storage, precisamos liberar o acesso anonimo para o blob, caso contrario a IA não irá ter acesso aos recursos que subiremos para consulta (SETTINGS => CONFIGURATION)
- Passo 05: Dentro do recurso de storage, vamos criar um container no menu lateral (DATA STORAGES => CONTAINERS), vamos subir os arquivos e adicionar as pesquisas que irão ser analisadas pelo AI Service
- Passo 06: Agora vamos importar e indexar os dados pelo recurso AI Search, dentro do recurso agora com o container criado, podemos acessar o submenu de Import Data e apontar para o container
- Passo 07: Após todas as configurações executadas, retornaremos ao AI Service, dentro da opção SEARCH EXPLORER, vamos testar as configs com o comando
  ```
  search=*&$count=true    (  verifica se a indexação esta funcionando e mostra os documentos )
  ```
- Passo 08: Podemos buscar agora que os dados estão corretos, os valores de acordo com o local por exemplo
  ```
  search=locations:'Chicago' ( Consulta as ocorrencias acontecidas em Chicado )  
  ```
- Passo 08: Vamos verificar os casos em que o sentimento é negativo
  ```
  search=sentiment:'negative' ( Consulta as ocorrencias com sentimento negativo )  
  ```
Obs: Os comandos acima precisam ser copiados sem os dados dentro dos parenteses.
