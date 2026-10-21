---
name: apresentacao-bullets
description: Reorganiza apresentações existentes em bullets hierárquicos, preservando conteúdo, fontes e identidade visual.
disable-model-invocation: true
license: MIT
metadata:
  author: Patrick Andrade
  version: "1.2.0"
---

# Apresentação — bullets

Transforme conteúdo plano em uma cadeia visual de **ideia principal → premissas ou mecanismo → resultado ou implicação**. Atue na microestrutura textual de apresentações existentes ou de rascunhos já produzidos.

Esta skill complementa o planejamento pedagógico da `aula-academica`: preserve a arquitetura da aula já definida e concentre-se na hierarquia que torna o raciocínio visível em cada slide.

## Preserve o escopo

- Preserve significado, sequência argumentativa, fatos, fontes, tabelas, gráficos, fórmulas, código, layouts e elementos visuais.
- Preserve tema, template, mestre, placeholders, quantidade de slides e conteúdo substantivo, salvo autorização expressa para alterá-los.
- Faça apenas ajustes leves de redação necessários à hierarquia: rótulos (conforme a seção abaixo), paralelismo, pontuação e remoção de duplicações literais.
- Trabalhe apenas com argumentos, dados e fontes já presentes. Quando a reorganização revelar uma lacuna substantiva, sinalize-a em vez de preenchê-la.
- Trate títulos, divisores de seção, tabelas, gráficos, equações em destaque, blocos de código e mídia como elementos próprios; organize o texto que os contextualiza sem convertê-los artificialmente em listas.

## Fluxo de trabalho

1. Inspecione a apresentação inteira e o template antes de editar. Identifique a hierarquia nativa de parágrafos, os padrões de layout, a convenção de caixa e ênfase do deck e as instruções específicas do usuário.
2. Em cada slide substantivo, determine a ideia principal e agrupe o restante por função lógica: conceito, diagnóstico, premissas, mecanismo, evidência, resultado, implicação, limite ou decisão.
3. Converta parágrafos soltos, citações e listas genéricas em uma hierarquia coerente:
   - primeiro nível para os blocos lógicos;
   - segundo nível para explicações, evidências, etapas e alternativas;
   - terceiro nível somente quando uma distinção indispensável não couber nos dois primeiros.
4. Preserve uma lista numerada apenas quando ordem, prioridade ou contagem tiver significado. Nos demais casos, use bullets hierárquicos.
5. Aplique as regras de rótulos e do formato abaixo e grave o resultado no destino indicado em [Onde gravar](#onde-gravar).
6. Renderize e inspecione todos os slides. Corrija a estrutura até que a hierarquia seja visível e não haja texto unido, corte ou sobreposição; quando o texto não couber, siga [Quando o texto não cabe](#quando-o-texto-não-cabe).
7. Entregue o [relatório final](#relatório-final).

Leia [`references/padroes-de-reorganizacao.md`](references/padroes-de-reorganizacao.md) antes de editar fontes com parágrafos planos, cadeias causais, premissas, exercícios, fórmulas, colunas, notas ou hierarquia parcial.

## Rótulos, ênfase e pontuação

- Use um rótulo funcional (`Mecanismo:`, `Premissas:`, `Critérios de decisão:`) quando ele agrupar sub-bullets ou nomear uma função que a frase não deixa clara. Quando a frase já expressa a ideia, deixe o item de primeiro nível sem rótulo.
- Escreva o rótulo em texto simples, com a mesma ênfase do corpo. Aplique negrito somente quando o template ou o usuário pedir; ênfase que já estava no original permanece.
- Varie os rótulos conforme a função real de cada bloco; uma série fixa repetida em todos os slides (Conceito, Mecanismo, Resultado) vira tique visual.
- Abra uma sublista apenas com dois ou mais itens; um item isolado volta para a linha do pai.
- Termine cada item sem pontuação final (`;` ou `.`). Mantenha a pontuação interna das frases e o `?` das perguntas.
- Comece com minúscula o texto que segue um rótulo com dois-pontos. Para a inicial dos demais itens, siga a convenção do deck; sem convenção, use maiúscula.

## Quarto e Markdown

- Coloque cada parágrafo de corpo dentro de um item iniciado por `-`, salvo os elementos próprios definidos acima.
- Use quatro espaços para cada sublista e mantenha uma linha em branco entre o bullet-pai e a sublista. Esse espaçamento é um requisito de renderização, não uma preferência estilística.
- Preserve blocos Div, colunas, tabelas, gráficos, equações, código e atributos Quarto em sua sintaxe original.
- Use marcadores Markdown; o caractere visual `•` pertence ao tema.
- Renderize pelo mesmo fluxo usado pelo projeto (em geral `quarto render`) e confira o arquivo final, não apenas a fonte.

## PowerPoint e Google Slides

- Use os níveis nativos de parágrafo e os placeholders do template. As duas ferramentas expõem a mesma hierarquia de lista.
- Preserve a formatação herdada do layout e do mestre.
- Crie listas pelos níveis nativos de parágrafo, nunca digitando caracteres de bullet.
- Mantenha gráficos, tabelas, fórmulas, código e elementos visuais em seus objetos próprios.
- Google Slides: quando o ambiente oferecer um conector do Google Slides, use-o para ler o deck, editar os níveis de parágrafo e conferir as miniaturas dos slides. Sem conector, entregue as mudanças por slide para o usuário aplicar no deck aberto. A skill funciona sem conector e não instala nenhum.

## Onde gravar

- Quarto e Markdown: edite o próprio arquivo-fonte.
- PowerPoint: grave em uma cópia `<nome>-bullets.pptx` ao lado do original, salvo pedido para editar o original.
- Google Slides: edite o deck indicado pelo usuário; o histórico de versões preserva o estado anterior.

## Quando o texto não cabe

1. Ajuste o conteúdo para caber no slide: enxugue a redação, reagrupe itens e retire redundâncias, preservando todo argumento, dado e fonte.
2. Se o resultado continuar inadequado (texto cortado, ilegível ou com perda de sentido), indique o slide ao usuário e proponha a divisão, com o ponto de corte sugerido.
3. Divida o slide somente após autorização.

## Inspeção

- Quarto: renderize e percorra a saída (HTML, PDF ou `.pptx`) slide a slide.
- PowerPoint: converta para PDF ou imagens com a ferramenta disponível (por exemplo, `soffice --headless --convert-to pdf`) e inspecione cada página.
- Google Slides: confira as miniaturas pelo conector ou peça ao usuário capturas dos slides alterados.
- Sem meio de renderizar, registre no relatório quais slides ficaram sem verificação visual.

## Notas e rastreabilidade

- Remova notas bibliográficas somente quando o usuário solicitar.
- Quando solicitado, notas repetitivas de livro, capítulo ou página podem ser removidas se a referência-base já estiver estabelecida para os alunos.
- Mantenha fontes oficiais, dados atuais, citações diretas, ativos externos e alegações que exijam rastreabilidade.
- Se uma nota combinar conteúdo repetitivo e uma fonte necessária, preserve a parte necessária.

## Relatório final

Entregue ao usuário, em lista curta:

- arquivo ou deck gravado;
- slides reorganizados, com uma linha sobre a mudança estrutural de cada um;
- lacunas substantivas sinalizadas;
- notas removidas;
- slides que não couberam e a divisão proposta;
- slides sem verificação visual, se houver.

## Critério de conclusão

Conclua somente quando:

- todo texto substantivo de corpo estiver no nível lógico adequado ou em um elemento próprio;
- o significado e a ordem do argumento permanecerem intactos;
- rótulos, ênfase e pontuação seguirem a seção correspondente;
- as fontes e notas remanescentes atenderem à política acima;
- todos os slides tiverem sido renderizados e inspecionados, ou os não verificados estiverem listados no relatório;
- não houver bullets unidos ao item-pai, hierarquia acidentalmente achatada, texto cortado ou elementos sobrepostos;
- o relatório final tiver sido entregue.
