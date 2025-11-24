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

- **Autores**  
  - Adquirem experiência prática em desenho, condução e análise de experimento controlado em Engenharia de Software;  
  - Produzem evidências que podem ser publicadas ou reutilizadas em disciplinas futuras.

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
   - Pelo menos um número mínimo de participantes (por exemplo, ≥ 60) completar todas as tarefas em ambas as arquiteturas, com dados consistentes.

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

Abaixo são apresentadas todas as métricas previstas no planejamento, com descrição e unidade.  
Atende ao requisito de haver **pelo menos 10 métricas diferentes**.

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
| M12  | **Diferença relativa de tempo entre arquiteturas** – razão entre os tempos médios de compreensão/implementação (por exemplo, tempo\_Clean ÷ tempo\_Camadas) para cada tipo de tarefa. | Valor adimensional (razão entre tempos) |

---

### 2.8 Síntese textual do GQM

O modelo GQM organiza o experimento de forma sistemática:

- A partir dos **objetivos específicos** (OE1–OE4) foram definidas **perguntas** que explicitam o que se deseja saber sobre esforço de compreensão, esforço de implementação, percepções dos participantes e apoio à decisão arquitetural.
- Para cada pergunta foram associadas **métricas objetivas** (tempos, tamanho da mudança, taxa de sucesso) e **métricas subjetivas** (escores em escala Likert), garantindo pelo menos duas métricas por pergunta.
- As métricas são reutilizadas em diferentes perguntas quando necessário, assegurando consistência e permitindo análises cruzadas entre esforço, percepções e resultados.

Essa estrutura fornece uma base clara para a coleta e análise de dados, garantindo alinhamento entre o problema de pesquisa, os objetivos do TCC, o desenho experimental e as métricas que serão efetivamente observadas.

---
