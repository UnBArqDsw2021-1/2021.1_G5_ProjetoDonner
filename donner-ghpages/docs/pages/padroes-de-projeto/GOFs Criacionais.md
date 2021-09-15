# GOFs Criacionais

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   03/09/2021   |  1.0    |  Criação do Documento  | Hugo Bezerra, Lucas Rodrigues, Marcos Adriano
|   14/09/2021   |  1.1    |  Adição das imagens  | Hugo Bezerra, Kleidson, Lucas Rodrigues, Lucas Gabriel
|   15/09/2021   |  1.2    |  Adição Singleton  | Kleidson, Gabriel Batalha, Lucas Gabriel, Lucas Rodrigues



## Singleton 

### Introdução

<div style="text-indent: 40px; text-align: justify">
<p>
O Singleton é um GoF Criacional que se baseia em permitir a existência de apenas uma instância de uma classe específica ao mesmo tempo que garante acesso global as propriedades dessa classe.
</p>
</div>

### Modelagem
![](https://i.imgur.com/vorjz5s.png)

### Aplicação

![](https://i.imgur.com/9Qgavu1.png)

### Comentário

<div style="text-indent: 40px; text-align: justify">
<p>
O banco de dados precisa ser instanciado uma única vez em toda aplicação. Na aplicação desse padrão no projeto da equipe, a classe Database retorna uma instância da conexão do banco de dados, fazendo a verificação se essa conexão já foi realizada. 
</p>
</div>


## Factory Method
### Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
O Factory Method é um dos GoFs criacionais e é descrito no livro (Design Patterns: Elements of Reusable Object-Oriented Software) da seguinte maneira: defini uma interface para a criação de objetos e deixa para a subclasse a decisão de qual classe instanciar.
</p>

</div>

### Modelagem
![](https://i.imgur.com/LrYUoMA.png)

### Aplicação
![](https://i.imgur.com/LuZGowZ.png)

![](https://i.imgur.com/MfEUvbL.png)

![](https://i.imgur.com/BwgyrqL.png)

![](https://i.imgur.com/hGE1qv8.png)





### Comentário

<div style="text-indent: 40px; text-align: justify">
<p>
No projeto utilizamos o Factory method para criação dos diferentes tipos de botões. A utilização desse padrão de projeto, faz com que não seja necessário o conhecimento direto de cada construtor das diferentes classes dos botões. Por isso, utiliza-se a classe FactoryButton especificando o tipo de botão desejado, obtendo a instância de uma das classes.
</p>
</div>

<!-- 
Abstract Factory pros usuarios
Factory Method pras campanhas

prototype pros anuncios
Abstract pros anuncios 
-->

## Referências
> PADRÕES de PROJETO. Disponível em: https://refactoring.guru/pt-br/design-patterns. Data de acesso: 03/09/2021

> PADRÕES Gof. Disponível em: http://www.facom.ufu.br/~bacala/ESOF/05b-Padrões%20Gof.pdf. Data de acesso: 03/09/2021

> Design Patterns: Padrões “GoF”. Disponível em: https://www.devmedia.com.br/design-patterns-padroes-gof/16781. Data de acesso: 03/09/2021

> Flutter Design Patterns: 10 — Factory Method. Disponível em:[https://medium.com/flutter-community/flutter-design-patterns-10-factory-method-c53ad11d863f](https://medium.com/flutter-community/flutter-design-patterns-10-factory-method-c53ad11d863f). Data de acesso: 10/09/2021

>Flutter Design Patterns: 1 — Singleton. Disponível em: [https://medium.com/flutter-community/flutter-design-patterns-1-singleton-437f04e923ce](https://medium.com/flutter-community/flutter-design-patterns-1-singleton-437f04e923ce). Data de acesso: 14/09/2021

>Singleton em TypeScript. Disponível em: [https://refactoring.guru/pt-br/design-patterns/singleton/typescript/example#lang-features](https://refactoring.guru/pt-br/design-patterns/singleton/typescript/example#lang-features). Data de acesso: 14/09/2021

> Design Patterns: Elements of Reusable Object-Oriented Software