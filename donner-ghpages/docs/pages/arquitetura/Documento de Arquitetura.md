# Documento de Arquitetura

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   30/09/2021   |  1.0  |  Criação do Documento  | Gabriel Batalha, Lucas Rodrigues

## 1. Introdução

### 1.1 Propósito
Esse documento tem o objetivo de oferecer uma visão geral da arquitetura do sistema de software Donner, buscando representar as decisões arquiteturais significativas que foram tomadas pela equipe. Para representar os aspectos do sistema a equipe utilizou diferentes visões da arquitetura.

### 1.2 Escopo
O escopo desse documento é o Projeto Donner como um todo, permitindo uma melhor entendimento do sistema e da construção de sua arquitetura.

### 1.3 Definições, Acrônimos e Abreviações

### 1.4 Visão Geral
O documento vai estar organizado da seguinte forma:
1. Introdução
2. Representação Arquitetural
3. Objetivos Arquiteturais e Restrições
4. Visão Lógica
5. Visão de Implementação
6. Visão de Dados
7. Tamanho e Desempenho
<!-- 
Incompleto
-->
## 2. Representação Arquitetural
<!-- 
This section describes what software architecture is for the current system, and how it is represented. Of the Use-Case, Logical, Process, Deployment, and Implementation Views, it enumerates the views that are necessary, and for each view, explains what types of model elements it contains.
-->

## 3. Objetivos Arquiteturais e Restrições
<!-- 
This section describes the software requirements and objectives that have some significant impact on the architecture; for example, safety, security, privacy, use of an off-the-shelf product, portability, distribution, and reuse. It also captures the special constraints that may apply: design and implementation strategy, development tools, team structure, schedule, legacy code, and so on.
-->
## 4. Visão Lógica

### Diagrama de Classe
Foi utilizado, para mostrar as classes significativas, seus relacionamentos, métodos e atributos, o Diagrama de Classe. Abaixo pode ser vista a versão mais recente do diagrama e a versão completa pode ser vista na aba [Diagrama de Classe](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_classe/).
[![](https://i.imgur.com/Sy8te4n.png)](https://i.imgur.com/Sy8te4n.png)

### Diagrama de Sequência
No diagrama de sequência pode ser visualizada a interação entre os objetos do sistema e a ordem na qual as interações ocorrem. Os diagramas de sequência podem ser encontrados na aba [Diagrama de Sequencia](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_sequencia/).

Diagrama de Sequência: Administração de Postagens
[![](https://i.imgur.com/UWS9xMC.png)](https://i.imgur.com/UWS9xMC.png)

### Diagrama de Comunicação
O diagrama de comunicação foi utilizado para mostrar a interação entre diferentes partes do sistema. Apesar desse tipo de diagrama ser semelhante ao diagrama de sequência, ele possui foco na estrutura das mensagens transmitidas entre os objetos. Abaixo é mostrada o diagrama de comunicação da interação sobre os anúncios. Os outros diagramas podem ser encontrados na aba [Diagramas de Comunicação](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_comunicacao/).

Diagrama de Comunicação: Interação Anúncios
[![](https://i.imgur.com/JouiJCc.png)](https://i.imgur.com/JouiJCc.png)

### Diagrama de Pacotes
Para ter uma visão geral das camadas envolvidas na aplicação foi utilizado o Diagrama de Modelo, que é um diagrama estrutural auxiliar do Diagrama de Pacotes. A página completa pode ser encontrada a aba [Diagrama de Pacotes](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_pacotes/).
[![](https://i.imgur.com/UQaAgnS.png)](https://i.imgur.com/UQaAgnS.png)


## 5. Visão de Implementação

### Diagrama de Componentes
Para a compreensão dos relacionamentos entre os componentes que constituem o sistema e de como cada componente interage com o restante do sistema foi utilizado o diagrama de componentes.
[![](https://i.imgur.com/GDI3YTT.png)](https://i.imgur.com/GDI3YTT.png)


<!-- 
Talvez mudar para introdução?
-->
## Referências

> Documento de Arquitetura de Software. Disponível em [http://www.facom.ufu.br/~flavio/pds1/files/2016-01/Documento%20de%20Arquitetura%20de%20Software%20do%20SPEU%201-Exemplo-RUP.pdf](http://www.facom.ufu.br/~flavio/pds1/files/2016-01/Documento%20de%20Arquitetura%20de%20Software%20do%20SPEU%201-Exemplo-RUP.pdf). Data de acesso: 30/09/2021

> Artefato: Documento de Arquitetura de Software. Disponível em : [https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/workproducts/rup_software_architecture_document_C367485C.html](https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/workproducts/rup_software_architecture_document_C367485C.html). Data de acesso: 30/09/2021