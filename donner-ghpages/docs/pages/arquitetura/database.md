# Banco de Dados

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   10/10/2021   |  1.0    |  Criação do Documento | Davi Antônio, Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues  | 
|   15/10/2021   |  1.1    | Atualização da introdução   | Hugo Bezerra, Lucas Rodrigues |

## Introdução
<div style="text-indent: 40px; text-align: justify">
Em relação ao banco de dados da nossa aplicação, iremos utilizar o Firebase e com isso a implementação do banco de dados e feita com o "Cloud Firestore que é um banco de dados de documentos NoSQL que permite armazenar, sincronizar e consultar dados facilmente para seus apps para dispositivos móveis e da Web, em escala global".


A base será composta por 5 categorias de documentos, sendo eles Users, Posts, Comments, Categories e Campaigns, onde um anúncio pertence a um usuário dono e um usuário pode possuir múltiplos anúncios (Posts). Esse relacionamento também pode ser observado no <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_comunicacao">Diagrama de Comunicação</a>.

|Users|Posts|Comments|Categories|Campaigns|
|--|--|--|--|--|
|city|categoryId|id|id|id|
|description|description|owner|description|description|
|email|id|post||start|
|id|isDonation|text||end|
|name|owner|||title|
|phone|title|
|photoUrl|
|state|

</div>

## Esquema do banco de dados
O Banco de Dados utilizado é o Cloud Firestore, banco de dados não relacional oferecido no serviço Firebase, provido pelo Google.

### Coleção Users
A coleção de usuários guarda os documentos com os dados necessários de todos os usuários registrados na aplicação por meio de um login Google

| Atributo | Tipo | Descrição |
|--|--|--|
| city | string | cidade |
| description | string | texto opcional |
| email | string | email do usuário |
| id | string | id do documento na base |
| name | string | nome completo do usuário |
| phone | string | telefone de contato |
| photoUrl | string | URL da foto (fornecida pelo login Google)|
| state | string | estado do Brasil em que reside o usuário |

### Coleção Posts
Guarda documentos referentes aos pedidos de doação ou objetos oferecidos pelos usuários

| Atributo | Tipo | Descrição |
|--|--|--|
| categoryId | string | id da categoria da postagem na base |
| description | string | descrição do item doado ou solicitado
| id | string | id do documento na base |
| isDonation | boolean | caso verdadeiro, a postagem é uma doação |
| owner | string | id do usuário que escreveu a postagem |
| title | string | título da postagem |

### Coleção Comments
Comentários postados pelos usuários registrados nas postagens existentes

| Atributo | Tipo | Descrição |
|--|--|--|
| id | string | id do documento na base |
| owner | string | id do usuário que postou o comentário |
| post | string | id do post ao qual o comentário pertence |
| text | string | conteúdo do comentário |

### Coleção Categories
Guarda as categorias que uma postagem pode envolver

| Atributo | Tipo | Descrição |
|--|--|--|
| id | string | id do documento na base |
| description | string | descrição da categoria |

### Coleção Campaigns
Campanhas criadas por usuários administradores

| Atributo | Tipo | Descrição |
|--|--|--|
| id | string | id do documento na base |
| description | string | descrição da campanha
| start | timestamp | data de início da campanha |
| end | timestamp | fim da campanha |
| title | string | título da campanha |

## Referências
> Google. Uso e limites do Firebase Cloud Firestore. Disponível em: [https://firebase.google.com/docs/firestore/quotas](https://firebase.google.com/docs/firestore/quotas). Acesso em: 08/10/2021.

> Google. Plano de preços do Firebase. Disponível em: [https://firebase.google.com/pricing/](https://firebase.google.com/pricing/). Acesso em: 08/10/2021