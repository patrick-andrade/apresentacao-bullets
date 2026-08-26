# apresentacao-bullets

Skill para reorganizar apresentações já existentes em bullets hierárquicos, sem mudar o argumento, as fontes nem a identidade visual.

O aplicativo do agente lê esta ficha e atua na microestrutura de cada slide: ideia principal, premissas ou mecanismo, resultado ou implicação. Não planeja a aula e não inventa conteúdo.

Funciona no [padrão aberto Agent Skills](https://agentskills.io/specification) (`SKILL.md`). Complementa [aula-academica](https://github.com/patrick-andrade/aula-academica): aquela skill define a arquitetura pedagógica; esta torna a hierarquia visível no texto já produzido.

Guia: [Skills na Prática](https://patrick-andrade.github.io/guias/skills-na-pratica.html).

## O que ela faz

- Converte parágrafos soltos e listas genéricas em uma hierarquia de um a três níveis.
- Preserva template, quantidade de slides, tabelas, gráficos, fórmulas, código e notas que exigem rastreabilidade.
- Serve em Quarto, Markdown, PowerPoint e Google Slides, editando o arquivo ou o deck aberto. Não instala Google Workspace nem usa conector, API ou exportação automática entre ferramentas.

A skill guarda o *como*. O chat continua dizendo *qual* apresentação e *o que* pode mudar.

## Instalar

O caminho mais simples para quem está começando é o **Codex**, com a pasta do curso apontada. O mesmo arquivo vale no Claude Code e no Cursor.

**Neste projeto** (recomendado para um curso):

```bash
npx skills add patrick-andrade/apresentacao-bullets
```

**Em todos os projetos desta máquina** (se você usa a skill em várias disciplinas):

```bash
npx skills add patrick-andrade/apresentacao-bullets --global
```

`npx` vem com o Node.js e baixa o instalador na hora. Sem isso, copie a pasta da skill para:

```text
.agents/skills/apresentacao-bullets/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── padroes-de-reorganizacao.md
```

na raiz da pasta do curso. No Claude Code, o equivalente é `.claude/skills/apresentacao-bullets/`. No Cursor, `.agents/skills/` também costuma bastar. Inclua `references/` e `agents/`; o `SKILL.md` sozinho não carrega os padrões de reorganização.

Abra um **chat novo** depois de instalar.

## Pedir

**Cursor** (linguagem natural; a description dispara a skill):

```text
Reorganize estes slides em bullets hierárquicos.
Preserve conteúdo, fontes e o template.
```

**Codex** (invocação explícita):

```text
Use $apresentacao-bullets para reorganizar esta apresentação
em bullets hierárquicos, preservando conteúdo, fontes e
identidade visual.
```

## Licença

[MIT](LICENSE). Você pode usar, copiar e adaptar nos seus cursos; mantenha o aviso de copyright e da licença.
