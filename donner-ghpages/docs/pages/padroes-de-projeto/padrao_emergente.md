# Padrão Emergente

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   13/09/2021   |  1.0    |  Criação do documento    | Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Gabriel e Lucas Rodrigues
|   19/09/2021   |  1.1    |  Aplicação do Lazy Load    | Davi Antônio, Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan

## Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
<i>Lazy Load</i> (carregamento preguiçoso), é um padrão de projeto que é muito utilizado no desenvolvimento de software e consiste em atrasar a inicialização de um objeto até que ele seja necessário. O objetivo do <i>Lazy load</i> é melhorar o desempenho da aplicação, principalmente aquelas que fazem carregamentos massivos de dados, carregando os dados conforme seja necessário. Dessa forma, a sua utilização pode reduzir o tempo de carregamento, além de conservar largura de banda e alguns recursos do sistema, tanto do servidor quanto do cliente.
</p>

<p>
Existem basicamente 4 formas de se implementar o <i>Lazy Load</i>, sendo elas,<i>virtual proxy</i>, <i>value holder</i>, <i>ghost</i>, e <i>lazy initialization</i>. Os nossos estudos focaram na <i>Lazy Initialization</i>.
</p>
</div>

### Lazy Initialization

<div style="text-indent: 40px; text-align: justify">
<p>
<i>Lazy initialization</i> (inicialização preguiçosa), é uma das formas de implementação do <i>Lazy Load</i> e se consiste em uma tática de atraso na criação de um objeto até o momento em que seja necessário, isso é feito a partir da implementação de uma função que irá checar primeiro se aquele objeto é nulo e em caso afirmativo irá calcular as propriedades do objeto e criá-lo durante a execução da função.
</p>

<p>
Ao utilizar o <i>lazy initialization</i> obtemos duas características importantes, o atraso de uma operação custosa até o momento em que ela se torna extremamente necessária e salvando o resultado garantimos que não vamos precisar realizar aquela mesma operação novamente.
</p>
<p>
O <i>lazy initialization</i> está sendo implementado, a seguir, como um exemplo <i>toy</i>. A Linguagem Dart tem um modificador <i>late</i> que tem como funcionamento especial implementar o <a href='https://dart.dev/null-safety/understanding-null-safety#lazy-initialization'> lazy initialization </a>.
</p>
<p>
No exemplo <i>toy</i>, na classe <i>CategoryScreen</i> o <i>late</i> é aplicado para a variável <i>Firestore Instance</i> de forma que ela só é inicializada na primeira vez que for acessada, o que caracteriza o <i>lazy initialization</i>.
</p>
</div>

### Modelagem

![](https://i.imgur.com/KHjzu7k.png)


### Exemplo Toy

```dart
class CategoryScreen extends StatelessWidget {
    const CategoryScreen({ Key? key }) : super(key: key);
    late final FirebaseFirestore firestoreInstance;
    @override
    Widget build(BuildContext context) {
       firestoreInstance = FirebaseFirestore.instance;
       return FutureBuilder <QuerySnapshot>(
          future: firestoreInstance.collection('produtos').get(),
          builder: (context, snapshot){
            if(!snapshot.hasData)
              return Center(child: CircularProgressIndicator());
            else{
              var dividedTiles = ListTile.divideTiles(
                tiles: snapshot.data!.docs.map(
                  (doc){
                   return CategoryTile(doc);
                  }
                ).toList(),
                color: Colors.grey).toList();
              return ListView(
                children: dividedTiles
              );
            }
          }
        );
      }
    }
```
### Outras implementações

<div style="text-indent: 40px; text-align: justify">
<p>
Falando simplificadamente sobre as outras formas de implementação do <i>Lazy Load</i>, temos que o <i>virtual proxy</i>  é um método que consiste em, quando acessar um objeto, chamar um objeto virtual com a mesma interface do objeto real. Quando o objeto virtual é chamado, carrega-se o objeto real, depois delega para ele.  
</p>
<p>
O método <i>ghost</i> consistem em carregar um objeto em um estado parcial, apenas usando um identificador. Então, quando uma propriedade do objeto for chamado pela primeira vez, carregue os dados completos. 
</p>
<p>
O método <i>value holder</i> consiste em criar um objeto genérico que lida com o comportamento do carregamento preguiçoso. Este objeto deve aparecer no lugar dos campos de dados de um objeto. 
</p>
</div>


## Referências
> FOWLER, Martin. Patterns of Enterprise Application Architecture. Addison-Wesley, 2002.

> Null safety - Lazy initialization. Disponível em: [https://dart.dev/null-safety/understanding-null-safety#lazy-initialization](https://dart.dev/null-safety/understanding-null-safety#lazy-initialization). Data de acesso 19/09/2021

> Lazy initialization. Disponível em:
[https://en.wikipedia.org/wiki/Lazy_initialization](https://en.wikipedia.org/wiki/Lazy_initialization). Data de acesso: 13/09/2021

> Lazy Initialization. Disponível em: [http://www.javapractices.com/topic/TopicAction.do?Id=34](http://www.javapractices.com/topic/TopicAction.do?Id=34). Data de acesso: 13/09/2021

> What is Lazy Loading. Disponível em: [https://www.imperva.com/learn/performance/lazy-loading/](https://www.imperva.com/learn/performance/lazy-loading/). Data de Acesso: 13/09/2021

> Lazy loading. Disponível em:
[https://pt.wikipedia.org/wiki/Lazy_loading](https://pt.wikipedia.org/wiki/Lazy_loading). Data de Acesso: 13/09/2021
