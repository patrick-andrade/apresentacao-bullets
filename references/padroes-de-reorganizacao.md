# Padrões de reorganização

Consulte estes exemplos para decidir agrupamento, nível e exceções. O objetivo é tornar explícita a função de cada trecho sem mudar o argumento.

## Padrão Quarto validado

Use um bullet-pai para o bloco lógico e quatro espaços para cada sub-bullet. Deixe uma linha em branco entre o pai e a sublista:

~~~markdown
- **Mecanismo:**

    - primeira etapa;
    - segunda etapa.

- **Resultado:** consequência observada.
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
- **Conceito:** a poluição é uma externalidade negativa.

- **Mecanismo:**

    - o custo privado não inclui todo o dano imposto à sociedade.

- **Resultado:** a produção de mercado fica acima do nível socialmente eficiente.
~~~

O conteúdo e a ordem foram preservados; os rótulos apenas revelam a função lógica.

## 2. Cadeia causal

Antes:

~~~markdown
A atividade gera um efeito sobre terceiros. Esse efeito não entra no preço. Os agentes tomam decisões com base em um custo incompleto. Surge uma diferença entre o resultado privado e o social.
~~~

Depois:

~~~markdown
- **Ponto de partida:** a atividade gera um efeito sobre terceiros.

- **Mecanismo:**

    - o efeito não entra no preço;
    - os agentes tomam decisões com base em um custo incompleto.

- **Implicação:** surge uma diferença entre o resultado privado e o social.
~~~

Quando a causalidade for o centro do slide, prefira blocos lógicos a uma sequência de frases independentes.

## 3. Premissas

Antes:

~~~markdown
Para que a negociação funcione, os direitos precisam estar definidos, os custos de transação devem ser baixos e as partes precisam conseguir negociar.
~~~

Depois:

~~~markdown
- **Premissas para a negociação:**

    - direitos bem definidos;
    - custos de transação baixos;
    - possibilidade efetiva de negociação entre as partes.
~~~

As premissas são pares no segundo nível. Não crie um terceiro nível para decompor frases curtas.

## 4. Exercício ou atividade

Antes:

~~~markdown
Considere o caso apresentado. Identifique quem gera e quem recebe a externalidade. Proponha um instrumento de política. Justifique a escolha. Tempo: 12 minutos.
~~~

Depois:

~~~markdown
- **Caso:** considere a situação apresentada.

- **Tarefa:**

    - identifique quem gera e quem recebe a externalidade;
    - proponha um instrumento de política;
    - justifique a escolha.

- **Tempo:** 12 minutos.
~~~

Preserve a sequência numerada somente se as etapas precisarem ser executadas em ordem ou se o número de respostas for parte da instrução.

## 5. Síntese e citação

Antes:

~~~markdown
Em síntese, alinhar o incentivo privado ao custo social altera a decisão na margem.

> Trecho citado mantido exatamente como no original.
~~~

Depois:

~~~markdown
- **Síntese:** alinhar o incentivo privado ao custo social altera a decisão na margem.

- **Formulação do autor:**

    > Trecho citado mantido exatamente como no original.
~~~

Mantenha a citação direta e sua fonte. O bullet organiza sua função no slide; não autoriza paráfrase nem supressão de rastreabilidade.

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
- **Composição:** o custo marginal social soma o custo marginal privado e o dano marginal.

$$
CMS(q) = CMP(q) + DM(q)
$$

- **Condição de eficiência:** no ótimo social, o benefício marginal é igual ao custo marginal social.
~~~

A equação continua em um bloco próprio. Organize apenas os parágrafos que a introduzem e interpretam.

## 7. Colunas, gráfico e texto

Preserve a estrutura de colunas e o bloco que produz o gráfico. Aplique a hierarquia somente à coluna textual:

~~~markdown
:::: {.columns}

::: {.column width="55%"}

```{r}
# código do gráfico preservado
```

:::

::: {.column width="45%"}

- **Leitura do gráfico:**

    - a curva privada representa o incentivo percebido pelo agente;
    - a curva social incorpora o efeito sobre terceiros.

- **Implicação:** a distância entre as curvas orienta o instrumento corretivo.

:::

::::
~~~

Não transforme legenda, eixo, fonte do gráfico ou código em bullet de conteúdo.

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
- **Alternativas de política:**

    - imposto;
    - regulação.

- **Critérios de decisão:**

    - informação disponível;
    - custos administrativos;
    - capacidade de monitoramento.
~~~

Reaproveite a hierarquia que já expressa corretamente a lógica. Ajuste apenas trechos planos, níveis inconsistentes ou agrupamentos sem função clara.

## 9. Sequência numerada

Ordem sem significado:

~~~markdown
1. Quem é afetado?
2. Qual é o mecanismo?
3. Qual instrumento pode responder?
~~~

Reorganização:

~~~markdown
- **Diagnóstico:**

    - quem é afetado;
    - qual é o mecanismo.

- **Decisão:** qual instrumento pode responder.
~~~

Ordem necessária:

~~~markdown
1. Calcule o custo marginal social.
2. Encontre a quantidade eficiente.
3. Compare-a com a quantidade de mercado.
~~~

No segundo caso, mantenha a numeração porque cada etapa depende da anterior.

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

Se uma nota contiver ambos os tipos, remova apenas a referência repetitiva e retenha a fonte necessária.

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

Aplique o critério de conclusão do [SKILL.md](../SKILL.md). Estes padrões só ilustram agrupamento e exceções; não substituem essa checagem.
