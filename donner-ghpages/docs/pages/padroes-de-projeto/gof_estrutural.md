# GOFs Estruturais

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   03/09/2021   |  1.0    | Criação do Documento  | Gabriel Batalha, Hugo Bezerra, Lucas Rodrigues, Marcos Adriano
|   16/09/2021   |  1.1    | Atualização do Documento  | Davi Antônio, Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Rodrigues, Lucas Gabriel
|   17/09/2021   |  1.2    | Adição da Aplicação do Composite  | Davi Antônio, Gabriel Batalha, Kleidson Alves, Lucas Rodrigues, Lucas Gabriel
|   19/09/2021   |  1.3    | Finalização do Adapter | Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues
|   20/09/2021   |  1.4    | Revisão do Documento | Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Davi Antônio, Wellington Jonathan

## Adapter 

### Introdução

<div style="text-indent: 40px; text-align: justify">
<p>
O Adapter é um padrão de projeto estrutural que tem como objetivo permitir a interação e cooperação de diferentes interfaces. Ele irá converter a interface de uma classe para uma que seja esperada pelo cliente. Uma das motivações para a utilização desse padrão é que uma classe poderia deixar de ser reutilizada por não corresponder à uma interface de um domínio requerida por uma aplicação.
</p>
</div>

### Modelagem

![](https://i.imgur.com/4TK9fsp.png)

Autores: Davi Antônio, Gabriel Batalha, Kleidson Alves, Lucas Rodrigues, Lucas Gabriel


### Aplicação

[![](https://i.imgur.com/iyJYbMV.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/widgets/models/client_model.dart)


### Comentário

<div style="text-indent: 40px; text-align: justify">
<p>
O Adapter foi utilizado na classe Client para adaptar os dados provenientes da API para um formato entendível pela aplicação e para formatar os dados da aplicação para serem enviados para a API.  
</p>
</div>

## Composite

### Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
O Composite é um padrão de projeto que se baseia em gerar estruturas em forma de árvores, de modo que estruturas simples ficam gradualmente mais complexas conforme a necessidade de se adicionar mais ramificações a estrutura de árvore, após construída, essa estrutura composite pode ser tratada como se fosse um objeto individual. A chave para o padrão Composite é uma classe abstrata que representa tanto as primitivas como os seus recipientes.
</p>
<p>
O Flutter utiliza na sua implementação o padrão de projeto composite, dessa forma os widgets utilizados no Flutter são geralmente compostos por outros menores, em uma estrutura de arvore.
</p>
</div>

### Modelagem

![](https://i.imgur.com/GOCQznN.png)

Autores: Davi Antônio, Gabriel Batalha, Kleidson Alves, Lucas Gabriel e Lucas Rodrigues

### Aplicação

[![](https://i.imgur.com/gRZbLF0.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/widgets/category_tile/category_tile.dart)

[![](https://i.imgur.com/V2l4NWk.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/screens/category_screen.dart)


### Comentário
<div style="text-indent: 40px; text-align: justify">
<p>
No projeto o composite foi utilizado para construção da tela de categoria. A estrutura de árvore pode ser observada nessa tela, visto que ela é construída sobre uma coluna que envolve uma lista de widgets. A coluna é utilizada para ordenar verticalmente outros Composites (CategoryTile) e leafs (Dividers).  Já na classe CategoryTile, observamos sua composição pelas leafs Text e Icon. O resultado é que toda a estrutura da tela de categoria será tratada como um único objeto da classe CategoryScreen.   
</p>
</div>

## Referências
> Padrões de projeto estruturais. Disponível em: [https://refactoring.guru/pt-br/design-patterns/structural-patterns](https://refactoring.guru/pt-br/design-patterns/structural-patterns). Data de acesso: 03/09/2021

> Padrão de Projeto Adapter em Java. Disponível em: [https://www.devmedia.com.br/padrao-de-projeto-adapter-em-java/26467](https://www.devmedia.com.br/padrao-de-projeto-adapter-em-java/26467). Data de acesso: 19/09/2021

> Flutter Design Patterns: 2 — Adapter. Disponível em: [https://medium.com/flutter-community/flutter-design-patterns-2-adapter-3f05c02a7c84](https://medium.com/flutter-community/flutter-design-patterns-2-adapter-3f05c02a7c84). Data de acesso: 19/09/2021

> Flutter Design Patterns: 4 — Composite. Disponível em: [https://medium.com/flutter-community/flutter-design-patterns-4-composite-23473cccf2b3](https://medium.com/flutter-community/flutter-design-patterns-4-composite-23473cccf2b3). Data de acesso: 19/09/2021
