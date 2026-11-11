# Padrões de reorganização

Consulte estes exemplos para decidir agrupamento, nível, ligação e exceções. O objetivo é tornar explícita a função de cada trecho e a ligação entre eles sem mudar o argumento. Rótulos, conectivos e pontuação seguem a seção correspondente do [SKILL.md](../SKILL.md): rótulo de bloco sem dois-pontos, rótulo na linha com dois-pontos, conectivo para ligar os passos e itens sem pontuação final.

## Padrão Quarto validado

Use um bullet-pai para o bloco lógico e quatro espaços para cada sub-bullet. Deixe uma linha em branco entre o pai e a sublista:

~~~markdown
- Hipóteses

    - primeira hipótese
    - segunda hipótese

- Por isso, a consequência observada
~~~

A linha em branco e os quatro espaços impedem que a conversão para PowerPoint trate pai e filho como um único parágrafo. Use o marcador Markdown `-`; o caractere visual `•` pertence ao tema ou ao mecanismo nativo da apresentação.

## 1. Parágrafos planos

Antes:

~~~markdown
A poluição é uma externalidade negativa.

O custo privado não inclui todo o dano imposto à sociedade.

A produção de mercado fica acima do nível socialmente eficiente.
~~~

Depois:

~~~markdown
- A poluição é uma externalidade negativa

- O custo privado não inclui todo o dano imposto à sociedade

- Por isso, a produção de mercado fica acima do nível socialmente eficiente
~~~

O conteúdo e a ordem foram preservados. As três frases já formam um argumento e dispensam rótulos; o conectivo mostra que a terceira decorre da segunda.

## 2. Cadeia causal

Antes:

~~~markdown
A atividade gera um efeito sobre terceiros. Esse efeito não entra no preço. Os agentes tomam decisões com base em um custo incompleto. Surge uma diferença entre o resultado privado e o social.
~~~

Depois:

~~~markdown
- A atividade gera um efeito sobre terceiros

- Mecanismo

    1. o efeito não entra no preço
    2. por isso, os agentes decidem com base em um custo incompleto
    3. logo, o resultado privado difere do social
~~~

Quando a causalidade for o centro do slide, numere as etapas e ligue cada uma à anterior. O rótulo de bloco abre a sublista sem dois-pontos.

## 3. Premissas

Antes:

~~~markdown
Para que a negociação funcione, os direitos precisam estar definidos, os custos de transação devem ser baixos e as partes precisam conseguir negociar.
~~~

Depois:

~~~markdown
- Premissas para a negociação

    - direitos bem definidos
    - custos de transação baixos
    - possibilidade efetiva de negociação entre as partes
~~~

As premissas são pares no segundo nível. Não crie um terceiro nível para decompor frases curtas.

## 4. Exercício ou atividade

Antes:

~~~markdown
Considere o caso apresentado. Identifique quem gera e quem recebe a externalidade. Proponha um instrumento de política. Justifique a escolha. Tempo: 12 minutos.
~~~

Depois:

~~~markdown
- Caso: considere a situação apresentada

- Tarefa

    - identifique quem gera e quem recebe a externalidade
    - proponha um instrumento de política
    - justifique a escolha

- Tempo: 12 minutos
~~~

"Caso" e "Tempo" são rótulos na linha e levam dois-pontos; "Tarefa" abre sublista e não leva. Preserve a sequência numerada somente se as etapas precisarem ser executadas em ordem ou se o número de respostas for parte da instrução.

## 5. Síntese e citação

Antes:

~~~markdown
Em síntese, alinhar o incentivo privado ao custo social altera a decisão na margem.

> Trecho citado mantido exatamente como no original.
~~~

Depois:

~~~markdown
- Em síntese, alinhar o incentivo privado ao custo social altera a decisão na margem

- Formulação do autor

    > Trecho citado mantido exatamente como no original.
~~~

A frase já anuncia que é síntese e dispensa rótulo. Mantenha a citação direta, com sua pontuação, e sua fonte. O bullet organiza sua função no slide; não autoriza paráfrase nem supressão de rastreabilidade.

## 6. Fórmula

Antes:

~~~markdown
O custo marginal social soma o custo marginal privado e o dano marginal.

$$
CMS(q) = CMP(q) + DM(q)
$$

No ótimo social, o benefício marginal é igual ao custo marginal social.
~~~

Depois:

~~~markdown
- O custo marginal social soma o custo marginal privado e o dano marginal

$$
CMS(q) = CMP(q) + DM(q)
$$

- No ótimo social, o benefício marginal é igual ao custo marginal social
~~~

A equação continua em um bloco próprio. Organize apenas os parágrafos que a introduzem e interpretam.

## 7. Colunas, gráfico e texto

Preserve a estrutura de colunas e o bloco que produz o gráfico. Aplique a hierarquia somente à coluna textual:

~~~markdown
:::: {.columns}

::: {.column width="55%"}

```{r}
# código do gráfico preservado, com a linha de fonte na legenda
```

:::

::: {.column width="45%"}

- Leitura do gráfico

    - a curva privada representa o incentivo percebido pelo agente
    - a curva social incorpora o efeito sobre terceiros

- Por isso, a distância entre as curvas orienta o instrumento corretivo

:::

::::
~~~

Não transforme legenda, eixo, fonte do gráfico ou código em bullet de conteúdo. Se o gráfico não tiver linha de fonte visível, sinalize no relatório.

## 8. Hierarquia já parcial

Antes:

~~~markdown
- Instrumentos de política
    - imposto
    - regulação

A escolha depende de informação, custos administrativos e capacidade de monitoramento.
~~~

Depois:

~~~markdown
- Instrumentos de política

    - imposto
    - regulação

- Critérios de escolha

    - informação disponível
    - custos administrativos
    - capacidade de monitoramento
~~~

Reaproveite a hierarquia e os rótulos que já expressam corretamente a lógica. Ajuste apenas trechos planos, níveis inconsistentes, paralelismo, espaçamento de renderização ou agrupamentos sem função clara.

## 9. Sequência numerada

Ordem sem significado:

~~~markdown
1. Quem é afetado?
2. Qual é o mecanismo?
3. Qual instrumento pode responder?
~~~

Reorganização:

~~~markdown
- Diagnóstico

    - quem é afetado?
    - qual é o mecanismo?

- Decisão: qual instrumento pode responder?
~~~

Ordem necessária:

~~~markdown
1. Calcule o custo marginal social.
2. Encontre a quantidade eficiente.
3. Compare-a com a quantidade de mercado.
~~~

No segundo caso, mantenha a numeração porque cada etapa depende da anterior, e aplique a mesma regra de pontuação dos bullets:

~~~markdown
1. Calcule o custo marginal social
2. Encontre a quantidade eficiente
3. Compare-a com a quantidade de mercado
~~~

## 10. Notas

Nota repetitiva, removível somente após solicitação:

~~~markdown
::: notes
Stiglitz, capítulo 6, p. 143.
:::
~~~

Nota que deve permanecer:

~~~markdown
::: notes
Fonte dos dados: órgão oficial, série e data de atualização.
Imagem: autor, acervo ou licença do ativo externo.
:::
~~~

Se uma nota contiver ambos os tipos, remova apenas a referência repetitiva e retenha a fonte necessária. A regra de pontuação vale para bullets do slide, não para notas.

## 11. Resultado antes das premissas

Antes:

~~~markdown
- Resultado: a negociação entre as partes leva ao nível eficiente de poluição

- Mecanismo

    - quem valoriza mais o direito paga por ele
    - a poluição cai até o ponto em que reduzi-la custa mais do que o dano evitado

- Premissas

    - direitos bem definidos
    - custos de transação baixos
~~~

Depois:

~~~markdown
- Premissas

    - direitos bem definidos
    - custos de transação baixos

- Mecanismo

    1. quem valoriza mais o direito paga por ele
    2. por isso, a poluição cai até o ponto em que reduzi-la custa mais do que o dano evitado

- Com essas premissas, a negociação entre as partes leva ao nível eficiente de poluição
~~~

Todos os blocos já estavam no slide; só a ordem mudou, para que o resultado venha depois do que ele usa. Registre no relatório: "slide N: premissas e mecanismo movidos para antes do resultado".

## 12. Rótulo sem referente

Antes:

~~~markdown
- A política ambiental dispõe de instrumentos de preço e de quantidade

- O regulador raramente conhece o custo de reduzir a poluição

- Dois tipos

    - imposto sobre a emissão
    - teto de emissões com licenças negociáveis
~~~

Depois:

~~~markdown
- A política ambiental dispõe de instrumentos de preço e de quantidade

    - de preço: imposto sobre a emissão
    - de quantidade: teto de emissões com licenças negociáveis

- O regulador raramente conhece o custo de reduzir a poluição
~~~

"Dois tipos" estava longe do termo a que se referia. A sublista voltou para junto dele, e cada item ganhou o rótulo que o liga à frase-pai.

## 13. Lacuna que se sinaliza

~~~markdown
- Sob certas condições, a negociação privada resolve a externalidade

- Estudos mostram que isso é raro quando há muitos afetados
~~~

O slide não diz quais condições nem quais estudos, e essa informação não está em outro ponto do deck. Mantenha o texto e registre no relatório: "slide N: 'sob certas condições' não nomeia as condições; 'estudos mostram' não identifica o estudo nem a magnitude". Preencher a lacuna é decisão de conteúdo.

## Exceções

| Elemento | Tratamento |
|---|---|
| Título do slide | Preserve como título; não o converta em bullet. |
| Divisor de seção | Preserve o layout enxuto e a função de transição. |
| Tabela | Preserve a estrutura tabular; bullets podem introduzir ou interpretar a tabela. |
| Gráfico ou imagem | Preserve o objeto, legenda e fonte; bullets podem orientar a leitura. |
| Equação em destaque | Preserve o bloco matemático; bullets podem explicar variáveis e implicações. |
| Código | Preserve o bloco e sua sintaxe; bullets podem indicar objetivo ou saída. |
| Fonte ou nota necessária | Preserve em nota, rodapé ou campo de fonte conforme o template. |

## Auditoria final

Aplique a checagem de consistência e o critério de conclusão do [SKILL.md](../SKILL.md). Estes padrões só ilustram agrupamento, ligação e exceções; não substituem essa checagem.
