# GOFs Criacionais

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   03/09/2021   |  1.0    |  Criação do Documento  | Hugo Bezerra, Lucas Rodrigues, Marcos Adriano |
|   14/09/2021   |  1.1    |  Adição das imagens  | Hugo Bezerra, Kleidson, Lucas Rodrigues, Lucas Gabriel |
|   15/09/2021   |  1.2    |  Adição Singleton  | Kleidson, Gabriel Batalha, Lucas Gabriel, Lucas Rodrigues |
|   15/09/2021   |  1.3    |  Adição Prototype  | Davi Antônio |
|   16/09/2021   |  1.4    |  Corrigir erros ortográficos e melhorar referencial teórico  | Davi Antônio |
|   19/09/2021   |  1.5    |  Revisão do documento e remoção do Singleton | Kleidson, Gabriel Batalha, Lucas Gabriel, Lucas Rodrigues |

## Factory Method
### Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
O Factory Method é um dos GoFs criacionais e é descrito no livro (Design Patterns: Elements of Reusable Object-Oriented Software) da seguinte maneira: define uma interface para a criação de objetos e deixa para a subclasse a decisão de qual classe instanciar.
</p>

</div>

### Modelagem
![](https://i.imgur.com/LrYUoMA.png)

Autores: Gabriel Batalha, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues

### Aplicação
[![](https://i.imgur.com/LuZGowZ.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/widgets/button_widget/custom_button.dart)

[![](https://i.imgur.com/MfEUvbL.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/widgets/button_widget/custom_icon_button.dart)

[![](https://i.imgur.com/BwgyrqL.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/widgets/button_widget/custom_text_button.dart)

[![](https://i.imgur.com/hGE1qv8.png)](https://github.com/UnBArqDsw2021-1/2021.1_G5_ProjetoDonner_Front-end/blob/GOFs/donner/lib/widgets/button_widget/factory_button.dart)


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

## Prototype

<div style="text-indent: 40px; text-align: justify">
<p>
O padrão de protótipo cria novos objetos a partir de um objeto original ou base, o chamado protótipo, que implementa um método de clonagem que pode ou não especificar o estado desejado. Segundo JOHNSON, Eric et al., esse padrão é adequado para criar objetos com poucos estados possíveis dinamicamente, já que nessa situação não é necessária a complexidade adicionada com o uso de hierarquias com fábricas.
</p>
</div>

### Modelagem

![](https://i.imgur.com/cph7IBb.png)

(JOHNSON, Eric et al.; 1995)

<div style="text-indent: 40px; text-align: justify">
<p>
Há muitas maneiras de se implementar esse padrão. Algumas implementações, sugeridas pelo livro Design Patterns (JOHNSON, Eric et al.; 1995), possuem maior complexidade, assemelhando-se a uma fábrica, permitindo a instância de classes a partir de um repositório de protótipos disponíveis.
</p>
</div>

### Exemplo

<div style="text-indent: 40px; text-align: justify">
<p>
O exemplo autoral a seguir é uma adaptação do padrão *Prototype*. A classe não realiza uma interface ou estende uma classe abstrata com um método de clonagem. Entretanto, o método de clonagem permite que um cliente especifique, usando os parâmetros nomeados da linguagem Dart, o estado desejado do objeto que será criado como clone.
</p>
</div>

``` dart
class SignInFormModel {
  final String email;
  final String password;
  final bool isLoading;

  SignInFormModel({
    this.email = "",
    this.password = "",
    this.isLoading = false,
  });

  bool get canSubmit => email.isNotEmpty && password.isNotEmpty && !isLoading;

  SignInFormModel copyWith({
    String email,
    String password,
    bool isLoading,
  }) {
    return SignInFormModel(
        email: email ?? this.email,
        password: password ?? this.password,
        isLoading: isLoading ?? this.isLoading);
  }
```

<div style="text-indent: 40px; text-align: justify">
<p>
Nessa implementação, um parâmetro nomeado que não é informado não modifica o atributo referente a ele. Isso possibilita a redução nas criação de objetos para atributos, já que um atributo não modificado simplesmente utilizará a referência do objeto original.
</p>
</div>

## Referências
> PADRÕES de PROJETO. Disponível em: https://refactoring.guru/pt-br/design-patterns. Data de acesso: 03/09/2021

> PADRÕES Gof. Disponível em: http://www.facom.ufu.br/~bacala/ESOF/05b-Padrões%20Gof.pdf. Data de acesso: 03/09/2021

> Design Patterns: Padrões “GoF”. Disponível em: https://www.devmedia.com.br/design-patterns-padroes-gof/16781. Data de acesso: 03/09/2021

> Flutter Design Patterns: 10 — Factory Method. Disponível em:[https://medium.com/flutter-community/flutter-design-patterns-10-factory-method-c53ad11d863f](https://medium.com/flutter-community/flutter-design-patterns-10-factory-method-c53ad11d863f). Data de acesso: 10/09/2021

>Flutter Design Patterns: 1 — Singleton. Disponível em: [https://medium.com/flutter-community/flutter-design-patterns-1-singleton-437f04e923ce](https://medium.com/flutter-community/flutter-design-patterns-1-singleton-437f04e923ce). Data de acesso: 14/09/2021

>Singleton em TypeScript. Disponível em: [https://refactoring.guru/pt-br/design-patterns/singleton/typescript/example#lang-features](https://refactoring.guru/pt-br/design-patterns/singleton/typescript/example#lang-features). Data de acesso: 14/09/2021

> JOHNSON, Eric et al. Design Patterns: Elements of Reusable Object-Oriented Software. 1995.