# Boas vindas ao repositório do projeto de Relatório de Estoque!

Você já usa o GitHub diariamente para desenvolver os exercícios, certo? Agora, para desenvolver os projetos, você deverá seguir as instruções a seguir. Fique atento a cada passo e, se tiver qualquer dúvida, nos envie por _Slack_! #vqv 🚀

Aqui você vai encontrar os detalhes de como estruturar o desenvolvimento do seu projeto a partir desse repositório, utilizando uma branch específica e um _Pull Request_ para colocar seus códigos.

---

## Instruções para entregar seu projeto:

### ANTES DE COMEÇAR A DESENVOLVER:

1. Clone o repositório

- `git clone git@github.com:tryber/sd-0x-inventory-report.git`.
- Entre na pasta do repositório que você acabou de clonar:
  - `sd-0x-inventory-report`

2. Crie o ambiente virtual para o projeto

- `python3 -m venv .venv && source .venv/bin/activate`

3. Instale as dependências

- `python3 -m pip install -r requirements.txt`

4. Crie uma branch a partir da branch `master`

- Verifique que você está na branch `master`
  - Exemplo: `git branch`
- Se não estiver, mude para a branch `master`
  - Exemplo: `git checkout master`
- Agora crie uma branch à qual você vai submeter os `commits` do seu projeto
  - Você deve criar uma branch no seguinte formato: `nome-github-nome-do-projeto`
  - Exemplo: `git checkout -b exemplo-inventory-report`

5. Adicione as mudanças ao _stage_ do Git e faça um `commit`

- Verifique que as mudanças ainda não estão no _stage_
  - Exemplo: `git status` (deve aparecer listada a pasta _exemplo_ em vermelho)
- Adicione o novo arquivo ao _stage_ do Git
  - Exemplo:
    - `git add .` (adicionando todas as mudanças - _que estavam em vermelho_ - ao stage do Git)
    - `git status` (deve aparecer listado o arquivo _exemplo/README.md_ em verde)
- Faça o `commit` inicial
  - Exemplo:
    - `git commit -m 'iniciando o projeto inventory-report'` (fazendo o primeiro commit)
    - `git status` (deve aparecer uma mensagem tipo _nothing to commit_ )

6. Adicione a sua branch com o novo `commit` ao repositório remoto

- Usando o exemplo anterior: `git push -u origin exemplo-project-name`

7. Crie um novo `Pull Request` _(PR)_

- Vá até a página de _Pull Requests_ do [repositório no GitHub](https://github.com/tryber/sd-0x-inventory-report/pulls)
- Clique no botão verde _"New pull request"_
- Clique na caixa de seleção _"Compare"_ e escolha a sua branch **com atenção**
- Clique no botão verde _"Create pull request"_
- Adicione uma descrição para o _Pull Request_ e clique no botão verde _"Create pull request"_
- **Não se preocupe em preencher mais nada por enquanto!**
- Volte até a [página de _Pull Requests_ do repositório](https://github.com/tryber/sd-0x-inventory-report/pulls) e confira que o seu _Pull Request_ está criado

---

## Entregáveis

Para entregar o seu projeto você deverá criar um _Pull Request_ neste repositório. Este _Pull Request_ deverá conter, para aprovação em todos os requisitos, os arquivos `inventory.py`, `importer.py`, `csv_importer.py`, `json_importer.py`, `xml_importer.py`, `simple_report.py`, `complete_report.py`, que conterão seu código `Python`. Atente que os requisitos te orientarão a criar estes arquivos aos poucos.

### ⚠️ É importante que seus arquivos tenham exatamente estes nomes! ⚠️

Você pode adicionar outros arquivos se julgar necessário. Qualquer dúvida, procure a gente no Slack!.

Lembre-se que você pode consultar nosso conteúdo sobre [Git & GitHub](https://course.betrybe.com/intro/git/) sempre que precisar!

---

## O que deverá ser desenvolvido

No projeto passado você implementou algumas funções que faziam leitura e escrita de arquivos JSON e CSV, correto? Neste projeto nós vamos fazer algo parecido, mas orientados pela Programação Orientada a Objeto! Você implementará um gerador de relatórios que recebe arquivos com dados de um estoque e gera, de saída, um relatório acerca destes dados.

Esses dados de estoque poderão ser obtidos de diversas formas, sendo elas:

- Através da importação de um arquivo `CSV`;

- Através da importação de um arquivo `JSON`;

- Através da importação de um arquivo `XML`;

Além disso, o relatório final deverá ser gerável em duas versões: simples e completa.

### Como o projeto deve ser executável

Seu programa deverá ser executável **via linha de comando** com o comando `python3 main.py argumento1 argumento2`:

- O **argumento 1** deve receber o caminho de um arquivo a ser importado. O arquivo pode ser um `csv`, `json` ou `xml`.

- O **argumento 2** pode receber duas strings: `simples` e `completo`, cada uma gerando o respectivo relatório.

---

## Desenvolvimento e testes

Este repositório já contém um _template_ com a estrutura de diretórios e arquivos, tanto de código quanto de teste criados. Veja abaixo:

```
.
├── README.md
├── setup.cfg
├── requirements.txt
├── data
│   ├── inventory_20200823.csv
│   ├── inventory_20200823.json
│   └── inventory_20200823.xml
├── main.py
├── inventory
│   ├── inventory.py
│   └── inventory_iterator.py
├── importer
│   ├── importer.py
│   ├── csv_importer.py
│   ├── json_importer.py
│   └── xml_importer.py
├── reports
│   ├── simple_report.py
│   └── complete_report.py
├── tests
│   ├── main.py
│   ├── inventory.py
│   ├── inventory_iterator.py
│   ├── importer.py
│   ├── csv_importer.py
│   ├── json_importer.py
│   ├── xml_importer.py
│   ├── simple_report.py
│   └── complete_report.py
```

Apesar do projeto já possuir uma estrutura base, você quem deve implementar tanto as funções quanto os testes. Novos arquivos podem ser criados conforme a necessidade.

Para executar os testes, lembre-se de primeiro **criar e ativar o ambiente virtual**, além de também instalar as dependências do projeto. Isso pode ser feito através dos comandos:

```bash
$ python3 -m venv .venv

$ source .venv/bin/activate

$ python3 -m pip install -r requirements.txt
```

O arquivo `requirements.txt` contém todos as dependências que serão utilizadas no projeto, ele está agindo como se fosse um `package.json` de um projeto `Node.js`. Com as dependências já instaladas, para executar os testes basta usar o comando:

```bash
$ python3 -m pytest
```

Se quiser saber mais sobre a instalação de dependências com `pip`, veja esse artigo: https://medium.com/python-pandemonium/better-python-dependency-and-package-management-b5d8ea29dff1

Para verificar se você está seguindo o guia de estilo do Python corretamente, você pode executá-lo com o seguinte comando:

```bash
$ python3 -m flake8
```

---

## Dados

### Importação de dados de estoque

Arquivos de exemplo nos três formatos de importação estão disponíveis no diretório `data` deste repositório.

### Relatório simples

O relatório simples deve gerar, na linha de comando, os seguintes dados:

```json
TODO: TBD
```

### Relatório completo

O relatório completo deve gerar, na linha de comando, os seguintes dados:

```json
TODO: TBD
```


# TODO: Remove this

1- Importar CSV na classe Estoque (TODO: definir formato e dar arquivos de teste)
2- Importar JSON na classe Estoque (TODO: definir formato e dar arquivos de teste)
3- Classe abstrata "Importador", 2-3 classes especificas "CSVImporter", "JSONImporter", usando composição pra juntar com a classe Estoque
4- Implementar um iterator na classe estoque (TODO: ver o precisa pra implementar um iterator)
5- Exportador simples em CSV (TODO: definir formato)
6- Exportador complexo em CSV usando herança (TODO: definir formato)
7- (BONUS) 90% de cobertura

---

## Requisitos obrigatórios:

#### 1 - Deve haver uma função `generate` numa classe `SimpleReport` do módulo `simple-report`. Essa função deverá receber dados numa estrutura `dict` e deverá gerar uma saída para a linha de comando.

##### As seguintes verificações serão feitas:

- A função deve receber de parâmetro um dict no seguinte formato:

```python
TODO: TBD
```

- A função deverá gerar, na linha de comando, uma saída com o seguinte formato:

```bash
TODO: TBD
```

#### 2 - Deve haver uma função `generate` numa classe `CompleteReport` do módulo `complete-report`. Essa função deverá receber dados numa estrutura `dict` e deverá gerar uma saída para a linha de comando.

##### As seguintes verificações serão feitas:

- A função deve ser herdeira da classe `SimpleReport`, de modo a especializar seu comportamento.

- A função deve receber de parâmetro um dict no seguinte formato:

```python
TODO: TBD
```

- A função deverá gerar, na linha de comando, uma saída com o seguinte formato:

```bash
TODO: TBD
```

#### 3 - Deve haver uma função `import` dentro de uma classe `Inventory` do módulo `inventory`, capaz de ler um arquivo CSV passado como parâmetro de linha de comando

##### As seguintes verificações serão feitas:

- A função, quando receber um arquivo CSV, deve chamar a função de gerar relatório correspondente à entrada passada, `simples` ou `completo`, com os dados importados corretamente passados por parâmetro a elas.

#### 4 - Deve haver uma função `import` dentro de uma classe `Inventory` do módulo `inventory`, capaz de ler um arquivo JSON passado como parâmetro de linha de comando

##### As seguintes verificações serão feitas:

- A função, quando receber um arquivo JSON, deve chamar a função de gerar relatório correspondente à entrada passada, `simples` ou `completo`, com os dados importados corretamente passados por parâmetro a elas.

#### 5 - Deve haver uma função `import` dentro de uma classe `Inventory` do módulo `inventory`, capaz de ler um arquivo XML passado como parâmetro  de linha de comando

##### As seguintes verificações serão feitas:

- A função, quando receber um arquivo XML, deve chamar a função de gerar relatório correspondente à entrada passada, `simples` ou `completo`, com os dados importados corretamente passados por parâmetro a elas.

#### 6 - Deve haver uma classe abstrata `Importer` no módulo import. Deve haver três classes herdeiras desta: `CsvImporter`, `JsonImporter` e `XmlImporter`, cada uma definida em seu respectivo módulo.

##### As seguintes verificações serão feitas:

- A classe abstrata deve definir uma função de cabeçalho `import` a ser implementado por cada classe herdeira. Ela deve receber como parâmetro o nome do arquivo a ser importado.

- A função import definida por cada classe herdeira deve lançar uma exceção caso a extensão do arquivo passado por parâmetro seja inválida (por exemplo, quando se passa um `csv` para o `JsonImporter`).

- A função deverá ler os dados do arquivo passado e retorná-los estruturados em um `dict`. Por exemplo:

```python
TODO: TBD
```

#### 7 - Deve haver uma classe `InventoryIterator` no módulo `inventory-iterator`, que implementa a interface de um iterator. A classe `Inventory` deve implementar o método `__iter__` associado a essa classe.

##### As seguintes verificações serão feitas:

- As classes `InventoryIterator` e `Inventory` devem implementar corretamente a interface de um iterator, de modo que o código abaixo nos dê o primeiro item do dicionário de dados importados:

```python
# ... Acima, um código que instancia e importa um arquivo para a variável `inventory`

iterator = iter(inventory)
first_item = next(iterator)
```


## Requisitos bônus:

#### 8 - A cobertura de testes do projeto deve ser de no mínimo 90%.

##### As seguintes verificações serão feitas:

- Todos os testes que envolvem mensagens na saída padrão ou de erro, devem ter sua saída redirecionada para Fakes com `StringIO`;

- Todos os testes que envolvem manipulação de arquivos criam Fakes com `StringIO`;

- Todas as requisições externas a uma classe utilizam _Mocks_;

- A cobertura de testes é de no mínimo 90%.

---

### DURANTE O DESENVOLVIMENTO

- Faça `commits` das alterações que você fizer no código regularmente

- Lembre-se de sempre após um (ou alguns) `commits` atualizar o repositório remoto

- Os comandos que você utilizará com mais frequência são:
  1. `git status` _(para verificar o que está em vermelho - fora do stage - e o que está em verde - no stage)_
  2. `git add` _(para adicionar arquivos ao stage do Git)_
  3. `git commit` _(para criar um commit com os arquivos que estão no stage do Git)_
  4. `git push -u nome-da-branch` _(para enviar o commit para o repositório remoto na primeira vez que fizer o `push` de uma nova branch)_
  5. `git push` _(para enviar o commit para o repositório remoto após o passo anterior)_

---

### DEPOIS DE TERMINAR O DESENVOLVIMENTO (OPCIONAL)

Para sinalizar que o seu projeto está pronto para o _"Code Review"_ dos seus colegas, faça o seguinte:

- Vá até a página **DO SEU** _Pull Request_, adicione a label de _"code-review"_ e marque seus colegas:

  - No menu à direita, clique no _link_ **"Labels"** e escolha a _label_ **code-review**;

  - No menu à direita, clique no _link_ **"Assignees"** e escolha **o seu usuário**;

  - No menu à direita, clique no _link_ **"Reviewers"** e digite `students`, selecione o time `tryber/students-sd-0x`.

Caso tenha alguma dúvida, [aqui tem um video explicativo](https://vimeo.com/362189205).

---

### REVISANDO UM PULL REQUEST

Use o conteúdo sobre [Code Review](https://course.betrybe.com/real-life-engineer/code-review/) para te ajudar a revisar os _Pull Requests_.

#VQV 🚀
