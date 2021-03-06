# GRASPs

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   01/09/2021   |  1.0    |  Criação do Documento    | Kleidson Alves, Lucas Gabriel
|   03/09/2021   |  1.1    |  Adição das Imagens   | Gabriel Batalha, Kleidson Alves, Lucas Gabriel 
|   16/09/2021   |  1.2    |  Adição de Texto   | Wellington Jonathan
|   20/09/2021   |  1.3    |  Revisão do Documento   | Kleidson Alves, Lucas Rodrigues, Lucas Gabriel

## Introdução
<div style="text-indent: 40px; text-align: justify">

<p>
Podemos entender Design Patterns ou padrões de projetos  como soluções generalistas para problemas que acontecem recorrentemente durante o desenvolvimento de um software. Voltado principalmente a uma  definição de alto nível de como um problema comum pode ser solucionado, os padrões de projetos não se tratam apenas de um framework ou um código pronto. Sua implementação está fortemente ligada à orientação a objetos e utilização da UML.
</p>

<p>
Os padrões de projeto GRASP (General Responsibility Assignment Software Patterns), consistem em práticas para atribuição de responsabilidades, para classes e objetos, em projetos orientados a objetos.
</p>

<p>
Estes padrões de projeto  foram publicados originalmente pelo especialista Craig Larman no livro “Applying UML and Patterns – An Introduction to Object-Oriented Analysis and Design and the Unified Process” (obra traduzida em português com o título “Utilizando UML e Padrões – Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo”).
</p>

<p>
O conceito de responsabilidade deve ser compreendido, basicamente, como as obrigações que um objeto possui quando se leva em conta o seu papel dentro de um determinado contexto. Além disso, é preciso considerar ainda as prováveis colaborações (interações) entre diferentes objetos. Cada padrão GRASP está melhor detalhado abaixo.
</p>

</div>


## Criador

<div style="text-indent: 40px; text-align: justify">
<p> 
Uma atividade muito importante para um sistema de orientação a objetos é a criação de um objeto. Com base nisso, torna-se uma atividade fundamental identificar qual classe será responsável pela criação de determinado objeto. Diante desse contexto há o padrão Criador que determina qual classe deve ser responsável pela criação do objeto.
</p>
</div>

Problema: Quem seria responsável por criar novas instâncias de algumas classes? 

Solução: Atribua à classe B a responsabilidade de criar uma instância da classe A se:

1. B agrega objetos de A
2. B contém A
3. B armazena instância de A
4. B usa objetos de A
5. B possui informação necessária à criação de A

![](https://i.imgur.com/3d9YuGW.png)
Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel

<div style="text-indent: 40px; text-align: justify">
<p> 
A imagem acima é uma retratação de uma modelagem do projeto que se encaixa no padrão de projeto GRASP Criador. No exemplo, a classe <i>Client</i> é a classe responsável por instanciar os objetos da classe <i>Announcement</i>. Isso significa que cada objeto <i>Client</i> é o responsável por criar seus próprios <i>Announcements</i>, visto que ele detém as informações necessárias para tal atividade.
</p>
</div>


## Especialista
<div style="text-indent: 40px; text-align: justify">

<p>
O princípio Especialista é um princípio utilizado para determinar onde delegar responsabilidades. Nesse princípio, uma abordagem geral para atribuir responsabilidades é olhar para uma determinada responsabilidade, determinar a informação necessária para cumpri-la e depois determinar onde essa informação está armazenada.
</p>
</div>

Problema: Qual é o princípio geral para a atribuição de responsabilidades aos objetos?

Solução: Atribua a responsabilidade ao especialista: a classe que tem as informações necessárias para assumir a responsabilidade.

![](https://i.imgur.com/5KlsGvJ.png)
Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel

<div style="text-indent: 40px; text-align: justify">
<p> 
A imagem acima destaca uma modelagem que se enquadra no padrão GRASP Especialista. A classe <i>Announcement</i> contém informações com respeito a categoria do anúncio e uma lista de comentários que estão relacionados a ele. Essas informação são obtidas a partir da agregação com outras classes - <i>Category</i> e <i>Comment</i>. O padrão de Especialidade pode ser observado pelo fato de a responsabilidade de mostrar todas as informações de anúncio ser atribuída a classe <i>Announcement</i>, ou seja, aquela que detém todas as informações necessárias para isso.
</p>
</div>


![](https://i.imgur.com/GlBaoTc.png)
Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel

<div style="text-indent: 40px; text-align: justify">
<p> 
 A imagem acima destaca a aplicação do Especialista, tendo como foco a método <i>applyFilter</i> presente na classe <i>Collection</i>. Na etapa de modelagem, a equipe identificou o seguinte problema: quem seria responsável por fazer a aplicação do filtro na lista de anúncios presentes na aplicação? Seguindo o padrão Especialista, a classe que recebe essa responsabilidade dever ser aquela que possui todas as informações necessárias para a realização desta. Diante disso, a <i>Collection</i> foi identificada como tal, pois possui a lista de todos os anúncios, podendo obter todos os atributos necessários para aplicar o filtro corretamente.  
</p>
</div>

## Polimorfismo

<div style="text-indent: 40px; text-align: justify">
<p>
O polimorfismo é um princípio, no qual subclasses de uma superclasse são capazes de invocar métodos de mesma assinatura, porém com comportamento diferente para cada subclasse.
</p>
</div>

Problema: Como tratar alternativas baseadas no tipo da classe? Como criar componentes de software “plugáveis”?

Solução: É aconselhável atribuir responsabilidades aos tipos usando operações polimórficas, isso quando alternativas ou comportamento relacionados variam com o tipo da classe.

![](https://i.imgur.com/VGlpfyC.png)
Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel

<div style="text-indent: 40px; text-align: justify">

 <p>
A imagem acima é uma retratação de uma modelagem do projeto que se encaixa no padrão de projeto GRASP Polimorfismo. O exemplo de polimorfismo é dado pelas classes <i>User</i> (super classe) e as classes <i>Admin</i> e <i>Client</i> (subclasses), a classe <i>User</i> contém os métodos <i>deleteComment()</i> e <i>deleteAnnouncement()</i> que são herdados pelas subclasses, entretanto, na classe <i>Admin</i>, o comportamento desses métodos são alterados visto que o <i>Client</i> só pode deletar anúncios e comentários dos quais ele é o autor, enquanto o <i>Admin</i> pode deletá-los independentemente do autor.
</p>
</div>

## Controlador
<div style="text-indent: 40px; text-align: justify">
<p>
O controlador é o princípio que determina que as responsabilidades de manipulação de um evento devem ser atribuídas a um objeto controlador, que, por sua vez, é um objeto de interface não-usuário. Sendo assim, esse controlador terá algumas responsabilidades importantes, tais como determinar quais objetos são responsáveis por tratar eventos gerados na camada de interface com o usuário, determinar as operações que o sistema é capaz de realizar e determinar mensagens de retorno ao usuário.
</p>
</div>

Problema: Quem seria responsável por lidar com um evento do sistema?

Solução: Atribua responsabilidade de lidar com eventos a uma classe que:
1. Represente o sistema como um todo
2. Representa a organização
3. Represente algo ativo no mundo real envolvido na tarefa
4. Represente um controlador artificial dos eventos de sistema de um caso de uso

![](https://i.imgur.com/ymlttU2.png)
Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel


<div style="text-indent: 40px; text-align: justify">
<p>
A imagem acima é uma retratação de uma modelagem do projeto que se encaixa no padrão de projeto GRASP Controlador. A classe <i>Authentication</i> tem como função controlar a autenticação dos usuários, sendo que aqueles que já possuem uma conta registrada no Banco de Dados utilizam o método de <i>signin</i> ou <i>signout</i> para sair, enquanto os que estão autenticando pela primeira vez utilizam o método de <i>signup</i>.
</p>
</div>

## Baixo Acoplamento

<div style="text-indent: 40px; text-align: justify">
<p>
O acoplamento é uma medida de de quão forte um objeto está conectado, tem conhecimento ou depende de outro. Para alcançar o baixo acoplamento é preciso distribuir as responsabilidades de maneira eficaz.
</p>
<p>
O baixo acoplamento permite que exista uma menor dependência entre classes, mudanças em uma classe tenham menor impacto sobre outras e o código tenha maior potencial de ser reutilizado.
</p>
</div>

Problema: Como minimizar dependências e maximizar reuso? 

Solução: Atribuir a responsabilidade de modo que a dependência entre classes seja baixa.

## Variações Protegidas

<div style="text-indent: 40px; text-align: justify">
<p>
Esse princípio determina a proteção do sistema com a variação de outros elementos, tais como objetos sistemas e subsistemas. Consiste em encapsular o comportamento que realmente importa e utilização de polimorfismo para criar várias implementações da interface. 
</p>
</div>


Problema: Como projetar objetos, subsistemas e sistemas, de modo que, as variações ou instabilidades nesses elementos não sejam responsáveis por impactos indesejáveis em outros elementos?

Solução: Identificar pontos de variação e atribuir responsabilidades para criar uma interface estável em volta desses pontos;

![](https://i.imgur.com/NF9lFb7.png)
Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel

A imagem acima é uma retratação de uma modelagem do projeto que se encaixa no padrão de projeto GRASP Variações Protegidas. O exemplo apresenta duas classes que utilizam do Polimorfismo e Encapsulamento, onde apenas as classes filhas de <i>User</i> fazem uso dos métodos <i>deleteComment()</i> e <i>deleteAnnouncement()</i> da mãe.


## Indireção

<div style="text-indent: 40px; text-align: justify">
<p>
Indireção é um principio que indica que a criação de uma classe intermediaria, aquela que tem a responsabilidade de mediador entre dois elementos. Isso pode simplificar a aplicação reduzindo o número de referências entre objetos. Indireção é uma das maneiras de se obter um baixo acoplamento.
</p>
</div>


Problema: Como evitar acoplamento direto e manter alta possibilidade de reuso através do desacoplamento de objetos?

Solução: A responsabilidade será atribuída a um objeto intermediário que faz mediação entre componentes e serviços de modo que esses não sejam diretamente acoplados.


## Alta coesão

<div style="text-indent: 40px; text-align: justify">
<p>
A alta coesão visa manter os objetos adequadamente focados, gerenciáveis e compreensíveis. De maneira geral as responsabilidades de um elemento estão fortemente focadas e relacionadas, o que é, também, uma forma de auxiliar no baixo acoplamento.
</p>
</div>


Problema: Como manter a complexidade sob controle?

Solução: Atribuir uma responsabilidade para que a coesão se mantenha alta


## Invenção pura

<div style="text-indent: 40px; text-align: justify">
<p>
 Trata-se de classe que não representa nenhum conceito no domínio do problema, ela apenas funciona como uma classe prestadora de serviços. A aplicação desse princípio resulta em baixo acoplamento, alta coesão e o potencial de reutilização derivado.
</p>
</div>


Problema: Quando não se quer violar a alta coesão e baixo acoplamento e o expert não oferece soluções apropriadas, qual objeto deve ter a responsabilidade?

Solução: Criação de classes puras


## Referências
> GRASP (padrão orientado a objetos). Disponível em:
[https://pt.wikipedia.org/wiki/GRASP_(padr%C3%A3o_orientado_a_objetos)](https://pt.wikipedia.org/wiki/GRASP_(padr%C3%A3o_orientado_a_objetos)). Data de acesso: 01/09/2021

>Understanding the GRASP Design Patterns. Disponível em: [https://medium.com/@ReganKoopmans/understanding-the-grasp-design-patterns-2cab23c7226e](https://medium.com/@ReganKoopmans/understanding-the-grasp-design-patterns-2cab23c7226e). Data de acesso: 01/09/2021


>Padrões GRASP — Padrões de Atribuir Responsabilidades. Disponível em: [https://medium.com/@ReganKoopmans/understanding-the-grasp-design-patterns-2cab23c7226e](https://medium.com/@leandrovboas/padr%C3%B5es-grasp-padr%C3%B5es-de-atribuir-responsabilidades-1ae4351eb204). Data de acesso: 01/09/2021

> Padrão de projeto de software. Disponível em: [https://pt.wikipedia.org/wiki/Padr%C3%A3o_de_projeto_de_software#Padr%C3%B5es[6][7][8]](https://pt.wikipedia.org/wiki/Padr%C3%A3o_de_projeto_de_software#Padr%C3%B5es[6][7][8]). Data de acesso: 01/09/2021

> Controller – Padrões GRASP. Disponível em: [https://www.ramonsilva.net/post/controller-padr%C3%B5es-grasp](https://www.ramonsilva.net/post/controller-padr%C3%B5es-grasp). Data de acesso: 01/09/2021


