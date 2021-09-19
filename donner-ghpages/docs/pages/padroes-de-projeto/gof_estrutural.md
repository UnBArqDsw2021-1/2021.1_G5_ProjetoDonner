# GOFs Estruturais

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   03/09/2021   |  1.0    | Criação do Documento  | Gabriel Batalha, Hugo Bezerra, Lucas Rodrigues, Marcos Adriano
|   16/09/2021   |  1.1    | Atualização do Documento  | Davi Antônio, Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Rodrigues, Lucas Gabriel
|   17/09/2021   |  1.2    | Adição da Aplicação do Composite  | Davi Antônio, Gabriel Batalha, Kleidson Alves, Lucas Rodrigues, Lucas Gabriel
|   19/09/2021   |  1.3    | Finalização do adapter | Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues

## Adapter 

### Introdução

<div style="text-indent: 40px; text-align: justify">
<p>
O Adapter é um padrão de projeto que tem como objetivo permitir que objetos com interfaces diferentes possam colaborar entre si. Ele servirá como um intermediador que recebe solicitações do cliente e converte essa solicitação em um formato entendível para o fornecedor. 
</p>
</div>

### Modelagem

![](https://i.imgur.com/4TK9fsp.png)

### Aplicação

![](https://i.imgur.com/iyJYbMV.png)


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
O Composite é um padrão de projeto estrutural que permite que você componha objetos em estruturas de árvores e então trabalhe com essas estruturas como se elas fossem objetos individuais.
</p>
<p>
O Flutter utiliza na sua implementação o padrão de projeto composite, dessa forma os widgets utilizados no Flutter são geralmente compostos por outros menores, em uma estrutura de arvore.
</p>
</div>

### Modelagem

![](https://i.imgur.com/GOCQznN.png)

Autores: Davi Antônio, Gabriel Batalha, Kleidson Alves, Lucas Gabriel e Lucas Rodrigues

### Aplicação

![](https://i.imgur.com/gRZbLF0.png)

![](https://i.imgur.com/V2l4NWk.png)


### Comentário
<div style="text-indent: 40px; text-align: justify">
<p>
No projeto o composite foi utilizado para construção da tela de categoria. A estrutura de árvore pode ser observada nessa tela, visto que ela é construída sobre uma coluna que envolve uma lista de widgets. A coluna é utilizada para ordenar verticalmente outros Composites (CategoryTile) e leafs (Dividers).  Já na classe CategoryTile, observamos sua composição pelas leafs Text e Icon. O resultado final é que toda a estrutura da tela de categoria será tratada como um único objeto da classe CategoryScreen.   
</p>
</div>

## Referências
> PADRÕES de PROJETO. Disponível em: https://refactoring.guru/pt-br/design-patterns. Data de acesso: 03/09/2021

> PADRÕES Gof. Disponível em: http://www.facom.ufu.br/~bacala/ESOF/05b-Padrões%20Gof.pdf. Data de acesso: 03/09/2021

> Design Patterns: Padrões “GoF”. Disponível em: https://www.devmedia.com.br/design-patterns-padroes-gof/16781. Data de acesso: 03/09/2021