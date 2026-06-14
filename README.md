# Agent Skills Library

Biblioteca de agentes em Markdown para orientar ferramentas de IA na criação, revisão, documentação e validação de projetos de software.

A proposta deste repositório é transformar prompts soltos em agentes reutilizáveis, com responsabilidades claras, critérios de qualidade, limites de atuação e formatos de entrega bem definidos.

---

## Objetivo

Este projeto foi criado para organizar agentes especializados que podem ser usados em assistentes de IA, IDEs com copilotos, ferramentas de coding agents e fluxos de desenvolvimento assistido por IA.

Cada agente define:

* Quando deve ser usado.
* Qual papel deve assumir.
* Como deve pensar antes de responder.
* Quais limites não deve ultrapassar.
* Como deve gerar código, documentação ou validação.
* Como deve reportar entregas e pendências.
* Como deve lidar com validações reais ou não executadas.

O foco é aumentar a qualidade, previsibilidade e segurança no uso de IA durante o desenvolvimento de software.

---

## Agentes disponíveis

### Frontend Design Agent

Arquivo:

```txt
agents/frontend-design-agent.md
```

Agente especializado em criação, refatoração e melhoria de interfaces frontend.

Pode ser usado para:

* Páginas web.
* Dashboards.
* Componentes.
* Formulários.
* Modais.
* Sidebars.
* Cards.
* Tabelas.
* Layouts responsivos.
* Melhorias de UI/UX.
* Interfaces em React, Svelte, Vue, HTML e CSS.

Principais focos:

* Pensamento de produto.
* Qualidade visual.
* Responsividade.
* Acessibilidade básica.
* Escopo controlado.
* Código necessário, sem refatorações paralelas.
* Validação honesta, sem afirmar execução quando ela não aconteceu.

---

### Frontend QA Agent

Arquivo:

```txt
agents/frontend-qa-agent.md
```

Agente especializado em validação frontend antes de revisão, entrega ou pull request.

Pode ser usado para:

* Revisar telas implementadas.
* Validar responsividade.
* Conferir fluxos de usuário.
* Testar estados de interface.
* Identificar problemas visuais.
* Revisar acessibilidade básica.
* Avaliar risco de regressão.

Principais focos:

* Fluxo principal do usuário.
* Layout em desktop, tablet e mobile.
* Estados de loading, erro, vazio e sucesso.
* Consistência visual.
* Acessibilidade básica.
* Build, lint e validações recomendadas.

---

### Documentation Agent

Arquivo:

```txt
agents/documentation-agent.md
```

Agente especializado em criação e melhoria de documentação técnica, funcional e de produto.

Pode ser usado para:

* README.
* Guias de setup.
* Documentação de arquitetura.
* Fluxos de usuário.
* Documentação de APIs.
* Changelogs.
* Resumos de entrega.
* Documentação de agentes.
* Materiais de onboarding.

Principais focos:

* Clareza.
* Organização.
* Precisão.
* Público-alvo.
* Separação entre implementação atual e melhorias futuras.
* Evitar invenção de funcionalidades, comandos ou endpoints.

---

## Template disponível

### Agent Template

Arquivo:

```txt
templates/agent-template.md
```

Modelo base para criação de novos agentes em Markdown.

Use este template quando quiser criar um novo agente com:

* Frontmatter.
* Escopo claro.
* Modos de operação.
* Missão principal.
* Regras de trabalho.
* Restrições.
* Formato de saída.
* Comportamento de validação.

---

## Estrutura do repositório

```txt
agent-skills-library/
├── README.md
├── agents/
│   ├── frontend-design-agent.md
│   ├── frontend-qa-agent.md
│   └── documentation-agent.md
├── templates/
│   └── agent-template.md
└── examples/
```

---

## Como usar

Escolha o agente mais adequado para a tarefa e forneça o conteúdo dele como contexto para a ferramenta de IA que estiver usando.

Exemplo de uso:

```md
Use o agente `frontend-design-agent`.

Tarefa:
Refatorar a sidebar da aplicação para melhorar responsividade em telas menores.

Contexto:
A aplicação é um dashboard web com navegação lateral, área principal de conteúdo e componentes reutilizáveis.

Critérios de aceite:
- Não pode gerar overflow horizontal.
- Deve funcionar em desktop, tablet e mobile.
- Não deve alterar regras de backend.
- Deve manter o padrão visual existente.
- Deve recomendar validação com `npm run lint` e `npm run build`.

Entrega esperada:
- Arquivos que devem ser alterados.
- Código ou instruções de implementação.
- Validação recomendada.
- Riscos ou pontos de atenção.
```

---

## Modos de operação

Os agentes deste repositório foram escritos considerando dois modos de uso.

### Assistant Mode

Modo usado quando a IA não tem acesso direto aos arquivos, terminal ou ambiente de execução.

Nesse modo, o agente deve:

* Sugerir alterações.
* Explicar onde aplicar o código.
* Informar comandos de validação.
* Declarar que a validação não foi executada.
* Não afirmar que editou arquivos ou rodou comandos.

### Executor Mode

Modo usado quando a IA tem acesso real ao projeto, arquivos e terminal.

Nesse modo, o agente pode:

* Ler arquivos.
* Editar código.
* Executar comandos.
* Reportar resultados reais.
* Listar arquivos alterados.
* Informar falhas de validação.

O agente só deve afirmar que algo foi executado se isso realmente aconteceu.

---

## Princípios dos agentes

Todos os agentes deste repositório seguem alguns princípios gerais:

* Escopo controlado.
* Clareza antes de complexidade.
* Validação honesta.
* Sem alucinação de comandos, arquivos ou features.
* Sem alteração fora do pedido.
* Sem dependências novas sem justificativa.
* Sem prometer execução quando não há ferramenta para executar.
* Separação entre fatos confirmados, sugestões e pendências.
* Entregas úteis, revisáveis e fáceis de manter.

---

## Para quem este repositório é útil

Este repositório pode ser útil para:

* Pessoas desenvolvedoras.
* Analistas de dados que trabalham com produtos digitais.
* Estudantes de tecnologia.
* Times que usam IA no desenvolvimento.
* Pessoas criando copilotos internos.
* Quem deseja padronizar o uso de IA em projetos.
* Quem quer transformar prompts soltos em agentes reutilizáveis.

---

## Próximos agentes planejados

Ideias de próximos agentes:

* Backend Agent.
* Code Review Agent.
* Data Analytics Agent.
* Power BI Agent.
* Product Requirements Agent.
* Git Workflow Agent.
* API Documentation Agent.
* Testing Agent.

---

## Status do projeto

Este repositório está em evolução.

A primeira versão contém agentes focados em frontend, QA visual e documentação.
Novos agentes, exemplos de uso e melhorias nos templates serão adicionados conforme os fluxos forem testados em projetos reais.

---

## Licença

Consulte o arquivo `LICENSE.txt` para os termos completos de uso.
