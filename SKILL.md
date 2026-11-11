---
name: apresentacao-bullets
description: Reorganiza apresentações existentes em bullets hierárquicos, preservando conteúdo, fontes e identidade visual.
disable-model-invocation: true
license: MIT
metadata:
  author: Patrick Andrade
  version: "1.3.0"
---

# Apresentação — bullets

Torne visível, na hierarquia dos bullets, o raciocínio que cada slide já contém: cada trecho no nível da sua função e na ordem em que um depende do outro, com a definição antes do uso e as premissas antes do resultado. Atue na microestrutura textual de apresentações existentes ou de rascunhos já produzidos.

Esta skill cuida da forma. O que o slide afirma, como ele abre, que fontes mostra e quantos slides existem são decisões de conteúdo: pertencem ao autor ou, em aulas, à skill `aula-academica`, cujo contrato da lâmina prevalece quando as duas forem usadas. A ordem de uso é produzir o conteúdo, aplicar esta skill e só então auditar.

## Preserve o escopo

- Preserve significado, fatos, fontes, tabelas, gráficos, fórmulas, código, layouts e elementos visuais.
- Preserve tema, template, mestre, placeholders, quantidade e ordem dos slides e conteúdo substantivo, salvo autorização expressa para alterá-los.
- Dentro de um slide, mude a ordem dos blocos somente para restaurar a dependência lógica (definição antes do uso, premissas antes do resultado, pergunta antes da resposta) e registre a mudança no relatório.
- Faça apenas ajustes leves de redação necessários à hierarquia: rótulos e conectivos (conforme a seção abaixo), paralelismo, pontuação e remoção de duplicações literais.
- Trabalhe apenas com argumentos, dados e fontes já presentes. Quando a reorganização revelar uma lacuna substantiva, sinalize-a em vez de preenchê-la.
- Trate títulos, divisores de seção, tabelas, gráficos, equações em destaque, blocos de código e mídia como elementos próprios; organize o texto que os contextualiza sem convertê-los artificialmente em listas.

## Fluxo de trabalho

1. Inspecione a apresentação inteira e o template antes de editar. Identifique a hierarquia nativa de parágrafos, os padrões de layout, a convenção de caixa, ênfase e rótulos do deck e as instruções específicas do usuário.
2. Em cada slide substantivo, identifique a função de cada trecho (pergunta, definição, premissas, mecanismo, evidência, resultado, implicação, limite ou decisão) e o que depende de quê.
3. Converta parágrafos soltos, citações e listas genéricas em uma hierarquia coerente:
   - primeiro nível para os blocos lógicos;
   - segundo nível para explicações, evidências, etapas e alternativas;
   - terceiro nível somente quando uma distinção indispensável não couber nos dois primeiros.
4. Preserve uma lista numerada apenas quando ordem, prioridade ou contagem tiver significado. Nos demais casos, use bullets hierárquicos.
5. Aplique as regras de rótulos, conectivos e formato abaixo e grave o resultado no destino indicado em [Onde gravar](#onde-gravar).
6. Faça a [checagem de consistência](#checagem-de-consistência) em cada slide alterado.
7. Renderize e inspecione todos os slides. Corrija a estrutura até que a hierarquia seja visível e não haja texto unido, corte ou sobreposição; quando o texto não couber, siga [Quando o texto não cabe](#quando-o-texto-não-cabe).
8. Entregue o [relatório final](#relatório-final).

Leia [`references/padroes-de-reorganizacao.md`](references/padroes-de-reorganizacao.md) antes de editar fontes com parágrafos planos, cadeias causais, premissas, exercícios, fórmulas, colunas, notas, hierarquia parcial ou blocos fora da ordem de dependência.

## Rótulos, conectivos e pontuação

O rótulo classifica um trecho; o conectivo mostra por que um trecho decorre do outro. Um argumento precisa do segundo.

- Ligue os passos de uma cadeia com o conectivo que o texto original autoriza (porque, por isso, logo, mas, se… então) ou com numeração, quando a ordem for o próprio argumento. Se a relação entre dois passos não estiver clara no original, sinalize em vez de escolher uma.
- Rótulo de bloco, o que abre uma sublista: texto simples, sem dois-pontos (`- Hipóteses`). O recuo já mostra que os itens abaixo pertencem a ele.
- Rótulo na linha, seguido de texto no mesmo item: com dois-pontos (`- Exemplo: a iluminação das ruas`). Use-o quando a frase não conseguir dizer sua função sozinha, como em exemplo, fonte, tarefa ou pergunta. Para resultado, conclusão e implicação, prefira a frase com conectivo: `- Por isso, a produção fica acima do nível eficiente`.
- Dê referente ao rótulo: `- Dois tipos de bem público`, e não `- Dois tipos`.
- Quando a frase já expressa a ideia, deixe o item de primeiro nível sem rótulo.
- Escreva o rótulo em texto simples, com a mesma ênfase do corpo. Aplique negrito somente quando o template ou o usuário pedir; ênfase que já estava no original permanece.
- Varie os rótulos conforme a função real de cada bloco; uma série fixa repetida em todos os slides (Conceito, Mecanismo, Resultado) vira tique visual.
- Abra uma sublista apenas com dois ou mais itens; um item isolado volta para a linha do pai.
- Termine cada item sem pontuação final (`;` ou `.`). Mantenha a pontuação interna das frases e o `?` das perguntas.
- Comece com minúscula o texto que segue um rótulo com dois-pontos. Para a inicial dos demais itens, siga a convenção do deck; sem convenção, use maiúscula.
- Se o deck já usa outra convenção de rótulos de modo consistente (por exemplo, dois-pontos em todo rótulo de bloco), mantenha-a e pergunte ao usuário antes de padronizar.

## Checagem de consistência

Leia os itens de cada slide em sequência, como um parágrafo. O slide passa quando a leitura forma um argumento em que nada é usado antes de aparecer.

Corrija o que é forma e sinalize no relatório o que pede conteúdo novo:

| Sinal | O que fazer |
|---|---|
| Resultado ou afirmação antes das premissas ou da definição que ele usa, todas presentes no slide | reordene os blocos e registre |
| Rótulo sem referente | complete com o termo que o próprio slide já traz, ou leve a sublista para junto dele |
| Etapas de uma cadeia sem ligação | acrescente o conectivo que o original autoriza ou numere |
| Rótulo que não corresponde à função do trecho | troque pelo rótulo correto ou retire |
| Termo técnico, sigla ou nome próprio sem definição no slide nem em slide anterior | sinalize |
| Hipóteses ou evidências indeterminadas ("sob certas hipóteses", "estudos mostram") | sinalize |
| Conclusão que não decorre dos itens exibidos | sinalize |
| Figura ou tabela sem linha de fonte visível | sinalize |

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
- Mantenha no slide toda atribuição visível (autor e ano, linha de fonte de figura ou tabela).
- Se uma nota combinar conteúdo repetitivo e uma fonte necessária, preserve a parte necessária.

## Relatório final

Entregue ao usuário, em lista curta:

- arquivo ou deck gravado;
- slides reorganizados, com uma linha sobre a mudança estrutural de cada um;
- blocos reordenados dentro de um slide, com a dependência restaurada;
- lacunas e inconsistências sinalizadas pela checagem, com o trecho literal;
- notas removidas;
- slides que não couberam e a divisão proposta;
- slides sem verificação visual, se houver.

## Critério de conclusão

Conclua somente quando:

- todo texto substantivo de corpo estiver no nível lógico adequado ou em um elemento próprio;
- o significado permanecer intacto e toda mudança de ordem dentro de um slide estiver no relatório;
- cada slide alterado tiver passado pela checagem de consistência, com as correções feitas e as sinalizações registradas;
- rótulos, conectivos e pontuação seguirem a seção correspondente;
- as fontes e notas remanescentes atenderem à política acima;
- todos os slides tiverem sido renderizados e inspecionados, ou os não verificados estiverem listados no relatório;
- não houver bullets unidos ao item-pai, hierarquia acidentalmente achatada, texto cortado ou elementos sobrepostos;
- o relatório final tiver sido entregue.
