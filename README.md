# Documento de Visão – TCC de Pós-Graduação em Engenharia de Software

#### Testes Exploratórios vs Testes Automatizados: Uma Análise Comparativa na Detecção de Defeitos com Integração Jenkins, Cypress, Telegram e Validação via K6

### 1. Introdução
##### 1.1 Propósito
Este documento apresenta a visão geral de um projeto de software desenvolvido para fins acadêmicos, no contexto da pós-graduação em Engenharia de Software. O projeto tem como objetivo central explorar, comparar e validar abordagens de teste de software, integradas a um processo completo de desenvolvimento, incluindo: definição de requisitos, modelagem, arquitetura, implementação, qualidade e validação contínua.
##### 1.2 Escopo
Será desenvolvido um sistema web simulado para cadastro e consulta de usuários (CRUD). Esse sistema servirá como base para aplicar os testes automatizados e exploratórios. Todo o ciclo de engenharia será percorrido: desde a concepção do sistema, levantamento de requisitos, modelagem, implementação, testes e integração com ferramentas como Jenkins, Telegram API e K6.

### 2. Posicionamento
##### 2.1 Oportunidade
Empresas modernas enfrentam dilemas recorrentes sobre como implementar estratégias de testes eficazes e sustentáveis. Muitas vezes, faltam critérios claros para escolher entre testes manuais e automatizados. Este projeto busca oferecer dados reais e aplicáveis, simulando um ciclo completo de engenharia e integrando ferramentas modernas para tomada de decisão orientada por evidências.
##### 2.2 Declaração do Problema
| O problema | Afeta | Impacto | Uma solução eficaz seria |
|---|:---:|---:|---:|
| Escolha ineficaz entre testes manuais e automatizados | Equipes de QA, desenvolvedores e líderes técnicos | Custos elevados com manutenção de software e bugs em produção | Um estudo comparativo técnico embasado, com métricas de eficácia, esforço e confiabilidade |

### 3. Partes Interessadas
| Parte Interessada       | Papel                       | Interesse                                             |
| ----------------------- | --------------------------- | ----------------------------------------------------- |
| Desenvolvedor (Nagybhe) | Aluno e responsável técnico | Conclusão acadêmica e domínio prático das ferramentas |
| Orientador              | Supervisor acadêmico        | Aderência às boas práticas de engenharia              |
| Comunidade Técnica      | Público externo             | Compartilhamento de conhecimento, reuso da solução    |

### 4. Descrição da Solução
##### 4.1 Visão Geral
Será desenvolvido um sistema web (ex: cadastro de usuários), com arquitetura em camadas. A partir disso, serão aplicadas duas abordagens de testes:
* Exploratórios: executados manualmente com foco em cenários não previstos.
* Automatizados: criados com Cypress, executados via Jenkins.
* Notificações via Telegram: envio automático do status de testes.
* Validação via K6: testes de carga na API do Telegram para garantir robustez da comunicação automatizada.

### 5. Requisitos
##### 5.1 Requisitos Funcionais (RF)
| ID   | Descrição                                                                |
| ---- | ------------------------------------------------------------------------ |
| RF01 | O sistema deve permitir cadastro de usuários com nome, e-mail e telefone |
| RF02 | O sistema deve permitir listagem e busca de usuários cadastrados         |
| RF03 | O sistema deve notificar via Telegram o sucesso ou falha dos testes      |

##### 5.2 Requisitos Não Funcionais (RNF)
| ID    | Descrição                                                                              |
| ----- | -------------------------------------------------------------------------------------- |
| RNF01 | A aplicação deve responder em até 2 segundos por requisição                            |
| RNF02 | O sistema deve ser testado com no mínimo 100 requisições simultâneas à API do Telegram |
| RNF03 | Os testes automatizados devem cobrir ao menos 80% das funcionalidades                  |

### 6. Modelagem
##### 6.1 Casos de Uso
* Cadastrar Usuário
* Listar Usuários
* Buscar Usuário
* Executar Testes Automatizados
* Notificar via Telegram
##### 6.2 Diagrama de Casos de Uso
**(Aqui você pode inserir um diagrama com ferramentas como Draw.io, Lucidchart ou PlantUML)**

### 7. Arquitetura do Sistema
##### 7.1 Arquitetura em Camadas
* Aplicação (Front-End): React
* Aplicação (Back-End): Node.js + Express
* Persistência: Postgres
* Automação de Testes: Cypress + Jenkins + Telegram
* Performance: K6
* conteinerização | virtualização: Docker

### 8. Processo de Desenvolvimento
Será utilizado um processo iterativo e incremental baseado no ciclo ágil. As fases serão:
* Levantamento de requisitos
* Modelagem
* Implementação do sistema
* Planejamento e execução de testes (exploratórios e automatizados)
* Integração com Telegram + K6
* Coleta de métricas
* Análise comparativa

### 9. Testes e Validação
| Tipo         | Ferramenta   | Objetivo                                   |
| ------------ | ------------ | ------------------------------------------ |
| Exploratório | Manual       | Identificar falhas inesperadas             |
| Automatizado | Cypress      | Testar cenários definidos com CI           |
| Notificação  | Telegram API | Avisar sobre o resultado dos testes        |
| Performance  | K6           | Validar estabilidade da API de notificação |

### 10. Métricas de Avaliação
| Métrica                                       | Avaliação                    |
| --------------------------------------------- | ---------------------------- |
| % de falhas detectadas                        | Por tipo de teste            |
| Tempo médio para detectar falha               | Exploratório vs Automatizado |
| Cobertura de código                           | Cypress (via cobertura)      |
| Latência e disponibilidade da API do Telegram | Testada via K6               |

### 11. Riscos e Restrições
| Risco                     | Impacto                | Mitigação                                 |
| ------------------------- | ---------------------- | ----------------------------------------- |
| Falhas na API do Telegram | Falha nas notificações | Testes de stress com K6                   |
| Complexidade do Jenkins   | Atrasos na integração  | Documentação e testes iterativos          |
| Baixa severidade dos bugs | Comparação enviesada   | Inserção de falhas controladas no sistema |

### 12. Cronograma de Execução
| Semana | Atividade                                  |
| ------ | ------------------------------------------ |
| 1–2    | Levantamento de requisitos e modelagem     |
| 3–4    | Implementação do sistema base              |
| 5      | Testes exploratórios                       |
| 6      | Criação dos testes automatizados (Cypress) |
| 7      | Integração com Jenkins                     |
| 8      | Integração com Telegram e bot Node.js      |
| 9      | Testes de performance com K6               |
| 10     | Coleta de dados e análise comparativa      |
| 11     | Redação final do documento                 |
| 12     | Revisão e entrega do TCC                   |

### 13. Apêndices (a incluir futuramente)
* Scripts de teste Cypress
* Jenkinsfile
* Código do bot Telegram
* Script K6
* Relatório de cobertura
* Gráficos e planilhas de métricas