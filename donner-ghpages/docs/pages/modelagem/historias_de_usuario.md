# Histórias de usuário 

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   15/08/2021   |  1.0    |  Criação do Documento    | Kleidson Alves, Lucas Gabriel, Lucas Rodrigues
| 22/08/2021 | 1.1 | Revisão do Documento | Gabriel Batalha
| 23/08/2021 | 1.2 | Atualização do Documento | Wellington Jonathan
| 23/08/2021 | 1.3 | Correções ortográficas | Lucas Rodrigues

## Introdução

<div style="text-indent: 40px; text-align: justify">
<p>
Uma história de usuário é uma explicação informal e geral sobre um recurso de software escrito a partir da perspectiva do usuário final. Seu objetivo é articular como um recurso de software pode gerar valor para o cliente. No contexto ágil, refere-se a uma unidade de trabalho. É um objetivo final expresso pela perspectiva do usuário.
</p>
<p>
 A equipe assumiu a identidade das personas e de stakeholders a fim de explicitar seus desejos dentro de cada épico disponibilizado pela equipe. Dessa forma, foram geradas histórias formatadas para se encaixarem no documento, com critérios de aceitação definidos pela equipe com base nos requisitos descritos nos documentos de brainstorming, introspecção e storyboard.
</p>
</div>

## Resultados

### Épico 01: Usuário


#### Feature 01:  Autenticação


| US01 |
| -------- |
| *Eu, como usuário, desejo poder entrar na aplicação com a minha conta*|
| **Critérios de aceitação:** |
| - Deve haver um botão de login <br> - Deve haver a opção de se fazer login com a conta da Google <br> - Deve ser possível escolher a conta com a qual deseja se conectar|

| US02 |
| -------- |
| *Eu, como usuário, desejo poder sair da aplicação*|
| **Critérios de aceitação:** |
| - Deve haver um botão de logout |

| US03 |
| -------- |
| *Eu, como usuário, desejo poder navegar pela aplicação sem obrigação de realizar login com a minha conta*|
| **Critérios de aceitação:** |
| - A tela principal de anúncios deve ser a primeira a ser mostrada ao entrar na aplicação <br> - O usuário deve ser redirecionado à tela de login apenas quando tentar realizar atividades de criar anúncio, visitar perfil do anunciante, demonstrar interesse ou comentar em um anúncio|

#### Feature 02:  Perfil

| US04 |
| -------- |
| *Eu, como usuário, desejo poder atualizar as informações do meu perfil*|
| **Critérios de aceitação:** |
| - Deve haver um botão de edição no perfil do usuário logado <br> - Deve haver uma página de formulário editável para os dados do perfil <br> - Os dados do perfil devem ser atualizados após a confirmação do usuário |

| US05 |
| -------- |
| *Eu, como usuário, desejo poder visualizar informações do meu perfil*|
| **Critérios de aceitação:** |
| - Deve haver um botão de acesso à página do perfil <br> - Deve haver uma página de perfil<br>- A página deve conter todas as informações cadastradas pelo usuário |

#### Feature 03: Cadastro

| US06 |
| -------- |
| *Eu, como usuário, desejo poder cadastrar uma descrição para o meu perfil*|
| **Critérios de aceitação:** |
| - Deve haver um campo relacionado à descrição do perfil no formulário de cadastro do usuário|

| US07 |
| -------- |
| *Eu, como usuário, desejo cadastrar um ou mais números de telefone ao meu perfil*|
| **Critérios de aceitação:** |
| - Deve haver um campo relacionado ao telefone do perfil no formulário de cadastro do usuário |

| US08 |
| -------- |
| *Eu, como usuário, desejo cadastrar minha localização*|
| **Critérios de aceitação:** |
| - Deve haver um botão que permita que o usuário selecione sua cidade e seu estado |

#### Feature 04: Ajuda

| US09 |
| -------- |
| *Eu, como usuário, desejo ser instruído sobre como utilizar as funcionalidades da aplicação*|
| **Critérios de aceitação:** |
| - Um tutorial deve ser apresentado na primeira vez de uso da aplicação <br> - As principais funcionalidades da aplicação devem ser mostradas no tutorial |

### Épico 02: Administrador

#### Feature 05: Controle

| US10 |
| -------- |
| *Eu, como administrador, desejo poder deletar comentários de qualquer usuário*|
| **Critérios de aceitação:** |
| -  Todos os comentários devem permitir que o administrador os exclua|

| US11 |
| -------- |
| *Eu, como administrador, desejo poder deletar anúncios de qualquer usuário*|
| **Critérios de aceitação:** |
| - Para um usuário administrador, todo anúncio deve possuir a opção de ser excluído |

| US12 |
| -------- |
| *Eu, como administrador, desejo poder criar campanhas de doação*|
| **Critérios de aceitação:** |
| - Deve haver uma página com um formulário para criação de campanha <br> - Após a confirmação do administrador, a campanha deve ser salva na aplicação <br> - Todos os usuários devem poder ver a campanha |


### Épico 03: Anúncio

#### Feature 06: Comentário

| US13 |
| -------- |
| *Eu, como usuário, desejo poder deletar comentários feitos por mim*|
| **Critérios de aceitação:** |
| - No anúncio feito pelo usuário, deve haver a opção de excluir <br> - O comentário deve ser apagado para todos |

| US14 |
| -------- |
| *Eu, como usuário, desejo poder comentar em anúncios*|
| **Critérios de aceitação:** |
| -  Deve ser possível comentar em anúncios feitos por outros usuários<br>- Deve ser possível comentar em anúncios feitos pelo próprio usuário |

| US15 |
| -------- |
| *Eu, como usuário, desejo poder editar um comentário que fiz anteriormente*|
| **Critérios de aceitação:** |
| - Em todos os comentários feito pelo usuário, deve haver a opção de editar comentário <br> - O comentário é atualizado após a confirmação do usuário <br> - Um comentário editado deve ser apresentado como "editado"  |

#### Feature 07: Informação

| US16 |
| -------- |
| *Eu, como usuário, desejo poder ver mais detalhes sobre um anúncio*|
| **Critérios de aceitação:** |
|-Todos os anúncios devem ter uma página contendo seus detalhes<br>-  Ao clicar em um anúncio o usuário deve ser encaminhado para a página do anúncio|

| US17 |
| -------- |
| *Eu, como usuário, desejo poder ver o perfil do responsável pelo anúncio*|
| **Critérios de aceitação:** |
| - Na página do anúncio, deve haver uma breve informação sobre o anunciante <br> - Deve ser possível acessar o perfil do anunciante a partir da página de seu anúncio |

#### Feature 08: Gerenciar

| US18 |
| -------- |
| *Eu, como usuário, desejo poder criar um anúncio de pedido de doação ou oferta de doação*|
| **Critérios de aceitação:** |
| -  Deve haver um botão que permita ao usuário inciar o cadastro de um anúncio<br>- O usuário deve poder selecionar qual tipo de anúncio deseja criar, pedido de doação ou oferta de doação|

| US19 |
| -------- |
| *Eu, como usuário, desejo poder editar as informações de um anúncio ou pedido de doação criados por mim*|
| **Critérios de aceitação:** |
| -  Deve haver um botão que permita editar o próprio anúncio<br>- Deve haver uma página de formulário editável para os dados do anúncio<br>- Apenas o criador do anúncio deve poder editá-lo|

| US20 |
| -------- |
| *Eu, como usuário, desejo poder criar uma descrição para o anúncio ou pedido de doação*|
| **Critérios de aceitação:** |
| - Deve haver um campo para adicionar uma descrição do item que está sendo doado ou pedido |

| US21 |
| -------- |
| *Eu, como usuário, desejo poder excluir um anúncio que fiz anteriormente*|
| **Critérios de aceitação:** |
| - Deve ser possível um usuário acessar todos os seus anúncios <br> - Em cada um de seus anúncios, deve possuir a opção de "excluir" <br> - Deve ser solicitado uma confirmação de exclusão <br> - Após realizada a exclusão, o anúncio não deverá ser mostrado para nenhum usuário da aplicação |

| US22 |
| -------- |
| *Eu, como usuário, desejo poder adicionar imagens ao anúncio*|
| **Critérios de aceitação:** |
| - Na página de criação do anúncio, deve haver uma área para adicionar imagem <br> - Deve ser possível adicionar mais de uma imagem |

| US23 |
| -------- |
| *Eu, como usuário, desejo poder denunciar anúncios que eu julgue desrespeitosos ou ofensivos*|
| **Critérios de aceitação:** |
| - Em todos os anúncios, deve haver uma opção de denúncia <br> - A denúncia deve ser anônima|


| US24 |
| -------- |
| *Eu, como usuário, desejo poder selecionar uma categoria para o anúncio ou pedido de doação*|
| **Critérios de aceitação:** |
| -  Deve haver um botão que permita a seleção de uma das categorias para o anúncio <br> - O anúncio deve pertencer a apenas uma categoria |

#### Feature 09: Busca

| US25 |
| -------- |
| *Eu, como usuário, desejo poder pesquisar um anúncio por nome*|
| **Critérios de aceitação:** |
| - Deve haver um campo de busca <br> - Após solicitado pelo usuário, o usuário deve ser redirecionado para a página do anúncio <br> - Se um anúncio pesquisado não existir na aplicação , deve ser apresentada uma mensagem indicando isso|

| US26 |
| -------- |
| *Eu, como usuário, desejo poder filtrar os anúncios de acordo com as minhas necessidades*|
| **Critérios de aceitação:** |
| -  Deve haver um botão de filtro<br> - Deve ser possível filtrar a exibição dos produtos por categoria<br> - Deve ser possível filtrar a exibição dos produtos por tipo de anúncio(pedido ou oferta)|

| US27 |
| -------- |
| *Eu, como usuário, desejo visualizar a lista de anúncios no formato que eu escolher*|
| **Critérios de aceitação:** |
| - Deve haver uma forma de alterar o modo de visualização <br> - Deve haver a opção de visualização em lista <br> - Deve haver a opção de visualização em grade |

| US28 |
| -------- |
| *Eu, como usuário, desejo ver uma lista de anúncios*|
| **Critérios de aceitação:** |
| - A lista de anúncios deve ser mostrada para o usuário na tela principal|

#### Feature 09: Interesse

| US29 |
| -------- |
| *Eu, como usuário, desejo poder pesquisar um grupo de anúncios de determinada categoria*|
| **Critérios de aceitação:** |
| -  Deve haver um botão de categoria<br> - Deve ser possível filtrar a exibição dos produtos por categoria|

| US30 |
| -------- |
| *Eu, como usuário, desejo poder marcar anúncios nos quais eu demonstrei interesse*|
| **Critérios de aceitação:** |
| - Em todo anúncio não feito pelo usuário, deve haver a opção de demonstrar interesse|

| US31 |
| -------- |
| *Eu, como sistema, desejo colocar o usuário interessado em contato com o usuário do anúncio*|
| **Critérios de aceitação:** |
| - O sistema deve passar para o usuário interessado as informações de contato do usuário proprietário do anúncio |

#### Feature 10: Compartilhar

| US32 |
| -------- |
| *Eu, como usuário, desejo compartilhar um anúncio para outras plataformas*|
| **Critérios de aceitação:** |
| - Em todo anúncio, deve haver a opção de compartilhar o anúncio |

## Referências

> Histórias de usuários com exemplos e template. Disponível em [https://www.atlassian.com/br/agile/project-management/user-stories](https://www.atlassian.com/br/agile/project-management/user-stories). Data de acesso: 15/08/2021
 
> Epic, Feature e User Story (Epico, Funcionalidade e História de Usuário). Disponível em [https://www.ateomomento.com.br/epic-feature-e-user-story/](https://www.ateomomento.com.br/epic-feature-e-user-story/). Data de acesso: 15/08/2021


