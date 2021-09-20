
# Diagrama de Classe

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   13/08/2021   |  1.0    |  Criação do Documento    | Kleidson Alves, Lucas Gabriel
| 19/08/2021 | 1.1 | Atualização da Imagem | Kleidson Alves, Lucas Gabriel, Lucas Rodrigues
| 22/08/2021 | 1.2 | Revisão do documento | Marcos Adriano
| 19/09/2021 | 1.3 | Adição da Memória técnica | Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues 

## Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
O diagrama de classe é um diagrama estrutural(estático) UML. Ele mostra a estrutura do sistema projetado no nível de classes e interfaces, seus recursos, restrições e relacionamentos.
</p>
<p>
O diagrama de classe ajuda no melhor entendimento da visão geral dos esquemas de uma aplicação, especifica as necessidades do sistema de maneira visual e ilustra modelos de dados de qualquer complexidade. Para realizar a elaboração do artefato, a equipe utilizou a ferramenta lucidchart.
</p>
</div>

## Resultado

### Versão 1.0

![Diagrama de Classe versão 1](https://i.imgur.com/VDlHHIl.png)

<p>Autores: Kleidson Alves e Lucas Gabriel</p>

### Versão 2.0



## Memória Técnica 01
MEMÓRIA TÉCNICA ID_01

Data: 17 de Setembro de 2021

**Problema Identificado:** 
Incompatibilidade das práticas tradicionais de OO com as práticas acordadas pela Comunidade da Linguagem Dart, utilizada nesse projeto.
Especificamente, o fato que gera essa incompatibilidade é a Linguagem Dart julgar ser desnecessária a utilização dos getters e setters para atributos privados da classe,  o que não ocorre para o caso das práticas tradicionais da Orientação a Objetos.
FONTE: [https://dart.dev/tools/linter-rules#unnecessary_getters_setters](https://dart.dev/tools/linter-rules#unnecessary_getters_setters)

**Solução:** 
Seguir os padrões e as boas práticas da Linguagem Dart, em detrimento de outras orientações associadas as linguagens orientadas a objeto.
Decisão tomada pela equipe, com base em [debate](https://i.imgur.com/tsUMTew.png) e pesquisa feitas em [fóruns](https://stackoverflow.com/questions/61720221/why-should-i-avoid-wrapping-fields-in-getters-and-setters) da comunidade dart além da [página oficial de regras de estilo](https://dart.dev/tools/linter-rules#unnecessary_getters_setters) da Linguagem Dart.

OPÇÃO INCOMPATÍVEL:

    class Caixa {
      var _conteudo;
      get conteudo => _conteudo;
      set conteudo(value) {
        _conteudo = value;
      }
    }


OPÇÃO COMPATÍVEL:

    class Caixa {
      var conteudo;
    }



## Referências
> UML - Class. Disponível em: [https://www.uml-diagrams.org/class.html](https://www.uml-diagrams.org/class.html). Data de acesso: 13/08/2021

> UML Class and Object Diagrams Overview. Disponível em:[https://www.uml-diagrams.org/class-diagrams-overview.html](https://www.uml-diagrams.org/class-diagrams-overview.html). Data de acesso: 13/08/2021


> O que é um diagrama de classe UML?. Disponível em:[https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-classe-uml#section_1
](https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-classe-uml#section_1). Data de acesso: 13/08/2021