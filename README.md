<h1 align="center"> Tutorial_NoSQL <h1>

### 1. Antes de tudo
Antes da gente mergulhar nos conceitos sobre Banco de dados não relacional e MongoDB. Gostaria de aconselhar a leitura deste artigo da Medium, que fala sobre as diferenças entre famoso SQL e NoSQL. Após a leitura, volte aqui e vamos descobrir juntos o funcionamento dessa ferramenta poderosa :heart:
<p> Basta clicar neste link -> https://medium.com/devtranslate/diferencas-entre-sql-e-nosql-51311f9069bd </p>

### 2. Quase lá, apenas algumas cusiosidades

* O Shell do Mongo é escrito em JavaScript
* O mongo Utiliza a Sintaxe do Json (Não conhece? Ta aí um Artigo da DevMedia: https://www.devmedia.com.br/o-que-e-json/23166)

### 3. Agora é NoSQL e Mongo

Sabendo das diferenças e de algumas curiosidades, podemos finalmente conhecer os comandos do nosso mais novo parceiro de estudos. Ah, antes que eu me esqueça, deixarei aqui um link para a instalação do nosso mais novo parceiro de estudo. Fonte oficial hein: https://docs.mongodb.com/manual/installation/ :smile:

<h5 align="center">Ah, finalmente acabou a teoria? Sim, meu padawan! <h5>
  
**3.1. Instalei! e agora?**<br>
Abra o terminal sem medo e digite: 
```sql
mongodb # para ativar o mongodb
```
Agora digite: 
```sql
mongo # chamando o nosso banco de dados
```
Com ele já ativado e pronto digite: 
```sql
show dbs # Este comando mostrará os bancos de dados existentes
```
Agora o pulo do gato:
```sql
use NomeBanco # Se você colocar um nome que não existe na lista, Será criado pelo mongo automaticamente
```


<h5 align="center">Antes da gente seguir, vamos ver algumas diferenças de conceitos <h5>
  
  MySQL         | MongoDB
--------------  | ------
Banco de dados  | Banco de dados
Tabela          | Coleção
Linha           | Documento
Coluna          | Campo
Junção de Tabela| Documento incorporado
Primary Key     | Fornecido pelo próprio mongo

### 4. Vamos aos nossos comandos? 
Para tornar mais intuitivo o nosso aprendizado, tanto o meu, quanto o de vocês, vou dividir cada comando em subcapítulos. A minha intenção não é fazer comparações entre os comandos dos bancos de dados relacional e não relacional. Inclusive tenho um tutorial imcompleto, até mesmo momento, sobre SQL. Sem mais demoras, vamos começar a brincadeira. 

**4.1 Criado uma collection**<br>
Se olharmos as diferenças de conceitos, veremos que coleção é uma referência para a tabela do banco de dados relacional. Isso significa que é nela onde poderemos adicionar os nossos dados e atributos
```Javascript
db.createcollection("NomeDesejado")
```
**4.2 Inserindo dados numa coleção**<br>
Inserir dados numa coleção tem a mesma estrutura da construção de uma JSON. Basta chamar o comando e adicionar os dados necessários
```JavaScript
db.NomeColecao.insert
            ({
                     Livro: "Tudo sobre Mongo",
                     Autor: "Batman",
                     Cidade: "A colina dos Hobbits"
            })
```

<h5 align="center">Um pouco sobre consultas <h5>
  
**4.3 Vamos falar das consultas?**<br>

Assim como no banco relacional, NoSQL também tem diversas formas de fazer consultas. Este é o comando padrão
```JavaScript
db.NomeColecao.find()
```

**4.3.1. Consultando determinado valor**<br>
Caso você queira encontrar algum dado especifico, basta chama-lo com o comando find. Vamos a um exemplo para que possamos compreender melhor
```JavaScript
db.nomeColecao.find({ autor: { $eq: Batman }})
```

**4.3.2. Consultando dados entre valores especificos**<br>
Imagina que você ta lá de boas analisando os dados do seu site e pensa: "Quantas pessoas entre 20 e 30 anos acessam o meu site?". Não é impossível saber, basta usar essa mágica aqui 

```JavaScript
db.MInhaColecao.find(
                     { idade: { $gt: 20, $lt: 30 } }
  )
