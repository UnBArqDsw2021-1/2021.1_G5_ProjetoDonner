# Políticas

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   27/07/2021   |  1.0    |  Documento    | Lucas Gabriel |
|   05/08/2021   |  1.1    |  Modificar formatação e padrão de *commits*    | Davi Antônio |

## Introdução

<div style="text-indent: 40px; text-align: justify">
Esse documento contém os padrões, decididos pela equipe, para organização a cerca das contribuições no projeto.
</div>

## Nomeação de arquivos e pastas

<div style="text-indent: 40px; text-align: justify">
Os arquivos e pastas deverão utilizar o padrão <tt>snake_case</tt> para nomeação.
</div>

## Commits

<div style="text-indent: 40px; text-align: justify">
Os <i>commits</i> devem ser escritos em português brasileiro, e devem mencionar no corpo o número da <i>issue</i>  ao qual está relacionado.
</div>

```bash
git commit
```

```
Escrever mensagem de commit padrão
 
A definição de uma mensagem de commit padrão é importante para garantir
a padronização do processo de desenvolvimento.

Por isso, definiu-se esse commit como o padrão, o que impacta o
progresso na issue #<número da issue>.
```

<div style="text-indent: 40px; text-align: justify">
Os <i>commits</i> com de tarefas em pares devem conter o Co-Autor como mostrado no exemplo abaixo:
</div>

```
Título do commit

Parágrafo explicativo 1.

Parágrafo explicativo 2.

Parágrafo explicativo n.

- item de lista 1
- item de lista 2
- item de lista n
 
Co-authored-by: nome-autor <email@xxx.com>
Co-authored-by: nome-autor2 <email2@xxx.com>
```


## Branches

<div style="text-indent: 40px; text-align: justify">
As <i>Branches</i> devem ser nomeadas conforme especificado nesse documento.
</div>

<p></p>

* *Branch* que mantém uma versão estável do projeto
```
master
```

* *Branch* que mantém uma versão atualizada do projeto
```
devel
```

* *Branch* para documentação

```
docs/nome_do_documento
```

* *Branch* para *feature* (funcionalidade)

```
feature/nome_da_feature
```
* *Branch* para *bug* e correções

```
fix/nome_da_feature_corrigida
```


## Pull Request(PR)

<div style="text-indent: 40px; text-align: justify">
Os <i>Pull Requests</i> (PR) devem ser escritos em português brasileiro, de forma clara e suscinta.
</div>

* **Título**: Nome que descreva minimamente do que se trata
* **Descrição**: descrição clara, sobre o que o PR resolve, e as *issues* relacionadas

### Template PR

```
Título do PR

Esse PR resolveu as issues #X #Y:
* Tarefa realizada
* Tarefa realizada 2
```

### Importante

* O *Pull Request* só pode ser aceito após revisão de membros que não participaram no desenvolvimento da *branch*


## Issues

* **Título**: uma breve descrição da tarefa a ser realizada
* **Descrição**: uma descrição detalhada sobre o que deve ser feito para realizar a *issue*
* **Critérios de aceitação**: definir tarefas essenciais para aceitação da *issue*

### Importante

* Todas as *issues* devem ter no minimo um critério de aceitação
* As *issues* dever respeitar a estrutura do *template*

### Template Issue

```
Título

### Descrição
Descrição escrita sobre a issue

### Critérios de aceitação

- [ ] Critério 1
- [ ] Critério 2
- [ ] Critério 3
```