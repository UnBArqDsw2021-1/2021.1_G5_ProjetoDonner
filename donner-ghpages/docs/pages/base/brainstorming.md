# Brainstorming

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   28/07/2021   |  1.0    |  Criação do documento    | Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Davi Antônio, Wellington Jonathan

## Introdução
<div style="text-indent: 40px; text-align: justify">
A técnica de Brainstorming foi utilizada para descobrir as necessidades que a aplicação pretende abordar e dessa forma elicitar os Requisitos
<div/>
<p/>

**Legendas**
* N: Necessidade
* RF: Requisito Funcional
* RNF: Requisito não Funcional

### Necessidades

ID|Necessidade|Prioridade|Problema|Solução Atual|Solução Proposta
|--|--|--|--|--|--|
|N1|Doar objetos que não tem mais serventia|X|Acúmulo de objetos sem utilidade|Procurar instituições ou pessoas aceitando doações pessoalmente|Publicar esses objetos online em uma plataforma que facilite o acesso
|N2|Descobrir objetos que estão sendo doados|X|Não ter dinheiro para comprar um determinado objeto|Procurar instituições ou pessoas oferecendo doações pessoalmente |Procurar objetos necessitados em uma plataforma de fácil acesso
|N3|Necessidade de administração da plataforma|X|Necessidade de verificar as doações, doadores e divulgar campanhas de doação|Gerentes do posto de doações devem verificar presencialmente as doações|Gerentes do posto de doações podem administrar tudo manualmente usando perfil de administrador do sistema|

### Requisitos Funcionais

|ID|Requisitos|Descrição|Necessidade(s)|
|--|--|--|--|
|RF01|Cadastro de Usuário|Registra o usuário no sistema Donner|N1, N2
|RF02|Login de Usuário|Permitir acesso ao sistema de acordo com seu perfil de usuário.|N1, N2
|RF03|Pesquisar doações|Pesquisar doações disponíveis por categoria.| N2
|RF04|Publicar doação|Permitir cadastra doações.|N1
|RF05|Encerrar Doação|Usuário pode encerra a divulgação de uma doação.| N2
|RF06|Logout de Usuário| Desconectar o usuário da aplicação|N1, N2
|RF07|Atualização de perfil do usuário | Permitir que os dados cadastrados relacionados ao perfil do usuário sejam atualizados|N1, N2
|RF08|Comentar em postagens|Usuários logados podem comentar nas postagens de outros usúarios|N1, N2
|RF09| Administrar comentários| O Perfil de administrador pode apagar comentários nas postagens de outros usuários|N3|
|RF10| Administrar postagens| O Perfil de administrador pode apagar postagens de outros usuários|N3|
|RF11| Criar postagem de campanha| O Perfil de administrador pode criar e apagar campanhas de divulgação|N3|
|RF12| Demonstrar interesse|Usuário demostra interesse em alguma doação disponibilizada | N2


### Requisitos não funcionais

|ID|Requisitos não funcionais|Descrição|Necessidade(s)|
|--|--|--|--|
|RNF01| Privacidade do Contato| O sistema deve deixar visível apenas dados autorizados pelo usuário|N1, N2
|RNF02|Usuário não Logado| Usuários não logados podem apenas visualizar as postagens| N2

## Referências

>Woebcken, C. O que é brainstorming e as 7 melhores técnicas para a tomada de decisões inteligentes, 10/07/2019. Disponível em: [https://rockcontent.com/br/blog/brainstorming/](https://rockcontent.com/br/blog/brainstorming/). Data de acesso: 28/07/2021

q    