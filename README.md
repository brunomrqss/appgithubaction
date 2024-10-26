## Github Action com CI/CD Pipeline

**Github action** é uma ferramenta de automação que permite desenvolvedores a automatizar tarefas relacionadas ao seu ciclo de desenvolvimento de software, permitindo também customizar esses ciclos de trabalho que podem ser influenciados por diferentes eventos ou ações, como: push para um repositório remoto, um pull request e ate mesmo eventos agendados. Pode-se utilizar esses fluxos de trabalho (workflows) para vários propósitos, incluindo: CI/CD, teste, entre outros.

* **Continuous Integration (CI):** continuous integration (integração continua) é a pratica em que desenvolvedores podem mesclar as mudanças do seu código dentro do repositório compartilhado e que cada mudança é influenciada por uma estrutura de automação que garante que determinada mudança no código, são irá quebrar toda a funcionalidade existente em determinada aplicação.
  * e.g
  
  1. dev A - fazendo tarefa A 
  2. dev B - fazendo tarefa B
  
  Criam uma branch do projeto principal com o nome tarefaA e tarefaB, cria test cases e a build do projeto (estrutura), realiza o pullrequest para que seja feito os testes para não quebrar a aplicação. sendo que isso também deve ser feito entre os desenvolvedores para que não haja conflito nas alterações deles.

* **Continuous Deployment (CD):**

* **Workflows**: é uma serie de etapas, praticas e ferramentas que um desenvolvedor ou sua equipe de desenvolvedores seguem para escrever, testar e colaborar entre si e entregar o código de forma eficiente. esse fluxo de tarefas é desenhado de forma simplificada durante o processo de desenvolvimento de software que tem como objetivo melhorar a produtividade, eficiência do trabalho e minimizar erros. o fluxo de trabalho incorpora vários estágios de desenvolvimento desde a parte inicial, até o processo de entrega do produto. integrando também ferramentas de versionamento de código, revisão de código (code review), testes e CI/CD.

### Etapas de um Workflow (exemplo simples):

1. Coding
    * Escolha da IDE => Visual Studio Code
    * Escolha da linguagem de programação => Python
    * Padrões de Código ou de Projeto => Best Practices and Design Patterns

2. Version Control
    * Git
    * Gerenciamento da base de código
    * Colaboração de vários desenvolvedores: padrões de commit, criação de branchs, push, pull requests, resolução de conflitos de código...

3. Code Review
      * Revisão do código e da qualidade da solução da tarefa

5. Testing
     * Automated Testing
     * Unit testing
     * End to end test cases
  
6. CI
    * Build, testing
    * Notificação de conflitos
    * Resolução de erros
    * Permissão para mesclar branches

6. CD:
    * Deploy de diferentes ambientes como: DEV Environment, QA Environment, UAT e Prod

### Etapas de um workflow (exemplo em projeto):

**Developer Workflow**

Developer A > Team Data Science Project

1. Feature Development
    *  O desenvolvedor pega uma tarefa(task) específica

2. Push and Pull Request:
    *  O desenvolvedor cria uma branch da main, para começar a escrever o código e realizar a task. O coding é feito num ambiente local onde posteriormente é realizado o pull request. Logo após, o time irá avaliar a solicitação revendo a qualidade do código, o estilo se está seguindo os padrões da empresa ou do projeto e verificação de alguns erros. 

3. Automate CI pipeline
    * A cada pull request, um pipeline de CI é ativado
    * Esse pipeline builda a aplicação e executa todos os test cases
    * Se os testes passarem, o PR é aprovado e o código será mesclado com a branch main

4. Automate CD pipeline: 
    * Em cima do PR, um pipeline CD será ativado
    * A apicação será automaticamente implantada a um ambiente de desenvolvimento ou um ambiente fictício (teste)
    * Se os testes passarem, a aplicação será enviada para o ambiente de produção.

--------------------

Github action com projeto python

Etapas seguidas:

1. Criação do projeto python localmente com o nome githubactionproject
2. Adicionado projeto ao repositório remoto e criado um README.md
3. Construção da estrutura do diretório
   *  requirements.txt (pytest e pandas)
   * Pasta src com as funções de soma e subtração
   * Pasta test importando as funções para test e criado os test cases
4. Criação do diretório .github/workflows/unitttest.yml

A cada commit que é feito no projeto, o githubaction executa os testes.

obs: As instruções de como está estruturado o arquivo yml está dentro do próprio arquivo comentado por linhas.


