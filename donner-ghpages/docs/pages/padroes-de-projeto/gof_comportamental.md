# GOFs Comportamentais

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   03/09/2021   |  1.0    |  Criação do Documento  | Gabriel Batalha, Hugo Ricardo, Lucas Rodrigues, Marcos Adriano
|   19/09/2021   |  1.1    |  Adicionando GoFs *Observer* e *Template Method* | Davi Antônio, Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan
|   20/09/2021   |  1.2    |  Revisão do Documento | Davi Antônio, Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan

## Observer

### Introdução

<div style="text-indent: 40px; text-align: justify">
O Observer é um padrão de projeto que pode ser utilizado como um serviço de assinatura para objetos. Uma classe observa outra, procurando ser informada de uma mudança para tomar uma ação relevante.

</div>

<div style="text-indent: 40px; text-align: justify">
Utilizaremos um exemplo toy para demonstrar o uso do padrão de projeto Observer. Dentro do escopo do projeto, as doações precisam ser classificadas e categorizadas para facilitar a pesquisa dos usuários, como as doações são armazenadas em um banco de dados é preciso aguardar a requisição dos dados. Dessa maneira, funções que podem demorar para entregar sua resposta serão observadas por objetos responsáveis por decidir qual ação será tomada de acordo com os valores recebidos.
</div>

<div style="text-indent: 40px; text-align: justify">
No exemplo a seguir, as funções assíncronas retornam objetos genéricos do tipo Future, e esses valores são  observados por objetos FutureBuilder.
</div>

### Modelagem

![](https://i.imgur.com/onv7Xhf.png)

### Exemplo Toy

``` dart
  FutureBuilder<List<CategoryModel>>(
    future: widget.database.categories(),
    builder: (BuildContext context, AsyncSnapshot<dynamic> snapshot) {
      if (snapshot.hasData) {
        final List<CategoryModel> items = snapshot.data;
        if (items.isNotEmpty) {
          return ListView.separated(
              itemBuilder: (context, index) => Card(
                      child: Row(
                    mainAxisAlignment: MainAxisAlignment.start,
                    children: [
                      Icon(
                        items[index].icon,
                        color: AppColors.primary,
                      ),
                      const SizedBox(
                        width: 25.0,
                      ),
                      Text(
                        items[index].name,
                        style: AppTextStyles.bodyText,
                      )
                    ],
                  )),
              separatorBuilder: (context, index) => Divider(
                    height: 0.5,
                  ),
              itemCount: items.length);
        } else {
          return Center(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[
                Text("No categories on database"),
                Text("No categories found")
              ],
            ),
          );
        }
      } else if (snapshot.hasError) {
        return Center(child: Text(snapshot.error.toString()));
      } else {
        return CircularProgressIndicator();
      }
    },
  );
```



## Template Method

### Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
O padrão de projeto <i>Template Method</i> se baseia em definir um esqueleto padrão para um algoritmo subdividido em vários outros métodos que devem ser sobrescritos conforme surge a necessidade. 
</p>
<p>
Para demonstrar o uso do Template Method, utilizaremos um exemplo toy. No exemplo, utilizamos uma modelagem na qual Campaign e Announcement herdam da classe Post e assim como é definido o Template Method ocorre a sobrescrita dos métodos conforme necessário para diferenciar a Campaign e Announcement.
</p>
</div>

### Modelagem

![](https://i.imgur.com/EVPqsBz.png)


### Exemplo Toy


```dart
abstract class Post {
  alter() {
    var post = getData();
    post = updateData(post);
  }

  getData();
  updateData(Post post);
}
```

```dart
class Announcement extends Post {
  String owner;
  String description;
  List<String> photos;

  Announcement({
    required this.owner,
    required this.description,
    required this.photos,
  });

  alterDescription() {}

  addPhotoUrl() {}

  updateData(post) {
    addPhotoUrl();
    alterDescription();
  }

  @override
  getData() {
    return {owner, description, photos};
  }
}
```

```dart
class Campaign extends Post {
  String admin;
  String description;
  DateTime startDate;
  DateTime endDate;

  Campaign({
    required this.admin,
    required this.description,
    required this.startDate,
    required this.endDate,
  });

  alterDate() {
    startDate = DateTime(2021);
    endDate = DateTime(2021);
  }

  @override
  getData() {
    return {admin, description, startDate, endDate};
  }

  @override
  updateData(post) {
    alterDate();
  }
}
```

## Referências
> Template Method. Disponível em: [https://refactoring.guru/pt-br/design-patterns/template-method](https://refactoring.guru/pt-br/design-patterns/template-method). Data de acesso: 03/09/2021

> Observer. Disponível em: [https://refactoring.guru/pt-br/design-patterns/observer](https://refactoring.guru/pt-br/design-patterns/observer). Data de acesso: 03/09/2021

> Padrão de Projeto Observer em Java. Disponível em: [https://www.devmedia.com.br/padrao-de-projeto-observer-em-java/26163](https://www.devmedia.com.br/padrao-de-projeto-observer-em-java/26163). Data de acesso: 03/09/2021

> Design Patterns: Padrões “GoF”. Disponível em: [https://www.devmedia.com.br/design-patterns-padroes-gof/16781](https://www.devmedia.com.br/design-patterns-padroes-gof/16781). Data de acesso: 03/09/2021

> Flutter Design Patterns: 3 — Template Method. Disponível em: [https://medium.com/flutter-community/flutter-design-patterns-3-template-method-89799d84e378](https://medium.com/flutter-community/flutter-design-patterns-3-template-method-89799d84e378). Data de acesso: 19/09/2021 

> Padrão de Projeto Template Method em Java. Disponível em: [https://www.devmedia.com.br/padrao-de-projeto-template-method-em-java/26656](https://www.devmedia.com.br/padrao-de-projeto-template-method-em-java/26656). Data de acesso: 19/09/2021