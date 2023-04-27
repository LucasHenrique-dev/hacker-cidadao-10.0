# 🚮♻️🤖 [NOME LEGAL DO PROJETO]

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black)

## ℹ Tabela de Conteúdos
- [Descrição do Projeto](#dart-projeto-da-cadeira-de-compiladores-20222)
- [Especificações](#-especificações-do-projeto)
- [Como Usar](#-como-usar-a-dsl-no-codespaces)

## :dart: Projeto Hacker Cidadão - Desafio 4

Desafio: Geração de um novo ecossistema econômico na cidade baseado no upcycling, estimulando a inovação e o empreendedorismo e criando novas oportunidades de trabalho para população.

## 📃 Especificações do Projeto

Especificações incluem:
- espec1
- espec2

Visualize as especificações do projeto: [Especificações Gerador Gráfico de Relatório](especificacoes)

## ☕ Como Usar PROJETO no Codespaces

Para usar PROJETO, siga estas etapas:

1. Crie um codespace:
    * Clique em "Code" e depois na opção "Create codespace on <branch>", onde <branch> é a branch em que se está trabalhando no momento </br>
    ![Criação do Codespace](images/criar-codespace.png)
1. Compilar a descrição da linguagem fonte:
    * Use o seguinte comando
      ```shell
      java -jar antlr.jar -o src-gen GeradorRelatorio.g4
      ```
      > O comando acima executa o gerador ANTLR que converte a descrição da gramática (Expr.g4) em programas Java (Analisadores léxicos e sintáticos). Os códigos dos analisadores gerados serão armazendados na pasta src-gen.
1. Compilar programas em Java:
   * Use o seguinte comando
      ```shell
      javac -cp antlr.jar:fillo.jar:. -d classes src/*.java src-gen/*.java
      ```
      > O comando acima executa o compilador Java. O arquivo antlr.jar, que contem as bibliotecas runtime utilizadas pelo código gerado pelo antlr são adicionadas ao CLASSPATH, assim como fillo.jar para poder utilizar a API de Excel para Java. O compilador compila todos os arquivos java que estão no diretório "src" (arquivo escritos pelo programador) e no diretório "src-gen" (arquivos gerados automáticamente). Os arquivos binários compilados gerados pelo javac serão armazenados no diretório classes.

1. Executar o programa:
   * Use o seguinte comando
     ```shell
     java -cp antlr.jar:fillo.jar:classes Main
     ```
     > O comando acima executa a classe Main do compilador. Os arquivos binários das classes estão localizades no diretório "classes". Para a classe poder ser executada é necessário também incluir os arquivos do runtime do antlr.jar e fillo.jar.

## 📝 Licença

Esse projeto está sob licença. Veja o arquivo [LICENÇA](LICENSE) para mais detalhes.

[⬆ Voltar ao topo](#%EF%B8%8F-gerador-gráfico-de-relatório)<br>

