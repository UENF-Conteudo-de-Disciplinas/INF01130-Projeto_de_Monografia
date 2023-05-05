# Atividade 3

## Classroom

- Título: 3ro Artículo - leitura e resumido
- Professor: Luis Antonio Rivera Escriba
- Publicação: 2 de mai. (editado: 2 de mai.)
- Pontuação: 10 pontos
- Data de entrega: 04/05/2023 - 23:59
- Descrição:

> Artigo técnico resumido no formato aproximado ao proposto.
> Importante que vocês consigam extrair informação útil da fonte.
> Informação útil, por exemplo, pode ser envolvendo:
>
> - Apresentação do tema
> - Problema que aborda no artigo
> - Objetivos.
> - Teorias e técnicas utilizadas como base (nesse artigo)
> - Modelo que o autor propõe como contribuição
> - Teorias e/ou técnicas criadas
> - Soluções

Importante vocês dominem o tema. Para demonstrar isso, devem apresentar na sala
de aula

## Resumo do artigo

Título: Problema de Alocação de Horários: um Estudo de Caso Utilizando o Software Livre FET

Objetivo: propor a automatização de grade horária para o curso de CC da UNIFESO usando o FET (Free Timetabling Program)

### 1. Introdução

- Problemas na construção da grade:
  - Indisponibilidade de horário dos professores
  - Aposentadorias
  - Novos professores
  - Aditivos de contratos

- Motivações:
  - Curso sem sistema informatizado com fim de resolver problema de alocação e gerar quadro de horários.
  - Trabalho realizado manualmente semestralmente

- Resultados esperados são grades que:
  - Não tenham conflitos de matérias, disponibilidade de tempo e professores.
  - Obedeçam as restrições
  - Aloquem o máximo de matérias possíveis
  - Quadro de horários viável

- Foi usado o *Free Timetabling Program* (FET) que atendeu às necessidades do processo:
  - Cadastro dos dados
  - Geração das grades

### 2. Problema de Alocação de Horários

- Relacionam diferentes variáveis
  - Professores
  - Alunos
  - Matérias
  - Horários semanais

Classificado como NP-difícil

- Passos:
  - Consultar a disponibildiade horária de professores
  - Alocar em turmas disponíveis
    - Evitar turmas desmoduladas (?)
      - Com tempo vago
      - Muitas aulas diferentes no mesmo dia
    - Evitar que professores ministrem poucas aulas no dia

- Condições
  - Não alocar um professor na mesma turma e mesmo horário
  - Não alocar professor em horário que não possa
  - Não quebrar aulas
  - Limite diário de aulas
  - Elimitar "buracos" nos horários dos professores
  - Minimizar quantidade de dias para os professores

### 3. Técnicas utilizadas para resolver o problema de alocação de horários

Independente da técnia, é importante obedecer algumas regras para não haver necessidade de desfazer todo o processo.

- Técnicas:
  - Algoritmos Exatos (AE)
  - Algoritmos Heurísticos
  - Algoritmos Metaheurísticos

#### 1. Algoritmos exatos ou de programação inteira

- Características:
  - Tempo de resposta não satisfatório
  - Garantia de se encontrar solução ótima

- Deve-se criar regras e restrições com cautela
- Exemplos de algoritmos:
  - Branch-and-Bound
  - Branch-and-Cut
  - Branch-and-Price

#### 2. Algoritmos Heurísticos e Metaheurísticos

- Características:
  - Tempo computacional razoável
  - Não garantem encontrar a solução ótima

- Exemplos de metaheurísticas:
  - GRASP
  - Busca Tabu
  - Algoritmos Genéticos

##### 1. Greedy Randomized Adaptive Search Procedures (GRASP)

- Processo iterativo que consiste em duas fases
  - Construção
    - Busca gulosa
      - Soluções são construídas através de algum critério heurístico até ter uma solução viável
  - Busca local
    - Encontrar um ótimo local na vizinhança
  - Permite que diferentes soluções de boa qualidade sejam geradas

##### 2. Busca Tabu

- Tem como finalidade evitar alcançar soluções em mínimos locais
- Usa uma lista de movimentos tabu, para que ao encontrar um melhor local ele retorne à uma distância maior, assim prosseguindo para um caminho ainda não visitado.

##### 3. Algoritmos Genéticos (AGs)

- Baseado na ideia de evolução natural e na genética
- > Em média os indivíduos representam soluções cada vez melhores

- Características
  - Trabalham com uma população (conjunto de soluções) e não apenas uma
  - Necessitam do valor de uma função-objetivo
  - Usam transições probabilíticas e não regras determinísticas (?)

- É necessário que os indivíduos iniciais cubram a maior área possível do espaço de busca

- Fluxo básico do algoritmo:
  - Seleção
    - Indivíduos iniciais e temporários são manualmente gerados.
    - Os indivíduos com baixa **adequabilidade*** terão alta provabilidade de desaparecerem
  - Cruzamento
    - Troca de fragmentos entre a população atual
  - Mutação
    - Mudança de algum dos genes da solução de forma aleatória

- Precisa de condição de finalização, podendo ser...
  - Tempo
  - Estagnação da população
  - Número de geração
  - Etc.

### 4. *Free Timetabling Program* (FET)

Atualmente a elaboração é feita de forma manual com o MS Word que demanda dias ou semanas, principalmente quando ocorrem imprevistos como novas contratações, desligamentos, falta de disponibilidades, etc.

- Capacidade do software:
  - Cadastro de variáveis
    - Professores
    - Matérias
    - Períodos
    - Salas
    - Laboratórios
    - Etc.
  - Manipulação de horário das aulas
  - Número de aulas que cada professor leciona
  - Disponibilidade dos professores
  - Dividir o número de aulas por dia e por semana
  - Manejar manérias pré-requisitos de outras
  - É possível descrever o número de alunos em cada turma
  - O sistema gera grades horárias automaticamente
  - Exporta grades como XML ou HTML

### 5. Considerações Finais

- Tema complexo
- Problema de automatização é viável de ser entendido e implementado
- Software rápido, coeso, eficiente e comprovou ser capaz de gerar grades horárias

- Vantagens
  - Economia de tempo, custo e pessoal
  - Possibilidade de modificar os resultados
  - Informações detalhadas e interação com usuários
