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
use NomeDecidido # Mesmo que não exista um banco com esse nome, o Mongo criará automaticamente. 
