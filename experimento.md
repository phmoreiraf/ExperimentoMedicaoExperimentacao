# Planejamento do Experimento – TCC I  
**Avaliação Experimental da Clean Architecture versus Arquitetura em Camadas:  
Impactos na Clareza de Design e Facilidade de Evolução**

---

### 1.1 Identificação básica do trabalho

- **Título**  
  *Avaliação Experimental da Clean Architecture versus Arquitetura em Camadas: Impactos na Clareza de Design e Facilidade de Evolução*

- **Tema**  
  Comparação empírica de estilos arquiteturais (Clean Architecture vs arquitetura em camadas tradicional) quanto à clareza de design e à facilidade de evolução em sistemas/projetos.

- **Autor**  
  - Pedro Henrique Moreira Caixeta Ferreira

- **Curso**  
  Bacharelado em Engenharia de Software – PUC Minas

- **Instituição**  
  Instituto de Ciências Exatas e Informática – Pontifícia Universidade Católica de Minas Gerais (PUC Minas), Belo Horizonte – MG – Brasil.

- **Versão deste documento de planejamento**  
  v1.0 – Planejamento inicial do experimento

---

### 1.2 Contexto

Decisões de arquitetura de software influenciam diretamente a compreensão, a evolução e a manutenibilidade de sistemas, afetando esforço, custo e qualidade do produto. A literatura sobre dívida arquitetural e padrões de projeto mostra que escolhas estruturais mal fundamentadas tendem a aumentar defeitos, retrabalho e esforço de manutenção, além de impactar atributos como testabilidade e capacidade de evolução do código.

Nesse cenário, a **arquitetura em camadas tradicional** consolidou-se como um estilo amplamente adotado e ensinado, oferecendo uma organização relativamente simples, conhecida e suportada por diversos frameworks. Em paralelo, abordagens como a **Clean Architecture** propõem maior independência de detalhes de infraestrutura e maior isolamento do domínio, com separação mais rigorosa entre regras de negócio e mecanismos de entrega, persistência e acesso a dados.

Apesar do avanço da literatura sobre arquitetura, ainda existem poucas evidências empíricas *controladas* que comparem, em um mesmo conjunto de funcionalidades, a Clean Architecture e a arquitetura em camadas tradicional sob a perspectiva de **clareza de design** e **facilidade de evolução**. Em muitas discussões técnicas, a Clean Architecture é apresentada quase como “sucessora natural” da arquitetura em camadas, mas essa percepção nem sempre se baseia em resultados experimentais sistemáticos.

A pesquisa proposta busca justamente preencher essa lacuna, por meio de um **experimento controlado em sala de aula** com estudantes de Engenharia de Software, analisando a forma como desenvolvedores compreendem e modificam sistemas funcionalmente equivalentes que diferem apenas em seu estilo arquitetural.

---

### 1.3 Problema de pesquisa

O problema central que orienta o TCC pode ser formulado da seguinte forma:

> **Problema de pesquisa**  
> Em que medida a adoção da Clean Architecture, em comparação à arquitetura em camadas tradicional, impacta a clareza do design e a facilidade de evolução de sistemas de software, considerando aspectos como compreensibilidade, modularidade, manutenibilidade e esforço de modificação?

Esse problema deriva da necessidade de orientar decisões arquiteturais com base em **evidências empíricas**, e não apenas em tendências, preferências pessoais ou narrativas não verificadas. A resposta ao problema deve apoiar tanto equipes de engenharia, na definição de diretrizes arquiteturais, quanto docentes, na escolha de estilos a serem enfatizados em disciplinas e projetos.

---

### 2.1 Escopo

#### 2.1.1 Escopo do estudo

O experimento irá:

- Comparar duas versões de um mesmo sistema Java/Spring Boot:
  - **Versão A**: Arquitetura em camadas tradicional;
  - **Versão B**: Clean Architecture.
- Aplicar tarefas de:
  - **Compreensão do sistema** (leitura e entendimento do código);
  - **Implementação de uma modificação funcional simples** (evolução do código);
  - **Avaliação subjetiva** das arquiteturas por meio de questionário em escala Likert.
- Coletar dados objetivos e subjetivos para comparar clareza de design e facilidade de evolução entre as arquiteturas.

#### 2.1.2 Template de escopo

- **Contexto**  
  Experimento controlado conduzido em laboratório de informática da PUC Minas, em disciplina do curso de Engenharia de Software, com estudantes realizando tarefas práticas em duas variantes arquiteturais de um mesmo sistema.

- **Objetos de estudo**  
  - Protótipo 1: sistema Java 17 + Spring Boot 3.3.x em arquitetura em camadas tradicional;  
  - Protótipo 2: sistema Java 17 + Spring Boot 3.3.x em Clean Architecture.  
  Ambos implementam o mesmo conjunto de funcionalidades, diferenciando-se apenas pela estrutura arquitetural.

- **Participantes**  
  Estudantes de Engenharia de Software que cursam disciplina relacionada a desenvolvimento/arquitetura, com conhecimentos básicos em Java, orientação a objetos e uso de IDE.

- **Tarefas incluídas no escopo**  
  - Leitura e compreensão do código em cada arquitetura;  
  - Implementação de uma modificação funcional simples em cada arquitetura;  
  - Resposta a questionário de avaliação (percepção sobre clareza, facilidade de modificação e potencial de evolução);  
  - Registro de tempos, coleta de diferenças de código e consolidação das respostas.

- **Fora do escopo**  
  - Avaliação de desempenho em tempo de execução (latência, throughput etc.);  
  - Estudos longitudinais de evolução do sistema em ambiente produtivo;  
  - Comparação com outros estilos arquiteturais (por exemplo, microserviços, hexagonal, event-driven);  
  - Avaliação de usabilidade da interface de usuário (o foco está na estrutura de código e arquitetura).

- **Entregáveis principais**  
  - Protocolo experimental documentado (este planejamento);  
  - Conjunto de dados anonimizados (tempos, diferenças de código, respostas a questionários);  
  - Tabelas e gráficos comparando as arquiteturas;  
  - Análise estatística e discussão dos resultados;  
  - Capítulos de Resultados, Discussão e Conclusão do TCC.

---

### 2.2 Objetivos

#### 2.2.1 Objetivo geral

> **Comparar a Clean Architecture e a arquitetura em camadas tradicional quanto à clareza de design e à facilidade de evolução de sistemas Java/Spring Boot, com base em métricas objetivas e percepções dos desenvolvedores.**

#### 2.2.2 Objetivos específicos

- **OE1 – Esforço de compreensão**  
  Mensurar e comparar o esforço de compreensão do sistema em cada arquitetura, considerando tempo de compreensão e percepção de clareza estrutural.

- **OE2 – Esforço de implementação de modificações**  
  Mensurar e comparar o esforço de implementação de uma modificação funcional simples em cada arquitetura, considerando tempo de implementação, tamanho das mudanças de código e sucesso na implementação correta.

- **OE3 – Percepções dos participantes**  
  Avaliar como os participantes percebem, em cada arquitetura, a clareza da estrutura do código, a facilidade de localizar e implementar alterações e o potencial de manutenção e evolução.

- **OE4 – Apoio a decisões arquiteturais**  
  Integrar as evidências objetivas e subjetivas obtidas para propor recomendações práticas (por exemplo, um checklist) que auxiliem na decisão entre Clean Architecture e arquitetura em camadas em contextos semelhantes.

---

### 2.3 Stakeholders e impacto esperado

- **Autor**  
  - Adquire experiência prática em desenho, condução e análise de experimento controlado em Engenharia de Software;  
  - Produz evidências que podem ser reutilizadas em disciplinas futuras ou em publicações.

- **Estudantes participantes**  
  - Vivenciam na prática diferenças entre estilos arquiteturais;  
  - Têm contato com medição e experimentação em Engenharia de Software;  
  - Desenvolvem senso crítico sobre trade-offs arquiteturais.

- **Orientadores e docentes**  
  - Obtêm insumos para aprimorar o conteúdo de disciplinas de arquitetura e qualidade;  
  - Podem utilizar os resultados como casos didáticos em aulas futuras.

- **Coordenação de curso e instituição**  
  - Fortalecem a cultura de pesquisa empírica no curso;  
  - Podem apresentar o TCC como exemplo de integração entre teoria e prática.

- **Comunidade de Engenharia de Software**  
  - Recebe evidências adicionais sobre quando a Clean Architecture traz benefícios concretos em relação à arquitetura em camadas;  
  - Pode reutilizar o protocolo experimental em outros contextos e instituições.

---

### 2.4 Riscos de alto nível

| Risco                                       | Descrição                                                                                   | Estratégia de mitigação                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| R1 – Baixa participação de alunos          | Número de participantes menor que o planejado, prejudicando a análise estatística          | Agendar a aplicação em aula obrigatória; prever data reserva; comunicar com antecedência |
| R2 – Dados incompletos ou inconsistentes   | Ausência de tempos, respostas faltantes em questionários ou commits sem `git diff` adequado| Testar previamente formulários e roteiro; revisar dados logo após cada sessão            |
| R3 – Viés de ordem entre arquiteturas      | A arquitetura utilizada primeiro influencia o desempenho na segunda (efeito de aprendizado) | Sortear a ordem das arquiteturas e balancear: metade começa em cada variante            |
| R4 – Problemas técnicos no laboratório     | Falha em máquinas, IDE, rede ou repositórios durante a aplicação                           | Validar o ambiente antes; ter máquinas reserva; manter cópias locais dos repositórios    |
| R5 – Tempo de aula insuficiente            | As tarefas não cabem no tempo disponível, comprometendo a coleta completa                  | Realizar piloto com pequeno grupo; ajustar complexidade da tarefa e tempo previsto       |

---

### 2.5 Premissas

- Os participantes possuem conhecimentos básicos de programação em Java, orientação a objetos e uso de IDE.
- A turma já foi exposta previamente à ideia de arquitetura em camadas em disciplinas anteriores.
- As duas versões do sistema (camadas e Clean) são **funcionalmente equivalentes**, diferenciando-se apenas pela estrutura arquitetural.
- O laboratório de informática oferece estações com configuração homogênea de hardware e software (mesma versão de JDK, IDE e ferramentas).
- O tempo de aula reservado é suficiente para que todos os participantes concluam as tarefas e preencham o questionário.
- Os instrumentos de coleta (cronômetro, formulários, repositórios Git) funcionarão corretamente durante a aplicação.

---

### 2.6 Critérios de sucesso

O experimento será considerado bem-sucedido se:

1. **Amostra válida**  
   - Um número mínimo de participantes (por exemplo, ≥ 60) completa todas as tarefas em ambas as arquiteturas, com dados consistentes.

2. **Coleta de dados completa**  
   - Para cada participante e arquitetura, existirem registros de:  
     - Tempo de compreensão (M1);  
     - Tempo de implementação (M2);  
     - Diferença de código (M3);  
     - Respostas completas ao questionário Likert (M4–M10);  
     - Resultado de sucesso na implementação (M11).

3. **Análise estatística realizada**  
   - Aplicação de estatísticas descritivas e testes adequados (por exemplo, Shapiro–Wilk e Wilcoxon Signed-Rank) para comparar arquiteturas.

4. **Resposta ao problema de pesquisa**  
   - Os resultados permitem discutir de forma clara se há (ou não) diferenças relevantes entre as arquiteturas nos aspectos avaliados.

5. **Geração de recomendações práticas**  
   - A partir das métricas e análises, é possível propor recomendações ou um checklist que ajude outras equipes a decidir quando usar Clean Architecture ou arquitetura em camadas.

---

### 2.7 Modelo GQM (Goal–Question–Metric)

#### 2.7.1 Tabela GQM – Objetivos, Perguntas e Métricas

**Legenda de objetivos:**

- **OE1** – Esforço de compreensão  
- **OE2** – Esforço de implementação de modificações  
- **OE3** – Percepções dos participantes  
- **OE4** – Apoio a decisões arquiteturais

**Legenda de métricas (M1–M12): ver Seção 2.7.2.**

| Objetivo | Pergunta                                                                                                                                    | Métricas associadas        |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| OE1      | **Q1.1** – Há diferença significativa no tempo de compreensão do sistema entre a arquitetura em camadas e a Clean Architecture?            | M1, M12                    |
| OE1      | **Q1.2** – Os participantes percebem diferenças de clareza estrutural na fase de compreensão entre as duas arquiteturas?                   | M4, M6                     |
| OE1      | **Q1.3** – Como o tempo de compreensão se relaciona com as percepções subjetivas de clareza da estrutura do código?                        | M1, M4, M6                 |
| OE2      | **Q2.1** – Há diferença significativa no tempo necessário para implementar a modificação solicitada em cada arquitetura?                  | M2, M12                    |
| OE2      | **Q2.2** – O tamanho das mudanças de código realizadas difere entre a arquitetura em camadas e a Clean Architecture?                       | M3, M2                     |
| OE2      | **Q2.3** – Qual é a relação entre esforço de implementação (tempo e tamanho da mudança) e o sucesso na implementação correta?              | M2, M3, M11                |
| OE3      | **Q3.1** – Como os participantes avaliam a facilidade de localizar e implementar as alterações em cada arquitetura?                        | M5, M7, M8                 |
| OE3      | **Q3.2** – Como os participantes avaliam o risco percebido de impactar outras partes do sistema ao modificar o código?                     | M9, M7                     |
| OE3      | **Q3.3** – Em qual arquitetura os participantes percebem maior capacidade de manutenção e evolução do sistema?                             | M10, M9                    |
| OE4      | **Q4.1** – Como combinar métricas objetivas (tempo, mudança de código, sucesso) e percepções subjetivas para identificar cenários favoráveis à Clean Architecture? | M1, M2, M3, M4, M5, M10    |
| OE4      | **Q4.2** – Em que situações a indireção adicional da Clean Architecture não se traduz em ganhos de clareza e evolutividade em relação à arquitetura em camadas? | M1, M2, M3, M4, M10, M12   |
| OE4      | **Q4.3** – Quais indicadores devem compor um checklist prático para apoiar a decisão entre Clean Architecture e arquitetura em camadas em projetos futuros? | M1, M2, M3, M4, M5, M9, M10, M11, M12 |

---

#### 2.7.2 Tabela de métricas

| ID   | Métrica                                                                                                                          | Unidade                                 |
|------|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| M1   | **Tempo de compreensão do sistema** – tempo necessário para que o participante entenda o propósito e o funcionamento do sistema em cada arquitetura. | Segundos                                |
| M2   | **Tempo de implementação da modificação** – tempo total gasto para implementar a funcionalidade solicitada em cada arquitetura. | Segundos                                |
| M3   | **Tamanho da mudança de código** – quantidade de linhas adicionadas, removidas ou modificadas entre a versão inicial e a final (via `git diff`). | Linhas de código                        |
| M4   | **Clareza da estrutura para compreensão** – média das respostas em escala Likert (1–5) à afirmação “A estrutura do código facilitou a compreensão do sistema”, por arquitetura. | Pontos em escala Likert (1–5)          |
| M5   | **Facilidade para localizar onde alterar** – média das respostas em escala Likert (1–5) à afirmação “Foi fácil identificar onde implementar as alterações necessárias”. | Pontos em escala Likert (1–5)          |
| M6   | **Clareza da organização de classes e pacotes** – média das respostas à afirmação “A organização das classes e pacotes estava clara e coerente”. | Pontos em escala Likert (1–5)          |
| M7   | **Facilidade de implementação** – média das respostas à afirmação “A arquitetura facilitou a implementação da modificação solicitada”. | Pontos em escala Likert (1–5)          |
| M8   | **Facilidade de navegação no código** – média das respostas à afirmação “Foi simples navegar entre arquivos e localizar os componentes corretos”. | Pontos em escala Likert (1–5)          |
| M9   | **Risco percebido de impacto em outras partes** – média das respostas à afirmação “A estrutura da arquitetura reduziu o risco de impactar outras partes do sistema”. | Pontos em escala Likert (1–5)          |
| M10  | **Percepção de manutenção e evolução** – média das respostas à afirmação “Esta arquitetura favorece a manutenção e evolução do sistema”. | Pontos em escala Likert (1–5)          |
| M11  | **Taxa de sucesso na implementação** – proporção de participantes que implementam corretamente a funcionalidade solicitada (todos os testes de aceitação passam). | Percentual (%)                          |
| M12  | **Diferença relativa de tempo entre arquiteturas** – razão entre os tempos médios de compreensão/implementação (por exemplo, tempo_Clean ÷ tempo_Camadas) para cada tipo de tarefa. | Valor adimensional (razão entre tempos) |

---

### 2.8 Síntese textual do GQM

O modelo GQM organiza o experimento de forma sistemática:

- A partir dos **objetivos específicos** (OE1–OE4) foram definidas **perguntas** que explicitam o que se deseja saber sobre esforço de compreensão, esforço de implementação, percepções dos participantes e apoio à decisão arquitetural.
- Para cada pergunta foram associadas **métricas objetivas** (tempos, tamanho da mudança, taxa de sucesso) e **métricas subjetivas** (escores em escala Likert), garantindo pelo menos duas métricas por pergunta.
- As métricas são reutilizadas em diferentes perguntas quando necessário, assegurando consistência e permitindo análises cruzadas entre esforço, percepções e resultados.

Essa estrutura fornece uma base clara para a coleta e análise de dados, garantindo alinhamento entre o problema de pesquisa, os objetivos do TCC, o desenho experimental e as métricas que serão efetivamente observadas.

---

### 3.1 Modelo conceitual

O modelo conceitual do estudo parte da hipótese de que o **estilo arquitetural** adotado em um sistema (Clean Architecture ou arquitetura em camadas tradicional) influencia:

1. A **clareza de design**, refletida em:
   - Facilidade de compreensão do sistema;
   - Clareza da organização de classes e pacotes;
   - Percepção de estrutura mais ou menos “explicativa”.

2. A **facilidade de evolução**, refletida em:
   - Esforço para implementar uma modificação funcional simples (tempo e tamanho da mudança de código);
   - Risco percebido de impactar outras partes do sistema;
   - Percepção de capacidade de manutenção e evolução no médio prazo.

Em termos conceituais:

- **Estilo arquitetural (fator principal)** → afeta diretamente:
  - **Esforço de compreensão** (tempo e clareza percebida);
  - **Esforço de modificação** (tempo, tamanho da mudança, sucesso);
  - **Percepções de manutenção/evolução** (Likert).
- **Perfil do participante** (experiência com Spring Boot, contato prévio com Clean Architecture, experiência profissional) atua como **variáveis de controle/covariáveis**, podendo moderar os efeitos observados, mas não é manipulado no experimento.

### 3.2 Hipóteses do estudo

Com base no modelo conceitual e na literatura de arquitetura e design de software, são definidas as seguintes hipóteses substantivas:

- **H1 – Esforço de compreensão**  
  Há diferença significativa no esforço de compreensão do sistema entre a arquitetura em camadas e a Clean Architecture, considerando tempo de compreensão e clareza percebida da estrutura do código.

- **H2 – Esforço de implementação de modificações**  
  Há diferença significativa no esforço para implementar uma modificação funcional simples entre as duas arquiteturas, considerando tempo de implementação, tamanho da mudança de código e taxa de sucesso na implementação.

- **H3 – Percepções de clareza, risco e evolutividade**  
  As percepções de facilidade para localizar onde alterar, facilidade de navegação, risco percebido de impacto em outras partes do sistema e capacidade de manutenção/evolução diferem entre Clean Architecture e arquitetura em camadas.

- **H4 – Coerência entre métricas objetivas e percepções subjetivas**  
  Existe associação entre métricas objetivas (tempos, tamanho da mudança, taxa de sucesso) e percepções subjetivas (escores Likert), de forma que arquiteturas avaliadas como mais claras e evolutivas tendem a apresentar menor esforço de compreensão e modificação.

Nas análises estatísticas, essas hipóteses serão operacionalizadas por meio de hipóteses nulas (H0) de igualdade entre arquiteturas, testadas com nível de significância de 5%.

---

### 3.3 Variáveis, fatores, tratamentos e objetos de estudo

#### 3.3.1 Variáveis do estudo

A tabela abaixo resume as principais variáveis, seu papel no experimento e uma breve descrição.

| Variável                                      | Tipo                        | Descrição resumida                                                                 |
|----------------------------------------------|-----------------------------|------------------------------------------------------------------------------------|
| Estilo arquitetural                          | Independente (fator)        | Estilo de arquitetura utilizado no sistema: arquitetura em camadas ou Clean.      |
| Tempo de compreensão (M1)                    | Dependente                  | Tempo, em segundos, para o participante compreender o sistema em cada arquitetura.|
| Tempo de implementação (M2)                  | Dependente                  | Tempo, em segundos, para implementar a modificação funcional em cada arquitetura. |
| Tamanho da mudança de código (M3)           | Dependente                  | Linhas adicionadas/removidas/modificadas segundo `git diff`.                      |
| Clareza da estrutura (M4, M6)               | Dependente (Likert)         | Percepção de clareza da estrutura e da organização de classes/pacotes.           |
| Facilidade para localizar/implementar (M5,M7)| Dependente (Likert)        | Percepções sobre localizar onde alterar e implementar a modificação.             |
| Facilidade de navegação (M8)                | Dependente (Likert)         | Percepção de quão simples foi navegar entre arquivos e componentes.              |
| Risco percebido de impacto (M9)             | Dependente (Likert)         | Percepção de risco de afetar outras partes do sistema ao modificar o código.     |
| Percepção de manutenção/evolução (M10)      | Dependente (Likert)         | Percepção sobre o quanto a arquitetura favorece manutenção e evolução.           |
| Taxa de sucesso na implementação (M11)      | Dependente                  | Percentual de participantes que implementam corretamente a funcionalidade.       |
| Experiência com Spring Boot                 | Controle / covariável       | Indica se o participante já trabalhou com Spring Boot (sim/não).                 |
| Contato prévio com Clean Architecture       | Controle / covariável       | Indica se o participante já teve contato com Clean Architecture (sim/não).       |
| Experiência profissional em desenvolvimento | Controle / covariável       | Indica se o participante tem experiência profissional na área (sim/não).         |

---

#### 3.3.2 Fatores, tratamentos e combinações

No estudo, considera-se explicitamente um **fator principal** e um fator de **ordem/contrabalançamento**:

- **Fator 1 – Estilo arquitetural (fator principal)**  
  - Tratamento A: Arquitetura em camadas tradicional  
  - Tratamento B: Clean Architecture  

- **Fator 2 – Ordem de exposição (fator de contrabalançamento)**  
  - Sequência 1: primeiro Camadas → depois Clean  
  - Sequência 2: primeiro Clean → depois Camadas  

A tabela a seguir resume os fatores, tratamentos e combinações relevantes:

| Fator                 | Tratamentos / Níveis                                 | Combinações no experimento                                   |
|-----------------------|------------------------------------------------------|--------------------------------------------------------------|
| Estilo arquitetural   | A: Camadas; B: Clean                                | Cada participante interage com A e B (delineamento intra-sujeito). |
| Ordem de exposição    | Seq1: A→B; Seq2: B→A                                 | Grupo Seq1: tarefas em Camadas primeiro; Grupo Seq2: tarefas em Clean primeiro. |

Como o delineamento é **intra-sujeito**, todos os participantes são submetidos a ambos os tratamentos do fator principal (arquitetura). A ordem em que cada tratamento é aplicado é controlada pelo segundo fator (ordem de exposição), reduzindo viés de aprendizagem.

---

#### 3.3.3 Objetos de estudo

Os objetos de estudo são dois protótipos de um mesmo sistema, desenvolvidos em:

- Java 17;
- Spring Boot 3.3.x;
- Mesmo domínio e mesmos requisitos funcionais.

A diferença entre eles está exclusivamente no **estilo arquitetural** adotado:

- Protótipo em **arquitetura em camadas tradicional**, com camadas como controller, service, repository etc.;
- Protótipo em **Clean Architecture**, com separação explícita entre regras de negócio (casos de uso, entidades) e detalhes de infraestrutura (adapters, frameworks).

Essa construção garante comparabilidade entre as arquiteturas, já que o domínio e as funcionalidades são mantidos constantes.

---

### 3.4 Desenho experimental

O desenho experimental é do tipo **intra-sujeito (within-subjects)**: todos os participantes realizam as mesmas tarefas em ambas as arquiteturas, em momentos distintos. A ordem das arquiteturas é contrabalanceada entre os participantes, de forma que aproximadamente metade da turma começa pela arquitetura em camadas e a outra metade pela Clean Architecture. :contentReference[oaicite:1]{index=1}  

O experimento é estruturado em três etapas principais:

1. **Leitura e compreensão do código-fonte**  
   - Cada participante recebe acesso ao repositório de uma das arquiteturas (conforme a ordem sorteada);  
   - O participante analisa o código até se sentir apto a responder questões de compreensão;  
   - O tempo de compreensão é medido (M1) e, em seguida, o participante responde a questões sobre entendimento do sistema e percepções de clareza (M4, M6).

2. **Implementação de uma modificação funcional simples**  
   - Com base em um requisito de mudança previamente definido, o participante implementa a modificação na arquitetura que está utilizando naquele momento;  
   - O tempo de implementação é registrado (M2);  
   - Ao final, a diferença de código é analisada via `git diff` (M3) e verifica-se se a implementação atende aos testes de aceitação (M11);  
   - O participante responde às questões sobre facilidade de localizar onde alterar, facilidade de navegação e risco percebido de impacto (M5, M7, M8, M9).

3. **Repetição do ciclo na outra arquitetura**  
   - O participante repete as etapas de compreensão e implementação na outra arquitetura (Clean ou Camadas, conforme a ordem sorteada);  
   - Novos tempos, diferenças de código e percepções são coletados, permitindo comparações intra-sujeito entre as arquiteturas.

Ao final do experimento, o questionário também coleta percepções globais sobre a capacidade de manutenção e evolução do sistema em cada arquitetura (M10) e dados de perfil (experiência e contato prévio).

---

### 4.1 População, sujeitos e amostragem

- **População-alvo**  
  Estudantes de cursos de Engenharia de Software (ou áreas afins) que já tenham cursado disciplinas básicas de programação orientada a objetos e desenvolvimento de aplicações web.

- **População acessível**  
  Turma de aproximadamente **70 estudantes** do curso de Engenharia de Software da PUC Minas, matriculada em disciplina que dispõe de laboratório de informática e cujo conteúdo permite a aplicação do experimento em aula.

- **Sujeitos do experimento**  
  - Cada estudante participante é considerado um sujeito experimental;  
  - Todos executam as tarefas em ambas as arquiteturas (delineamento intra-sujeito);  
  - Os sujeitos são tratados de forma anônima nas análises, usando códigos ou identificadores numéricos.

- **Amostragem**  
  - Amostragem por conveniência/censo da turma: todos os estudantes presentes na aula em que o experimento ocorre são convidados a participar;  
  - A participação é voluntária, e a não participação não implica qualquer prejuízo acadêmico;  
  - Dados de perfil (idade, experiência com Spring Boot, contato prévio com Clean Architecture e experiência profissional) são coletados para caracterizar a amostra e eventualmente atuar como covariáveis.

---

### 4.2 Instrumentação e protocolo operacional

#### 4.2.1 Instrumentos de coleta e apoio

- **Ambiente de desenvolvimento**  
  - IDE: IntelliJ IDEA (ou equivalente configurado para Java 17/Spring Boot 3.3.x);  
  - JDK 17 instalado em todas as máquinas.

- **Controle de versão**  
  - Git, com repositórios separados para cada arquitetura (Camadas e Clean);  
  - Uso de `git diff` para mensurar tamanho das mudanças de código (M3).

- **Coleta de tempos**  
  - Cronômetros (podem ser físicos ou digitais), operados pelos pesquisadores para garantir consistência na medição do tempo de compreensão (M1) e de implementação (M2).

- **Questionário eletrônico**  
  - Formulário (por exemplo, Google Forms) para registrar:
    - Dados de perfil (idade, experiência prévia etc.);  
    - Percepções em escala Likert sobre estrutura, facilidade de modificação, risco e evolutividade (M4–M10).

- **Roteiro de tarefas**  
  - Documento entregue aos participantes com:
    - Instruções sobre o objetivo da atividade;  
    - Descrição da funcionalidade a ser modificada/implementada;  
    - Orientações sobre como registrar o término de cada etapa.

---

#### 4.2.2 Variáveis (visão operacional)

A tabela abaixo reapresenta as variáveis sob a ótica da **instrumentação**, destacando como são medidas.

| Variável                         | Tipo       | Como é medida / Instrumento                           | Escala          |
|----------------------------------|------------|--------------------------------------------------------|-----------------|
| Estilo arquitetural             | Fator      | Atribuição do repositório (Camadas ou Clean)          | Nominal         |
| Tempo de compreensão (M1)       | Dependente | Cronômetro (início da leitura até declaração de compreensão) | Razão (segundos)|
| Tempo de implementação (M2)     | Dependente | Cronômetro (início da codificação até submissão)      | Razão (segundos)|
| Tamanho da mudança (M3)         | Dependente | Saída do comando `git diff` (linhas afetadas)         | Razão (linhas)  |
| Percepções Likert (M4–M10)      | Dependente | Questionário eletrônico (afirmações 1–5)              | Ordinal (1–5)   |
| Taxa de sucesso (M11)           | Dependente | Resultado dos testes de aceitação (sucesso/falha)     | Proporção (%)   |
| Experiência com Spring Boot     | Controle   | Questão dicotômica no questionário (sim/não)          | Nominal         |
| Contato prévio com Clean        | Controle   | Questão dicotômica no questionário (sim/não)          | Nominal         |
| Experiência profissional        | Controle   | Questão dicotômica no questionário (sim/não)          | Nominal         |

---

#### 4.2.3 Fatores, tratamentos e combinações (visão operacional)

A tabela abaixo detalha, agora do ponto de vista de **execução em sala**, como os fatores e tratamentos se concretizam:

| Fator              | Tratamentos / Níveis                                 | Implementação no protocolo                                             |
|--------------------|------------------------------------------------------|-------------------------------------------------------------------------|
| Estilo arquitetural| A: Camadas; B: Clean                                | Repositórios separados: um em Camadas, outro em Clean.                 |
| Ordem de exposição | Seq1: A→B; Seq2: B→A                                 | Sorteio/atribuição dos participantes para Seq1 ou Seq2.                |

**Combinações**:

- **Grupo Seq1**  
  1. Tarefa de compreensão e modificação na arquitetura em camadas (A);  
  2. Tarefa de compreensão e modificação na Clean Architecture (B).

- **Grupo Seq2**  
  1. Tarefa de compreensão e modificação na Clean Architecture (B);  
  2. Tarefa de compreensão e modificação na arquitetura em camadas (A).

---

### 4.3 Protocolo operacional (passo a passo)

Um possível protocolo operacional em aula é:

1. **Abertura e instruções gerais (5–10 min)**  
   - Apresentação breve do objetivo do experimento;  
   - Esclarecimento de que os dados serão anonimizados e utilizados apenas para fins acadêmicos.

2. **Distribuição dos grupos e repositórios (5 min)**  
   - Sorteio ou definição de quais alunos ficarão em Seq1 (A→B) e Seq2 (B→A);  
   - Entrega dos links dos repositórios Git correspondentes à primeira arquitetura de cada grupo.

3. **Tarefa 1 – Compreensão (Arquitetura 1)**  
   - Início simultâneo da atividade;  
   - Registro do tempo de compreensão (M1) para cada participante;  
   - Preenchimento das questões de percepção relativas à compreensão e estrutura.

4. **Tarefa 2 – Implementação (Arquitetura 1)**  
   - Apresentação do requisito de modificação;  
   - Registro do tempo de implementação (M2);  
   - Coleta da diferença de código via `git diff` (M3);  
   - Verificação de sucesso na implementação (M11);  
   - Preenchimento das questões de percepção relativas à facilidade de modificação, navegação e risco (M5–M9).

5. **Repetição nas Tarefas 3 e 4 com a Arquitetura 2**  
   - O ciclo de compreensão e implementação é repetido para a segunda arquitetura de cada grupo;  
   - Novos registros de M1, M2, M3, M11 e respostas Likert (M4–M10).

6. **Encerramento (5–10 min)**  
   - Coleta de eventuais comentários qualitativos dos participantes;  
   - Agradecimento e reforço de que os resultados serão consolidados no TCC.

---

### 4.4 Plano de análise de dados (pré-execução)

O plano de análise é definido **antes da execução** do experimento, para reduzir vieses e garantir transparência:

1. **Verificação e limpeza dos dados**
   - Conferir se todos os participantes têm:
     - M1, M2, M3, M11 registrados nas duas arquiteturas;  
     - Respostas completas às questões Likert;  
   - Tratar dados ausentes (por exemplo, excluir pares incompletos para análises pareadas).

2. **Análise descritiva**
   - Calcular, para cada arquitetura:
     - Mediana, média, desvio-padrão e intervalo interquartil de M1, M2, M3;  
     - Distribuição de respostas Likert (frequências e médias) para M4–M10;  
     - Taxa de sucesso M11.

3. **Teste de normalidade**
   - Aplicar o **teste de Shapiro–Wilk** para verificar a normalidade das distribuições de M1, M2, M3 (por arquitetura).

4. **Comparação entre arquiteturas (teste de hipóteses)**
   - Como se trata de dados pareados (mesmos participantes em ambas as arquiteturas), e assumindo que a normalidade provavelmente não será satisfeita:
     - Utilizar o **teste de Wilcoxon Signed-Rank** para comparar:
       - Tempo de compreensão (M1) entre Camadas e Clean (H1);  
       - Tempo de implementação (M2) (H2);  
       - Tamanho da mudança (M3) (H2);  
       - Escores Likert (M4–M10) (H3);  
     - Comparar taxas de sucesso (M11) por meio de proporções (por exemplo, teste de sinais ou análise descritiva reforçada).

5. **Associações entre métricas objetivas e percepções (H4)**
   - Calcular correlações (por exemplo, **Spearman**) entre:
     - M1, M2, M3, M11 e os escores médios de M4–M10;  
   - Verificar se menores tempos e tamanhos de mudança se associam a percepções mais positivas de clareza, facilidade e evolutividade.

6. **Interpretação e ligação com as hipóteses**
   - Para cada hipótese (H1–H4):
     - Verificar se os resultados suportam ou não a hipótese substantiva;  
     - Discutir implicações práticas para escolha entre Clean Architecture e arquitetura em camadas;  
     - Identificar possíveis ameaças à validade (tamanho da amostra, viés de aprendizagem residual, experiência prévia etc.).

Esse plano de análise garante que, ao final da coleta, o experimento esteja alinhado ao problema de pesquisa, às hipóteses formuladas e às boas práticas de experimentação em Engenharia de Software.

### 4.5 Fluxograma operacional do experimento

O fluxograma a seguir sintetiza o passo a passo operacional do experimento, destacando os principais stakeholders envolvidos, instrumentos utilizados, variáveis e métricas coletadas em cada etapa.

```mermaid
flowchart TD
    A["Planejamento do experimento (autor e orientadores)"] --> B["Preparação do ambiente (laboratório, IDE, JDK 17, Git, formulários)"]
    B --> C["Configuração dos repositórios (Arquitetura em Camadas e Clean Architecture)"]
    C --> D["Definição dos grupos Seq1 e Seq2 (ordem Camadas-Clean ou Clean-Camadas)"]
    D --> E["Briefing aos participantes (objetivo, ética, instruções gerais)"]
    E --> F["Tarefa 1 - Compreensão na Arquitetura 1 (coleta de M1, M4, M6)"]
    F --> G["Tarefa 2 - Implementação na Arquitetura 1 (coleta de M2, M3, M11, M5, M7, M8, M9)"]
    G --> H["Tarefa 3 - Compreensão na Arquitetura 2 (coleta de M1, M4, M6)"]
    H --> I["Tarefa 4 - Implementação na Arquitetura 2 (coleta de M2, M3, M11, M5, M7, M8, M9, M10)"]
    I --> J["Encerramento em sala (comentários qualitativos dos estudantes)"]
    J --> K["Consolidação dos dados (autor e orientadores)"]
    K --> L["Análise estatística e interpretação (aplicação do plano da Seção 4.4)"]
    L --> M["Redação dos resultados e conclusões (autor e orientadores)"]

