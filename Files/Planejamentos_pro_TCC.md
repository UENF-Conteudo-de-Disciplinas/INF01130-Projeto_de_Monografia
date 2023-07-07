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
  - Conseguir salvar diferentes alternativas de grade final e compará-las
- Etapas
  - Aquisição de informações
    - Pesquisa histórica
      - Levantar dados: quantidade de reprovações - Pessoas que perderam em pelo menos 1
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
- Tirar foto/escanear rabiscos e tentativas de mudança de grade nos períodos anteriores.
  - Fazer uma comparação automatizada de cada uma das tentativas dos últimos semestres, incluindo as grades
- Apresentação impressionante
  - Usar a ideia [desse holograma](https://youtu.be/z_xVCSyoo_c) para mexer num grafo 3D
    - Tipo [assim](https://youtu.be/lLPmELPQpFw)
- O scroll do mouse deve funcionar como um corte planar nas visualizações, permitindo andar em uma dimensão: ver a grade de cada aluno, a grade de cada professor, a grade de cada sala, a grade de cada horário. (isso seria BOM DEMAIS!!!) - Curvas de nível em timetabling

## Definir prioridades

- Aulas consecutivas
- Separar turma em dois
- seg/qua, qua/sex, ter/qui
- Limite de aula por dia

## Dúvidas e anotações

- Como se sabe a disponibilidade das salas?
- Quais são as salas apropriadas?
- Deve-se considerar que algumas aulas serão fixas?
  - Adicionar cadeado para matérias que serão fixas de outros cursos
- Como permitir a adição de restrições ou objetivos manualmente?
- Manipulação com Manim para modificação da fórmula matemática de programação inteira?
- Alguém tem uma listagem de todas as salas com todas as capacidades?
- Se considerarmos a demanda total como critério, consequentemente a demanda real (as que os alunos de fato desejam se matricular) também será englobada no melhor caso?
- De que forma eu posso tornar a multidimensionalidade do problema em algo visualmente agradável?
  - Dias X Horas X Salas
  - Pensei em uma abordagem 3D similar à troca de hotbar do Minecraft
- Será que se eu fizer várias equações de programação inteira para encontrar várias otimizações diferentes eu conseguiria misturar elas de uma boa forma e achar uma ótima geral?
- Interessante... Primeiro resolveriam-se os cálculos, físicas... as matemáticas e só depois as disciplinas específicas do curso. Interessante. Talvez eu poderia até definir isso como
- devo considerar a quantidade de matérias que cada professor ministra e quais cada um tem predisposição a ministrar, num critério similar à sua preferência de horários
- Será que eu deveria fazer um grafo de todas as disciplinas possíveis e à que cursos elas estão relacionadas?
- Eu poderia ter uma tabela de pesos para cada critério, rodar o código para pesos aleatórios e ver qual deles acharia uma solução melhor
- Fazer uma grade focando exclusivamente na redução de conflitos, mas seguindo as hard constraints (booleanas 0 e 1 que multiplicam o valor total?)
  - E depois fazer um com os padrõezinhos mais normais tipo "seg e quarta de 14 às 16"
- Acho que dá pra pensar no problema de timetabling como o problema de coloração de grafos e acho que já vi isso antes. Será que dá uma solução legal?
- Se tem duas aulas de cálculo, elas não precisam ser no mesmo horário.
- Fiquei com vontade de montar a grade do curso no mermaid fazendo eles num diagrama de sequência ou similar
- Quantas heurísticas implementar?
- Será que eu deveria só fazer o interativo? Talvez seja uma boa.

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
- [Esporte](https://robinxval.ugent.be/ITC2021/)

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
