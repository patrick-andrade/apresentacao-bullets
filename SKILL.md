---
name: apresentacao-bullets
description: Reorganiza apresentações existentes em bullets hierárquicos, preservando conteúdo, fontes e identidade visual.
disable-model-invocation: true
license: MIT
metadata:
  author: Patrick Andrade
  version: "1.1.0"
---

# Apresentação — bullets

Transforme conteúdo plano em uma cadeia visual de **ideia principal → premissas ou mecanismo → resultado ou implicação**. Atue na microestrutura textual de apresentações existentes ou de rascunhos já produzidos.

Esta skill complementa o planejamento pedagógico da `aula-academica`: preserve a arquitetura da aula já definida e concentre-se na hierarquia que torna o raciocínio visível em cada slide.

## Preserve o escopo

- Preserve significado, sequência argumentativa, fatos, fontes, tabelas, gráficos, fórmulas, código, layouts e elementos visuais.
- Preserve tema, template, mestre, placeholders, quantidade de slides e conteúdo substantivo, salvo autorização expressa para alterá-los.
- Faça apenas ajustes leves de redação necessários à hierarquia: rótulos semânticos, paralelismo, pontuação e remoção de duplicações literais.
- Trabalhe apenas com argumentos, dados e fontes já presentes. Quando a reorganização revelar uma lacuna substantiva, sinalize-a em vez de preenchê-la.
- Trate títulos, divisores de seção, tabelas, gráficos, equações em destaque, blocos de código e mídia como elementos próprios; organize o texto que os contextualiza sem convertê-los artificialmente em listas.

## Fluxo de trabalho

1. Inspecione a apresentação inteira e o template antes de editar. Identifique a hierarquia nativa de parágrafos, os padrões de layout e as instruções específicas do usuário.
2. Em cada slide substantivo, determine a ideia principal e agrupe o restante por função lógica: conceito, diagnóstico, premissas, mecanismo, evidência, resultado, implicação, limite ou decisão.
3. Converta parágrafos soltos, citações e listas genéricas em uma hierarquia coerente:
   - primeiro nível para os blocos lógicos;
   - segundo nível para explicações, evidências, etapas e alternativas;
   - terceiro nível somente quando uma distinção indispensável não couber nos dois primeiros.
4. Preserve uma lista numerada apenas quando ordem, prioridade ou contagem tiver significado. Nos demais casos, use bullets hierárquicos.
5. Aplique as regras do formato abaixo e renderize o resultado.
6. Inspecione todos os slides renderizados e corrija a estrutura até que a hierarquia seja visível e não haja texto unido, corte ou sobreposição.

Leia [`references/padroes-de-reorganizacao.md`](references/padroes-de-reorganizacao.md) antes de editar fontes com parágrafos planos, cadeias causais, premissas, exercícios, fórmulas, colunas, notas ou hierarquia parcial.

## Quarto e Markdown

- Coloque cada parágrafo de corpo dentro de um item iniciado por `-`, salvo os elementos próprios definidos acima.
- Use quatro espaços para cada sublista e mantenha uma linha em branco entre o bullet-pai e a sublista. Esse espaçamento é um requisito de renderização, não uma preferência estilística.
- Preserve blocos Div, colunas, tabelas, gráficos, equações, código e atributos Quarto em sua sintaxe original.
- Use marcadores Markdown; não insira o caractere visual `•` no texto.
- Renderize pelo mesmo fluxo usado pelo projeto e confira o arquivo final, não apenas a fonte.

## PowerPoint e Google Slides

- Use os níveis nativos de parágrafo e os placeholders do template, no PowerPoint e no Google Slides. As duas ferramentas expõem a mesma hierarquia de lista; esta skill não usa conector, API nem exportação automática entre elas.
- Preserve a formatação herdada do layout e do mestre.
- Não simule listas digitando caracteres de bullet manualmente.
- Mantenha gráficos, tabelas, fórmulas, código e elementos visuais em seus objetos próprios.

## Notas e rastreabilidade

- Remova notas bibliográficas somente quando o usuário solicitar.
- Quando solicitado, notas repetitivas de livro, capítulo ou página podem ser removidas se a referência-base já estiver estabelecida para os alunos.
- Mantenha fontes oficiais, dados atuais, citações diretas, ativos externos e alegações que exijam rastreabilidade.
- Se uma nota combinar conteúdo repetitivo e uma fonte necessária, preserve a parte necessária.

## Critério de conclusão

Conclua somente quando:

- todo texto substantivo de corpo estiver no nível lógico adequado ou em um elemento próprio;
- o significado e a ordem do argumento permanecerem intactos;
- as fontes e notas remanescentes atenderem à política acima;
- todos os slides tiverem sido renderizados e inspecionados integralmente;
- não houver bullets unidos ao item-pai, hierarquia acidentalmente achatada, texto cortado ou elementos sobrepostos.
