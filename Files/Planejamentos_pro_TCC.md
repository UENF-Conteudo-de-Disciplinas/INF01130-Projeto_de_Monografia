# Planos

## Coisas a fazer (requisitos)

- Contas de professores para adicionarem seus horários de preferência?
  - Anotações
    - Pouco relevante, visto que são poucos professores especificamente em computação, mas pode ser interessante em caso de expansão do código.
    - Por enquanto pode ser através de interrogatório direto do coordenador com os professores.
- Heurísticas
  - E se eu criar meio que um produto vetorial de todas as combinações possíveis, mensurar todas e retornar a melhor?
    - Eu poderia criar uns critérios de exclusão para remover alternativas inviáveis.
- Cadastro de informações
  - Professores
    - Criar tela de seleção de preferências para os professores. A ordem de preferência vai de 5 a -1, sendo 0 o mesmo que "Tanto faz" e -1 o mesmo que "não desejo que seja nesses horários".
  - Alunos
    - Lista de todos os alunos de computação
    - Informar também quais disciplinas cada aluno
      - Foi aprovado
      - Pretende fazer
      - Se inscreveu
  - Disciplinas
    - Quantidade de alunos que
      - podem fazer
      - Se inscreveram
    - Lista de requisitos das salas
      - Computador
      - Televisão
  - Pesos
    - Lista de pesos e prioridades definidos pelo coordenador
      - Conflitos de alunos
      - Fuga das preferências dos horários dos professores
      - Necessidade de contratação de bolsistas
    - Tabela dos pesos
      - Lista de pesos X Objetivos
        - Títulos das colunas
          - Peso por
            - Conflito por aluno
            - senioridade do aluno(?)
            - Preferência de professor
            - Sala maior do que o devido
            - etc.
        - Cada linha seria uma instância desses pesos, onde cada uma delas poderia ser uma opção válida de abordagem. Exemplos:
          - Priorizando alunos
          - Priorizando professores
          - Priorizando salas
          - etc.
- Análise de dados
  - Analisar a quantidade de reprovações históricas das disciplinas
- Interface
  - Responsiva pela mudança manual das disciplinas
- Etapas
  - Aquisição de informações
    - Pesquisa histórica
    - Salas
      - Vagas e caracterísicas
    - Disciplinas
      - Computação
      - Matemática
      - Outros
    - Professores
      - Computação
      - Matemática
      - Outros
        - Ingles
        - Física
        - Comp. Soc
        - Empreend
        - Metodologia
    - Alunos
      - Demandas
  - tabela preliminar
  - Demanda real
  - tabela definitiva
- Módulos do sistema
  - Interface
    - Checar e ajustar os parâmetros do sistema para gerenciar as informações
  - Entrada de Dados
    - Armazena todas as informações em um banco de dados relacional
    - Disponibilidade e preferência de professores
    - Tabelas de horários de semestres anteriores
    - etc.
  - Disponibilidade de tempo
    - Área em que os professores informarão suas disponibilidades
    - [Prefiro que isso esteja junto com o módulo anterior]
  - Módulo de otimização
    - Usando o pacote CPLEX para resolver o problema com programação linear
  - Relatórios
    - Apresentará uma lista de indicadores da tabela gerada
      - Indicadores
        - Uso de salas
        - Número de salas disponíveis
        - Conflitos de aulas
        - Valor da função objetivo
        - Tempo de processamento
- Como permitir a adição de restrições ou objetivos manualmente?
- Manipulação com Manim para modificação da fórmula matemática de programação inteira?

## Definir prioridades

- Aulas consecutivas
- Separar turma em dois
- seg/qua, qua/sex, ter/qui
- Limite de aula por dia

## Dúvidas

- Como se sabe a disponibilidade das salas?
- Quais são as salas apropriadas?
- Deve-se considerar que algumas aulas serão fixas?
  - Adicionar cadeado para matérias que serão fixas de outros cursos
- Como permitir a adição de restrições ou objetivos manualmente?
- Manipulação com Manim para modificação da fórmula matemática de programação inteira?
- Alguém tem uma listagem de todas as salas com todas as capacidades?
- Se considerarmos a demanda total como critério, consequentemente a demanda real (as que os alunos de fato desejam se matricular) também será englobada no melhor caso?

### Perguntas para Tang

- Quanto que o Coordenador pode mandar nos professores para que eles peguem X matérias?

## Perguntas sobre o uso

### Rivera

- Interfaces que ajudem a ter insights
- Aceitabilidade tecnológica
- Modelagem no ponto de vista Interface Homem Máquina
- Faltam mais dados sobre as experiências dos outros

### Eu

- Diferentes heurísticas

### Molina

## To Learn

- Quantum Approximate Optimization Algorithm (QAOA)
- Integer Programming (IP)
- CPLEX - modelling tool
- cCOIN-OR Branch-and-Cut
- The model was initially implemented in the General Algebraic Modeling System (GAMS IDE 2.0.31.8 Rev. 143)
- solved with the CPLEX solver 9.1.2 [alternatively the open source solver Coin-
Cbc (Forrest and Lougee-Heimer 2005)]
- Algoritmos Exatos (AE)
- Algoritmos Heurísticos e Metaheurísticos.
  - (Goldbarg e Luna 2005).
    - Branch-and-Bound
    - Branch-and-Cut
    - Branch-and-Price
- Metaheurísticos
  - GRASP
  - Busca Tabu
  - Algoritmos Genéticos
- Analisar de que forma que organizar os alunos->disciplinas como grafos ajudaria na resolução

## Bons links

- [TimeTable][TimeTable]
- [FET]
- [LinkTMuller]
- [GitHub]
- [Sci-Hub: Quebrador de link científico][SciHub]
- [Web of Science][WoS]
- [Periodicos Capes][Capes]
- [Salas CCT](https://uenf.br/cct/secretaria-academica/distribuicao-das-salas-de-aula-do-cct/)
- [Site CCT](https://uenf.br/cct/)

[Capes]: https://www.periodicos.capes.gov.br/
[LinkTMuller]: https://www.unitime.org/publications.php
[TimeTable]: https://teacherhead.com/2015/05/23/the-art-of-timetabling-principles-and-priorities/
[GitHub]: https://github.com/UniTime
[FET]: https://lalescu.ro/liviu/fet/
[SciHub]: https://sci-hub.se/
[WoS]: https://www.webofscience.com/wos/woscc/basic-search

## Livros

- Search and optimization by metaheuristics: Techniques and algorithms inspired by nature
- Object-oriented design knowledge: Principles, heuristics and best practices
- Metaheuristics: From Design to Implementation
- Metaheuristics for Production Scheduling
- Metaheuristics for hard optimization: Simulated annealing, tabu search, evolutionary and genetic algorithms, ant colonies,... Methods and case studie
