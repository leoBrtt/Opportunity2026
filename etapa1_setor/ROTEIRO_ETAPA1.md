# ROTEIRO – ETAPA 1: ANÁLISE SETORIAL (NETFLIX), MÉTODO MARCELLUS

Versão 2 — reescrita em 16/09/2026. A versão 1 (12/09) está no histórico do git.
Método adotado: ver `Marcellus.md`. Entrega: PDF ≤5 páginas, A4, Arial/Times 12, **18/09/2026 23h59**.

---

## ⚠️ 0. Duas coisas mudaram desde a versão 1

**(a) O prazo. Restam ~2,5 dias, não 6.** O cronograma antigo previa D4 = hoje com a pesquisa
toda pronta; as pastas `pesquisa/` e `dados/` estão vazias. O plano abaixo é de 48h, não de 6 dias.
Consequência prática: a lista de dados que peço a vocês caiu de 12 itens para **4**, e eu assumo
o resto. Não dá para esperar acesso de biblioteca ou relatório de corretora chegar a tempo.

**(b) A premissa central da versão 1 estava factualmente errada.** O roteiro antigo dizia
"Netflix anuncia compra da Warner Bros. (dez/2025)" e tratava a Netflix como consolidadora.
O que de fato aconteceu (verificado hoje, fontes em `empresa/fontes.md`):

| Data | Fato |
|---|---|
| 05/12/2025 | Conselho da WBD aceita proposta da Netflix (~US$ 83 bi) |
| 08/12/2025 | Paramount Skydance (David Ellison) lança oferta hostil, US$ 30/ação, tudo em dinheiro |
| 22/01/2026 | DOJ emite *second request* sobre Netflix–WBD; Netflix converte oferta para US$ 27,75 all-cash |
| fev/2026 | DOJ investiga se a Netflix exerce poder anticompetitivo **sobre criadores e produtores** (Clayton §7 / Sherman §2) |
| 27/02/2026 | **Netflix desiste e embolsa multa de rescisão de US$ 2,8 bi** |
| 23/04/2026 | Acionistas da WBD aprovam a Paramount (US$ 31/ação); taxa de rescisão regulatória de US$ 7 bi |
| set–dez/2026 | Fechamento esperado; *ticking fee* de US$ 0,25/ação por trimestre a partir de 30/09/2026 |

Isso não é um detalhe: **inverte o argumento**. A Netflix não é a consolidadora do setor — ela
tentou consolidar, foi barrada pelo preço e pelo antitruste, e o nº 2 do setor está sendo montado
por outro. E o motivo alegado pelo DOJ (poder de compra sobre criadores) é a confissão regulatória
de que o fosso da Netflix é real. Esse é o melhor material original que temos.

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

## 2. Os dados que EU busco sozinho (não gastem tempo com isso)

Já confirmei acesso e já puxei parte hoje. Tudo com fonte e data de acesso registradas.

- **SEC EDGAR**: 10-K/10-Q/8-K/proxies da Netflix, Disney, WBD, Paramount Skydance, Comcast, Roku, Alphabet.
- **Cartas trimestrais da Netflix** (ir.netflix.net) — consigo converter PDF em texto e extrair tabelas.
  Já extraí a do 2T26 (16/07/2026) integralmente.
- **Nielsen The Gauge** (releases públicos), notícias setoriais (Variety, Deadline, Reuters, CNBC, Bloomberg, Fortune).
- **Série histórica de preços** da Netflix por país e plano via Wayback Machine + centro de ajuda.
- **Deflatores**: CPI (FRED/BLS) e IPCA (IBGE/BCB).
- **Regulação**: textos da AVMSD, European Audiovisual Observatory, Ancine, Anatel, tramitação no Congresso.
- **Releases públicos** de Ampere, Omdia, Digital TV Research, Antenna, JustWatch, MUSO, Deloitte Digital Media Trends.
- **Todo o cálculo e os gráficos**: HHI, série de preço deflacionada, tabela de margem por elo da cadeia,
  ROCE, razão caixa de conteúdo / amortização, participação no tempo de TV.

## 3. Os dados que preciso de VOCÊS — só 4 itens

Prioridade absoluta, hoje (16/09) até o fim do dia. O resto eu abandono conscientemente.

| # | O quê | Por que é insubstituível | Prazo |
|---|---|---|---|
| **1** | **Decisão sobre as bifurcações da seção 5** (as 7 escolhas argumentativas) | É julgamento de vocês, não dado. Sem isso eu escrevo um relatório em cima do muro, que é o que mais reprova. | hoje, 16/09 |
| **2** | **Qualquer relatório sell-side ou setorial pago** que vocês consigam em horas (conta em corretora, professor, portal CAPES, biblioteca digital): Morgan Stanley / JPM / Goldman / MoffettNathanson sobre streaming; Ampere ou Omdia completos | É a única coisa que eu genuinamente não alcanço. Uma iniciação de cobertura vale por dez notícias e dá o *consenso* contra o qual vamos divergir. Se não vier até amanhã cedo, eu construo o consenso a partir de manchetes e sigo. | 17/09 manhã |
| **3** | **Trechos das cartas da Marcellus** que vocês analisaram, colados em `Marcellus.md` seção 6 | Para eu imitar o método real e não a minha memória dele. | hoje, 16/09 |
| **4** | **Nome do grupo, integrantes e idioma** (PT ou EN) | Vai na capa/cabeçalho e consome página. Recomendo **PT**: a banca é brasileira e a Etapa 4 é no Rio. | hoje, 16/09 |

**O que deliberadamente NÃO vamos buscar** (e por que está tudo bem): Kantar IBOPE, Comscore,
Antenna completo, Bloomberg/Economatica, PNAD TIC detalhada, Euromonitor. São ótimos para a Etapa 2.
Na Etapa 1, com 5 páginas, cada um desses acrescentaria uma linha e custaria meio dia.

**Se vocês tiverem tempo sobrando**, o item de maior retorno é montar a planilha de **histórico de
preços da Netflix no Brasil por plano com datas** (o site brasileiro e as notícias locais são mais
fáceis de garimpar em português). Eu cruzo com o IPCA e viro o gráfico de pricing power.

---

## 4. Estrutura do relatório (5 páginas) — arquitetura Marcellus

| # | Seção | Pág. | Argumento em uma frase | Gráfico |
|---|---|---|---|---|
| — | **Abertura** | 0,3 | Um número que contradiz o consenso: o streaming venceu a TV linear, mas a Netflix não venceu o streaming — e ainda assim é a única que lucra. | — |
| 1 | **Onde está o pool de lucro** | 1,0 | Mapeamos a cadeia por margem, não por receita: o lucro do vídeo premium global está concentrado em um player só. | G1 |
| 2 | **Por que ele fica lá: a barreira não-óbvia** | 1,1 | Teste de Greenwald (participação estável + ROCE>WACC persistente). A barreira não é catálogo nem tecnologia: é custo fixo de conteúdo diluído por uma base global que ninguém mais tem, e o poder de compra sobre criadores que decorre disso. | G2 + G3 |
| 3 | **O lucro do setor é caixa?** | 0,7 | **Seção original.** Neste setor, lucro contábil é escolha de política de amortização de conteúdo. Testamos quem converte. | G4 |
| 4 | **O que quebraria isso: as duas frentes** | 1,2 | (a) teto regulatório à consolidação, revelado pelo episódio WBD; (b) erosão por baixo, na fronteira da atenção (YouTube, criadores, engajamento quase estável). | G5 |
| 5 | **Regulação e fornecedores** | 0,4 | Aqui a regulação não limita preço — limita consolidação e transfere valor para ligas, sindicatos e cotas locais. | — |
| 6 | **Síntese: quanto tempo dura** | 0,3 | Base rate da mídia + as 3 perguntas que a Etapa 2 tem de responder. | — |

Referências em notas de rodapé compactas dentro do limite (anexos não são avaliados).
**Máximo 5 gráficos**, meia coluna cada. Texto obrigatoriamente fonte 12.

### Os gráficos (fecho a lista quando os dados estiverem prontos)
- **G1 – Margem operacional por elo da cadeia, 2019–2026E**: Netflix vs. DTC de Disney/WBD/Paramount/Peacock vs. estúdios vs. Roku (CTV) vs. Alphabet/YouTube. *Prova de onde fica o lucro.*
- **G2 – Gasto em conteúdo (US$ bi) ÷ base de assinantes**: custo de conteúdo por assinante por player. *Prova a economia de escala como barreira.*
- **G3 – Preço do plano padrão deflacionado**, EUA e Brasil, 2011–2026. *Prova quantitativa de pricing power — é exatamente o exemplo que o Opportunity cita nas orientações.*
- **G4 – Caixa gasto em conteúdo ÷ amortização de conteúdo**, Netflix vs. pares, com impairments dos rivais marcados. *A seção de qualidade contábil.*
- **G5 – Nielsen Gauge**: tempo de TV nos EUA por distribuidor, 2021–2026, YouTube vs. Netflix vs. broadcast vs. cabo. *A fronteira da atenção.*

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

## 6. Cronograma de 48 horas

| Quando | O quê | Quem |
|---|---|---|
| **16/09 tarde** | Vocês: decidir as 7 bifurcações, colar as cartas da Marcellus, definir grupo/idioma. Eu: puxar 10-K da Netflix e dos pares, Nielsen Gauge, série de preços, montar `empresa/fontes.md` | ambos |
| **16/09 noite** | Eu: montar as 5 bases de dados dos gráficos em `etapa1_setor/dados/` e as notas de pesquisa por seção | eu |
| **17/09 manhã** | Eu: rascunho completo das 5 páginas. Vocês: revisar argumento por argumento — não estilo, argumento | ambos |
| **17/09 tarde** | Gráficos finais; corte para 5 páginas; conferência de todas as fontes com data de acesso | ambos |
| **17/09 noite** | Leitura em voz alta (teste de coerência); versão candidata fechada | todos |
| **18/09 manhã** | Formatação A4/Arial 12, geração do PDF, conferência de limite de páginas | responsável pelo envio |
| **18/09 até 18h** | **Envio pela área logada.** Não usar as 6 horas finais de folga | responsável pelo envio |

Regra de corte: se às 17/09 à noite faltar dado para um gráfico, **o gráfico sai e o argumento fica
em texto com o número que já temos**. Não atrasamos por gráfico.

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

## 8. Armadilhas (mantidas da v1, ainda válidas)

- Tratar a Netflix como empresa "de tecnologia". É mídia com distribuição digital; o comparável é estúdio e TV.
- Ignorar o YouTube. Nos EUA ele tem mais tempo de TV do que a Netflix; omitir derruba a credibilidade.
- Usar assinantes como métrica central. A Netflix parou de divulgar e migrou o discurso para receita,
  margem e engajamento — e em 2027 reduz até a divulgação de horas vistas. O relatório tem de refletir isso.
- Descrever sem concluir. Toda seção fecha com "isso implica que…".
- Fonte sem data de acesso.
- Contato com RI da Netflix: proibido (3.2.2). Só nas reuniões coletivas do Opportunity.
