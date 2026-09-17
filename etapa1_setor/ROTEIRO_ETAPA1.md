# ROTEIRO – ETAPA 1: ANÁLISE SETORIAL (NETFLIX), MÉTODO MARCELLUS

Versão 3 — reescrita em 16/09/2026, noite. As versões 1 (12/09) e 2 (16/09, tarde) estão no git.
Método adotado: ver `Marcellus.md`. Entrega: PDF ≤5 páginas, A4, Arial/Times 12, **18/09/2026 23h59**.

---

## ⚠️ 0. O que mudou na v3: sem Bloomberg Terminal

O grupo não tem acesso ao Terminal. A v2 apoiava três coisas nele: consenso numérico de analistas
(`BEst`), export de segmentos (`FA`) e estimativas de assinantes por player (Bloomberg Intelligence).
**Testei as alternativas públicas hoje à noite, antes de reescrever este plano** — o que segue é o que
de fato funcionou, não o que eu esperava que funcionasse.

**O que ficou igual ou melhor:** todo o financeiro das empresas sai da SEC, de graça e em formato
legível por máquina. Confirmei três rotas funcionando:

| Rota testada | Resultado |
|---|---|
| Carta 2T26 da Netflix (8-K, EDGAR) | ✅ Todos os números ✅ do pré-relatório conferidos contra a fonte primária: receita US$ 12.560 mi, lucro operacional US$ 4.193 mi, margem 33,4%, guidance 2026 de US$ 51,0–51,4 bi e 31,5%, razão conteúdo/amortização ~1,1x, FCF ~US$ 12,5 bi, recompra US$ 4,7 bi, 97 bi de horas (+2%), ao vivo "pouco mais de 5%" do gasto, ads ~US$ 3 bi |
| API XBRL da SEC (`data.sec.gov`) | ✅ Série histórica padronizada de qualquer empresa, sem parsing de HTML |
| R-files do EDGAR (`FilingSummary.xml` → `R50.htm`) | ✅ Tabela de segmentos já estruturada. Substitui o export `FA → Segments` do Bloomberg integralmente |

**A descoberta que muda o trabalho:** a Disney **não** reporta DTC como segmento com resultado
operacional próprio — o 10-K dá Entertainment / Sports / Experiences, e o número do Disney+ está em
tabela do MD&A. O mesmo vale em graus diferentes para Comcast (Peacock dentro de Media) e Paramount.
Ou seja, o G1 exige extração de MD&A empresa por empresa, não só da nota de segmentos. É a parte mais
custosa do que sobrou, e por isso ela entra primeiro no cronograma.

**O que foi perdido de verdade** está na seção 2.1 abaixo, com a compensação de cada item. Não vou
fingir que o substituto é equivalente: em dois casos ele é pior, e o relatório vai declarar isso.

---

## 1. A tese setorial que vamos defender (hipótese-guia)

> **O setor de vídeo tem dois andares, e só um deles dá lucro.**
> No andar da atenção, o vídeo premium perde participação para plataformas abertas: o streaming
> chegou a 48,5% do tempo de TV nos EUA (jun/26), mas a fatia da própria Netflix encolheu no
> período, e o YouTube é hoje o maior distribuidor de tempo de TV do país. No andar do lucro,
> ocorre o inverso: quinze anos de guerra por assinantes deixaram **um único player com margem
> operacional estruturalmente positiva** (31,5% projetada para 2026), enquanto os rivais
> consolidam por necessidade, os estúdios viraram fornecedores e as ligas e criadores capturam
> valor crescente. A pergunta da Etapa 1 não é "o setor cresce?" — é **"esse pool de lucro
> concentrado dura quanto tempo, e o que o quebraria?"**

Se os dados derrubarem essa hipótese, ela muda. Mas ter tese desde já é o que permite escrever
em 48h, e é o que a Marcellus faz: a carta começa com a conclusão e o resto é evidência.

---

## 2. O que EU faço sozinho (rotas verificadas hoje)

Tudo abaixo é público, alcançável por mim e com fonte citável. Vocês não precisam tocar em nada disto.

| Fonte | O que sai dela | Alimenta |
|---|---|---|
| **API XBRL da SEC** (`data.sec.gov/api/xbrl/`) | Receita, lucro operacional, ativos, capital investido — série anual e trimestral padronizada, de todas as 7 empresas | G1, ROIC da Seção 2 |
| **R-files do EDGAR** (`FilingSummary.xml` → `R*.htm`) | Notas de segmento e de fluxo de caixa já em tabela | G1, G4 |
| **MD&A dos 10-K/10-Q** | Receita e resultado do DTC de Disney, Peacock e Paramount — o que a nota de segmentos não dá | G1 |
| **Cartas trimestrais da Netflix** (ir.netflix.net) | Guidance, engajamento, ads, ao vivo, recompras. 2T26 já extraída integralmente | todas as seções |
| **EDGAR full-text search** (`efts.sec.gov`) | *Impairments* de acervo em WBD e Paramount: valor, data e a frase exata do filing | G4, Seção 3 |
| **Nielsen** (releases públicos do Gauge) | Tempo de TV por distribuidor nos EUA | G5 |
| **Wayback Machine** + centro de ajuda da Netflix | Histórico de mensalidade por país e plano, 2011–2026 | G3 |
| **FRED/BLS** e **IBGE/SIDRA** | CPI e IPCA para deflacionar | G3 |
| **WebSearch / imprensa setorial** | Variety, Deadline, Reuters, CNBC, Fortune, Bloomberg (notícias abertas) | Seção 4a, consenso narrativo |
| **EDGAR: proxies e DFAN14A da WBD** | Termos do deal: valor, escopo, break fee, ticking fee | Seção 4a |
| **AVMSD, European Audiovisual Observatory, Ancine** | Cotas e obrigações de investimento | Seção 5 |

### 2.1. O que o Bloomberg dava e ninguém mais dá — e o que fazemos no lugar

Quatro perdas reais. Em ordem de gravidade:

**(1) Consenso numérico de analistas para 2027–2028.** Era o item nº 1 da lista anterior, porque
"divergir do consenso" é exigência das orientações do Opportunity.
→ **Compensação:** trocamos divergência *numérica* por divergência *de narrativa*. O consenso
publicado é citável em texto — "a guerra do streaming terminou e a Netflix ganhou" aparece em
dezenas de matérias de 2026, com autor e data. Divergimos disso, não de uma projeção de EBIT.
Para 2026 temos o guidance da própria empresa, que é fonte primária e mais forte que consenso.
**Custo real:** perdemos a frase "o mercado projeta X para 2028, nós projetamos Y". Na Etapa 1, que é
setorial e não de valuation, isso dói pouco. Na Etapa 2 vai doer — resolver até outubro.

**(2) Estimativas de assinantes por player (Ampere/Omdia via BI).** Sem isso, o **G2 original**
(gasto em conteúdo ÷ assinantes) é impossível: a Netflix parou de divulgar assinantes.
→ **Compensação: mudar a métrica do gráfico**, não estimar assinante no chute. Ver G2 revisado na
seção 4. Gasto em conteúdo **por dólar de receita** prova a mesma economia de escala e é 100%
auditável a partir dos filings. **É um substituto honesto, não um inferior.**

**(3) Função `WACC`.** O teste de Greenwald pedia ROCE > WACC persistente.
→ **Compensação:** calculo ROIC dos filings e comparo com um custo de capital **declarado como
premissa nossa** (ordem de 9%). Na prática o argumento não precisa de precisão: se a Netflix roda ROIC
de dezenas de por cento e os rivais rodam perto de zero ou negativo, a conclusão não depende do
segundo decimal do WACC. **Perda pequena.**

**(4) Base rate de mídia 1995–2015 (Seção 6).** O XBRL da SEC só é confiável de ~2009 em diante.
→ **Compensação:** a Seção 6 passa a usar 3–4 casos com âncoras datadas e citadas (ESPN no pico de
assinantes vs. hoje, TV a cabo, Blockbuster) em vez de uma série calculada de retorno excedente.
**É a maior perda de rigor do relatório inteiro.** Mitigação: a Seção 6 tem 0,3 página e é a síntese —
ela pode viver de âncoras bem escolhidas. Mas não vamos escrever "N anos" com falsa precisão.

---

## 3. O que preciso de VOCÊS — agora são 3 itens, e nenhum é dado

Boa notícia da mudança de plano: **a lista para vocês encurtou.** Como não há Terminal para operar,
sobra só o que é julgamento de vocês — que é justamente o que eu não posso substituir.

| # | O quê | Por que é insubstituível | Prazo |
|---|---|---|---|
| **1** | **Decisão sobre as 7 bifurcações da seção 5** | É julgamento, não dado. Sem isso eu escrevo um relatório em cima do muro, que é o que mais reprova em "persuasão" e "coerência" | hoje, 16/09 |
| **2** | **Nome do grupo, integrantes e idioma** (PT ou EN) | Vai na capa e consome página. Recomendo **PT**: banca brasileira, Etapa 4 no Rio | hoje, 16/09 |
| **3** | **Trechos das cartas da Marcellus** colados em `Marcellus.md` seção 6 | Para eu imitar o método real e não a minha memória dele | hoje, 16/09 |

**Item opcional de alto retorno**, se sobrar tempo de alguém: **histórico de mensalidade da Netflix no
Brasil por plano, com datas**. O site brasileiro e a imprensa local são mais fáceis de garimpar em
português do que via Wayback em inglês, e isso alimenta o G3 — que na v3 passou a ser o gráfico mais
importante do relatório (ver seção 4). Se ninguém puder, eu faço via Wayback, só demora mais.

**O que não peço mais:** relatório sell-side pago. Sem conta em corretora e sem Terminal, a chance de
conseguir em 36h é baixa o suficiente para não valer o custo de oportunidade. Assumimos a perda (1)
da seção 2.1 e seguimos.

---

## 4. Estrutura do relatório (5 páginas) e os gráficos revisados

A arquitetura das seções **não mudou** — a tese sobrevive intacta à perda do Bloomberg, porque ela
sempre se apoiou em filings e não em consenso. Mudou a prioridade dos gráficos.

| # | Seção | Pág. | Argumento em uma frase | Gráfico |
|---|---|---|---|---|
| — | **Abertura** | 0,3 | O streaming venceu a TV linear, mas a Netflix não venceu o streaming — e ainda assim é a única que lucra | — |
| 1 | **Onde está o pool de lucro** | 1,0 | Mapeamos a cadeia por margem, não por receita | G1 |
| 2 | **Por que ele fica lá: a barreira não-óbvia** | 1,1 | Custo fixo de conteúdo diluído por uma base que ninguém mais tem, e o poder de compra sobre criadores que decorre disso | G2 + G3 |
| 3 | **O lucro do setor é caixa?** | 0,7 | **Seção original.** Lucro contábil aqui é escolha de política de amortização | G4 |
| 4 | **O que quebraria isso: as duas frentes** | 1,2 | (a) teto regulatório à consolidação; (b) erosão pela fronteira da atenção | G5 |
| 5 | **Regulação e fornecedores** | 0,4 | A regulação não limita preço — limita consolidação e transfere valor a quem produz | — |
| 6 | **Síntese: quanto tempo dura** | 0,3 | Âncoras históricas de mídia + as 3 perguntas da Etapa 2 | — |

### Os gráficos, em nova ordem de prioridade

**G3 — Mensalidade deflacionada, EUA e Brasil, 2011–2026. → PROMOVIDO A GRÁFICO PRINCIPAL.**
É 100% construível com o que eu alcanço (Wayback + CPI/IPCA), não dependia de Bloomberg em nada, e é
**exatamente o exemplo que as orientações do Opportunity citam** ("mostrar que foi capaz de recompor
preços em termos reais"). Com a perda do consenso, é ele que carrega a prova quantitativa de
*pricing power*. Era o 3º da lista; agora é o 1º.

**G4 — Caixa de conteúdo ÷ amortização, Netflix vs. pares, com impairments marcados.**
Sai inteiro do fluxo de caixa dos filings. É a seção que nenhum concorrente do desafio vai escrever.
Prioridade 2.

**G1 — Margem operacional por elo da cadeia, 2022–2026E.**
Netflix vs. DTC de Disney/WBD/Paramount/Peacock vs. estúdios vs. Roku (CTV) vs. YouTube.
**Mudança de escopo: 2022–2026, não 2019–2026.** Motivo analítico, não de preguiça — a WBD só existe
a partir de abr/2022 (fusão Warner+Discovery) e a Paramount Skydance a partir de ago/2025; série que
começa em 2019 mistura entidades diferentes e é atacável. Prioridade 3 porque é a extração mais cara
(MD&A empresa por empresa).

**G2 — REVISADO: gasto em conteúdo (caixa, US$ bi) e gasto em conteúdo ÷ receita, por player.**
A versão antiga (÷ assinantes) morreu com a perda das estimativas de Ampere/Omdia. A nova prova a
mesma coisa — que o líder compra conteúdo numa escala que os rivais não alcançam e ainda assim gasta
menos por dólar de receita — e tem a vantagem de ser auditável linha por linha nos filings.
Prioridade 4 (mesma passada de extração do G4).

**G5 — Nielsen Gauge: tempo de TV nos EUA por distribuidor.**
Prioridade 5, e é o mais frágil: o conflito metodológico do §7.1 continua aberto. **Se até 17/09 à
noite eu não tiver uma série coerente, ele sai e o argumento fica em texto com o número datado.**

Máximo 5 gráficos, meia coluna cada. Referências em notas de rodapé compactas. Texto em fonte 12.

---

## 5. As 7 bifurcações argumentativas — decisão de vocês

Cada uma tem duas leituras defensáveis com os mesmos dados. **Escolher é obrigatório**: um relatório
que fica nos dois lados perde em "persuasão" e "coerência", dois dos quatro critérios do edital.
Marquei minha recomendação, mas a decisão é do grupo.

### Bifurcação 1 — Qual é o mercado relevante?
- **(A) SVOD premium global** (Netflix, Disney+, Prime Video, HBO Max, Paramount+, Apple TV+). Estreito. Leva a: oligopólio endurecendo, Netflix líder folgada, fosso profundo.
- **(B) Mercado de atenção**: todo vídeo em tela, incluindo YouTube, TikTok e games. Leva a: mercado fragmentando, Netflix com ~8% do tempo de TV, papel de nicho premium.
- **(C) Bolso do consumidor + pool de publicidade em vídeo** (~US$ 650 bi endereçáveis pela própria narrativa da Netflix). Leva a: pista longa de crescimento, share baixo.
- ➡️ **Minha recomendação: definir pelo pool de LUCRO, não pelo de atenção nem pelo de receita.** É a
  jogada Marcellus e é original: "o mercado de atenção é enorme e não tem dono; o mercado de lucro do
  vídeo premium é pequeno e tem um dono só". Usa-se (B) como teste de realidade competitiva dentro
  da seção 4. **Risco:** o avaliador pode ler como estreitamento conveniente do mercado — por isso
  a definição precisa ser declarada e justificada no primeiro parágrafo, não escondida.

### Bifurcação 2 — A estrutura está endurecendo ou ainda é contestável?
- **(A) Endurecendo:** consolidação (Paramount+WBD), saída de subescala, disciplina de preço generalizada, bundles. Fosso setorial crescente.
- **(B) Não:** a participação da Netflix no tempo de TV **caiu** (~9,0% no 1T26 → 7,9% em jun/26 — *confirmar metodologia, ver §7*); o YouTube cresce; Amazon, Apple e Google são concorrentes financeiramente indiferentes ao P&L de streaming e por isso nunca saem. Pelo teste de Greenwald, participação instável = não há fosso setorial.
- ➡️ **Minha recomendação: os dois andares (tese da seção 1).** Endurecendo no vídeo premium,
  contestado na atenção. É a única leitura que reconcilia os dados sem escolher os que convêm, e
  é mais difícil de atacar numa arguição. **Risco:** exige escrita precisa para não soar ambígua —
  a frase de fechamento de cada seção resolve isso.

### Bifurcação 3 — O lucro reportado do setor é real?
- **(A) É:** razão caixa de conteúdo / amortização da Netflix ~1,1x em 2026E, FCF projetado ~US$ 12,5 bi, US$ 4,7 bi de recompra só no 2T26. Lucro vira caixa.
- **(B) Cuidado:** razão >1,0 significa que a empresa gasta mais caixa do que reconhece como despesa; o ativo de conteúdo continua crescendo e a DRE subestima o custo de reposição. Nos rivais, a prova está nos *impairments* bilionários de acervo.
- ➡️ **Minha recomendação: usar as duas — é a seção de qualidade contábil.** Netflix passa no teste,
  o setor em geral não. Isso é o filtro 1 da Marcellus aplicado a um setor inteiro e **nenhum
  concorrente do desafio vai escrever essa seção**. **Risco:** é a seção mais técnica; se mal escrita,
  vira jargão. Tem de caber em 0,7 página com um gráfico e uma conclusão em linguagem simples.

### Bifurcação 4 — Esporte ao vivo: barreira nova ou transferência de valor?
- **(A) Barreira:** é o último conteúdo não replicável. Dados da própria Netflix: ao vivo será ~5% do gasto em conteúdo em 2026 e só ~1% das horas vistas, **mas respondeu por 6 dos 10 maiores dias de adesão dos últimos 5 anos**. Aquisição de cliente baratíssima.
- **(B) Armadilha:** direitos esportivos historicamente transferem margem do distribuidor para a liga, que é monopólio natural. Foi o que corroeu a TV a cabo e a ESPN. Quem persegue esporte entrega o lucro ao fornecedor.
- ➡️ **Minha recomendação: (A) com a ressalva de (B) explicitada.** O par 5%-do-gasto / 6-dos-10-dias
  é um dos números mais fortes do relatório inteiro e é pouco citado. Mas o argumento só fica
  Marcellus se dissermos qual seria o sinal de que virou (B): renovações a múltiplos crescentes sem
  ganho proporcional de adesão.

### Bifurcação 5 — Publicidade: segundo motor ou diluição?
- **(A) Motor:** ~US$ 3 bi em 2026, praticamente dobrando; verba migrando de TV linear para CTV; inventário premium e ferramentas de ads próprias.
- **(B) Diluição:** o plano com anúncios reduz o ARPU médio e joga a Netflix num mercado (publicidade digital em vídeo) onde Google, Amazon e Meta têm 20 anos de vantagem em adtech e dados. É entrar num setor em que ela **não** tem fosso.
- ➡️ **Minha recomendação: (B) como alerta setorial, (A) como fato.** Na Etapa 1 a publicidade
  interessa como *mudança de estrutura do setor* (o pool de receita do vídeo se funde ao pool de
  publicidade, e aí o concorrente passa a ser o YouTube em definitivo), não como linha de receita.
  Isso amarra a seção 4. O julgamento sobre ARPU fica para a Etapa 2.

### Bifurcação 6 — O que significa ter perdido a Warner Bros.?
- **(A) Bala desviada:** saiu com US$ 2,8 bi, evitou integrar ativo de cabo em declínio e um litígio antitruste. Disciplina de alocação de capital — o filtro 3 da Marcellus, com sinal positivo.
- **(B) Derrota estratégica:** a Netflix tentou comprar escala em propriedade intelectual e perdeu; o nº 2 agora é grande de verdade (HBO, DC, acervo Warner, CBS, Paramount+); a tentativa revela que a produção orgânica não era considerada suficiente.
- **(C) Teto regulatório revelado:** o DOJ investigou explicitamente poder de mercado **sobre criadores**. Ou seja, a Netflix está proibida de consolidar — o setor vai se consolidar **ao redor dela**, não através dela.
- ➡️ **Minha recomendação: (C) como argumento principal, (A) como nota de alocação de capital.**
  (C) é o insight mais original disponível e ainda não tem consenso de mercado formado. E tem um
  efeito bonito: a acusação do DOJ é, na prática, **a validação do fosso feita por um terceiro
  hostil**. **Risco:** depende de fatos ainda em movimento — o fechamento Paramount–WBD pode sair
  entre agora e dezembro. Por isso todo parágrafo sobre isso leva data explícita.

### Bifurcação 7 — Brasil/LATAM: pista de crescimento ou ARPU estruturalmente baixo?
- **(A) Subpenetrado, cresce**, receita LATAM ultrapassou US$ 1,5 bi/trimestre no 2T26.
- **(B) ARPU baixo e exposto a câmbio**, alta sensibilidade a preço, concorrência local (Globoplay), pirataria. Crescimento futuro vem de **preço em mercado maduro**, não de penetração em emergente.
- ➡️ **Minha recomendação: (B), com Brasil como estudo de caso de um parágrafo**, não como seção.
  A banca é brasileira e vai gostar do recorte local, mas o argumento honesto é que o lucro
  incremental do setor vem de preço nos mercados ricos. Dizer isso com dado é mais persuasivo do
  que puxar sardinha para o mercado local. **Risco:** contrariar a expectativa da banca — mitigado
  se o parágrafo mostrar que entendemos o mercado local em profundidade.

---

## 6. Cronograma revisado — 36 horas

Mais apertado que a v2 porque a extração que era export de Excel virou parsing de filing. Compensa
que não há dependência de terceiro: não espero nada de fora para começar.

| Quando | O quê | Quem |
|---|---|---|
| **16/09 noite** | Vocês: 3 itens da seção 3. Eu: pipeline de extração da SEC (XBRL + R-files) para as 7 empresas; G4 e G2 montados | ambos |
| **17/09 manhã** | Eu: MD&A das rivais para o G1; série de preços do G3 com CPI/IPCA; Nielsen para o G5 | eu |
| **17/09 tarde** | Eu: rascunho completo das 5 páginas. Vocês: revisar **argumento por argumento**, não estilo | ambos |
| **17/09 noite** | Gráficos finais; corte para 5 páginas; conferência de fonte e data de acesso item por item; leitura em voz alta | ambos |
| **18/09 manhã** | Formatação A4/Arial 12, PDF, conferência do limite de páginas | responsável pelo envio |
| **18/09 até 18h** | **Envio pela área logada.** Não usar as 6 horas finais de folga | responsável pelo envio |

**Regras de corte, em ordem de aplicação:**
1. Se faltar dado para um gráfico às 17/09 à noite, **o gráfico sai** e o argumento fica em texto com
   o número que já temos. Nunca atrasamos por gráfico.
2. Ordem de sacrifício se o tempo estourar: G5, depois G2, depois G1. **G3 e G4 não se sacrificam** —
   são os dois que sustentam a originalidade do relatório.
3. Nenhum número entra no PDF sem estar em `empresa/fontes.md` com data de acesso.

---

## 7. Fatos a confirmar antes de irem para o PDF

Marcados no pré-relatório com ⚠️. Nenhum entra no texto sem checagem:
1. Série do Nielsen Gauge — "The Gauge" e "Media Distributor Gauge" têm metodologias diferentes
   (a segunda consolida por distribuidor); os números de 9,0% e 7,9% podem não ser comparáveis.
   Há ainda indício de mudança/descontinuação do relatório em ago/2026. **Usar uma única série coerente.**
2. Status do fechamento Paramount–WBD na data do envio (18/09) — pode mudar até o último dia.
3. Se a narrativa do TAM de ~US$ 650 bi ainda consta das cartas recentes da Netflix ou foi abandonada.
4. Números de gasto em conteúdo dos rivais: usar caixa (fluxo de caixa) e não despesa da DRE, e dizer qual.
5. Tramitação da Condecine sobre streaming e da cota de conteúdo nacional no Brasil em set/2026.
6. **Consenso de analistas:** não temos fonte numérica auditável. Onde o texto disser "o mercado
   espera", a frase tem de vir com citação de matéria datada e autor, **nunca** como número de
   consenso genérico. Sem Bloomberg, inventar precisão aqui é o risco mais fácil de ser pego.
7. **Margem do DTC das rivais:** confirmar, para cada empresa, se o número usado é resultado
   operacional de segmento reportado ou linha de MD&A — e dizer qual no rodapé do G1. Disney, Comcast
   e Paramount divulgam em níveis diferentes, e comparar coisas diferentes derruba o gráfico.

---

## 8. Armadilhas (mantidas da v1, ainda válidas)

- Tratar a Netflix como empresa "de tecnologia". É mídia com distribuição digital; o comparável é estúdio e TV.
- Ignorar o YouTube. Nos EUA ele tem mais tempo de TV do que a Netflix; omitir derruba a credibilidade.
- Usar assinantes como métrica central. A Netflix parou de divulgar e migrou o discurso para receita,
  margem e engajamento — e em 2027 reduz até a divulgação de horas vistas. O relatório tem de refletir isso.
- Descrever sem concluir. Toda seção fecha com "isso implica que…".
- Fonte sem data de acesso.
- Contato com RI da Netflix: proibido (3.2.2). Só nas reuniões coletivas do Opportunity.
