# Bancos de dados com o Chamy

Em resumo, sua avaliação vai ser seguinte forma

Nota1 que vai ter peso de 2,5<br>
Nota2 que vai ter 0,5<br>
Nota de acompanhamento<br>
e por último, a média do trabalho que ele vai pedir

## Campo

Mapeamento do atributo, ou seja, representa uma coluna em uma tabela e armazena um único tipo de dado para cada registro

Exemplos: Na tabela ![img.png](img.png)

Vemos que há 4 campos, o ID, Nome, Email e DataNascimento e cada um tem armazena seus dados especificos, como por exemplo

Nome tem campos para guardar dados de nomes, Email para guardar dados de Email e assim por diante

## Chave primaria

Uma Chave Primária é um campo que identifica de forma única cada registro em uma tabela

### Caracteristicas da chave primária:

* Não pode seer Null, ou seja, o valor não pode ser vazio
* É um valor único, pois cada linha deve-se ter o valor da chave único na tabela
* Identifica unicamente um registro, que garante que cada linha possa ser referenciada de maneira única

Um exemplo para criar uma tabela com a chave primária:

````sql
create table Cliente (
    Clicodigo int,
    Nome varchar(50),
    Email varchar(100),
    Primary Key (Clicodigo)
)
````

A partir disso, ele criará a tabela com a chave primaria que seria CliCodigo

## Chave Composta

É uma chave primária formada por dois ou mais campos em uma tabela. Isso significa que a combinação dos valores desses
campos deve ser única para cada registro.

* A Chave primária é composta por mais de um campo
* A combinação dos valores desses campos deve ser únicas
* Não pode ter valores NULL

Em resumo, a chave composta é uma ferramenta poderosa para garantir a integridade e a precisão dos dados em um banco de dados relacional
especialmente em situação onde uma chave primária simples não é suficiente


## Comente:

#### a. Relacionamentos devem ser implementados somente em casos específicos?

Sim, desde que tenha a questão de lógica associação entre as tabelas, Eles garantem a integridades dos dados e evitam que
não tenham sem sentido, não existe relação se não houver a chave estrageira

#### b. É normal que tenha valores nulos?

Em certas situações é normal que tenha valores nulos, pensa nos casos de registro de telefone, que geralmente tem 1 e o outro 
telefone, o usuário pode muito bem somente registrar somente 1, enquanto outro fica nulo, que isso é considerado normal, no entanto
não é bom manter os valores nulos

## Quais são Objetivos de um banco de dados

Armazenamento com concistencia, é um repositorio de fatos, mas não somente isso mas é um sistema para gerenciar os dados
de maneira eficiente e confiável

## Quais são as vantagens da chave estrangeira

A Vantagem da chave estrageira que ela está sendo referenciada em outra tabela, tendo a associação entre as 2 com consistencia,
que isso se chama integridade referencial, isso facilita a manutenção do banco de dados e eficiência nas consultas ao 
estruturar corretamente os relacionamentos

## Existe chave estrangeira composta?

SIm ela eexiste, ela são usadas para referenciar chaves primárias compostas de outras tabelas

## Como mapear uma especialização de uma entidade superclasse com uma única classe?


````mermaid
erDiagram
    Empregado{
        
    }
    
    Vendedor{
        
    }
    
    Entregador{
        
    }
    Empregado  ||--o{ Vendedor: places
    Empregado ||--o{ Entregador : places
    
````
#### Olhando a essa imagem, a superclasse ela seria o EMPREGADO, tendo seus 2 filhos, que seria o VENDEDOR e ENTREGADOR, 
Isso seria a mapeação de uma entidade superclasse

## O que seria dissociação

É quando as 2 classes filhas não tem alguma relação um com a outra, elas não se misturam, ou seja, elas podem está dentro
do contexto, mas elas não possuem relação direta com outra, elas existem independentemente

## O que seria Sobreposição

É quando as 2 classes filhas elas tem alguma relação um com a outra, elas podem se misturar, ou seja, elas podem compartilha 
mesmos atributos, Isso significa que os objetos podem pertencer a mais de uma categoria ao mesmo tempo

## Ordem de comandos em SQL

<ol>
<li>distic</li>
<li>Select</li>
<li>From</li>
<li>Inner Join <br> Inner Join 2 <br> Inner Join n
<li>Where</li>
<li>Group by</li>
<li>Order By</li>
<li>Limit</li>
</ol>

<strong>Então a ORDEM ELA SERIA: 3 -> 4 -> 5 -> 6 -> 7 -> 8 -> 1 -> 2</strong>
