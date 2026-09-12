# ROTEIRO – Desafio Opportunity 2026

Status: rascunho para validação. Nada abaixo foi executado ainda.
Fonte: `contexto.md` (regulamento oficial + orientações do Opportunity).
Data de referência: 12/09/2026.

---

## 0. Lacunas a preencher antes de começar

| Item | Por que importa | Quem responde |
|---|---|---|
| Nome da empresa escolhida (ticker) | **Netflix (NASDAQ: NFLX)** – definido em 12/09 | ✔ |
| Integrantes do grupo (2 ou 3) e nome do grupo | Divisão de tarefas, assinatura dos entregáveis | Leonardo |
| Idioma dos trabalhos (PT ou EN) | Regulamento permite ambos (3.2.3) | Leonardo |
| Data das reuniões coletivas de Q&A com a empresa | Única via permitida de contato (3.2.2) | Site do desafio |

---

## 1. Calendário e entregáveis (fixos pelo regulamento)

| Etapa | Prazo | Entregável | Limite | Caráter |
|---|---|---|---|---|
| 1 | 18/09/2026 23h59 | Análise setorial (PDF) | 5 páginas | Eliminatório |
| 2 | 23/10/2026 23h59 | Tese de investimento (PDF) + apresentação (PDF) | 10 páginas + 10 slides | Eliminatório |
| 3 | 07/12/2026 23h59 | Apresentação final, com mentoria do Opportunity | 15 slides | Preparatório |
| 4 | 09/12/2026 | Defesa oral para a banca (preferencialmente presencial, RJ) | – | Classificatório |

Formato obrigatório dos escritos: A4, Arial ou Times New Roman 12, PDF, anexos não avaliados.
Critérios além do técnico: coerência, concisão, persuasão, originalidade/criatividade.
Toda informação usada precisa ter fonte citada (1.8). Contato direto com RI/executivos é proibido (3.2.2).

**Prazo crítico: a Etapa 1 vence em 6 dias.** O roteiro abaixo prioriza ela.

---

## 2. Estrutura de arquivos do projeto (a ser criada)

```
Oppotunity/
├── contexto.md              # fonte original (não editar)
├── ROTEIRO.md               # este arquivo
├── CONTEXTO_IA.md           # referência condensada para IA (fase A)
├── empresa/                 # dados da empresa escolhida
│   ├── perfil.md            # ticker, setor, resumo, pessoas-chave
│   └── fontes.md            # lista de fontes com links e data de acesso
├── etapa1_setor/
│   ├── pesquisa/            # notas brutas por tema do checklist I
│   ├── dados/               # planilhas/CSVs usados em gráficos
│   ├── rascunho.md          # texto em construção
│   └── entrega/             # PDF final
├── etapa2_tese/
│   ├── pesquisa/            # checklist II a V
│   ├── modelo/              # valuation (DCF, múltiplos)
│   ├── rascunho.md
│   └── entrega/             # PDF do texto + PDF dos slides
└── etapa3_4_final/
    └── apresentacao/        # 15 slides + roteiro de fala
```

---

## 3. Fases de trabalho

### Fase A – Base de referência (hoje)
Objetivo: transformar `contexto.md` em `CONTEXTO_IA.md`, otimizado para leitura por IA.

Conteúdo previsto do `CONTEXTO_IA.md`:
1. Resumo do desafio em 5 linhas.
2. Tabela de prazos e limites (a mesma da seção 1).
3. Regras que geram eliminação (lista curta, verificável).
4. Critérios de avaliação.
5. Checklist das 5 seções (I a V) reescrito como perguntas numeradas, sem prosa.
6. Diretrizes de qualidade do Opportunity: qualitativo com respaldo quantitativo, holístico, não "check the checklist", pensar o futuro a partir do histórico.
7. Campo "Empresa escolhida" e "Grupo" a preencher.

Fora do arquivo: cláusulas de imagem, LGPD, inscrição (já passaram ou não afetam a produção).

Entregável: `CONTEXTO_IA.md` revisado por você.

### Fase B – Etapa 1: análise setorial (12/09 a 18/09)
Objetivo: 5 páginas respondendo o checklist I com dados e fontes.

| Dia | Atividade |
|---|---|
| D0 (12/09) | Definir empresa, delimitar mercado relevante, listar fontes primárias (CVM, RI, relatórios setoriais, associações, IBGE/BCB) |
| D1–D2 | Pesquisa: tamanho e crescimento do mercado (TAM), estrutura competitiva, players, barreiras, penetração |
| D2–D3 | Pesquisa: cadeia de valor (quem captura lucro), perfil do consumidor, substitutos, regulação |
| D3 | Escolher 3 a 5 gráficos que sustentem os argumentos centrais; montar dados |
| D4 | Redação do rascunho completo (estrutura abaixo) |
| D5 | Revisão: corte para 5 páginas, coerência, fontes, formato A4/fonte 12 |
| D6 (18/09) | PDF final, conferência do formato, envio pela área logada |

Estrutura proposta do texto (5 páginas):
1. Mercado relevante e tamanho (0,75 pág.)
2. Dinâmica de crescimento e drivers (0,75 pág.)
3. Estrutura competitiva e barreiras (1,25 pág.)
4. Cadeia de valor e captura de lucro (1 pág.)
5. Regulação e impacto na oferta/preço (0,5 pág.)
6. Síntese: o que o setor implica para a empresa (0,75 pág.) – ponte para a Etapa 2

Entregável: `etapa1_setor/entrega/etapa1.pdf`.

### Fase C – Etapa 2: tese de investimento (19/09 a 23/10)
Objetivo: 10 páginas + 10 slides respondendo "Você seria sócio da empresa? Por quê?" com posição de compra, venda ou neutro.

Blocos de trabalho:
1. Modelo de negócios e governança (checklist II): unit economics, custos, vantagem competitiva, KPIs, estratégia, sócios e pessoas-chave.
2. Histórico financeiro: 5 a 10 anos de DRE, balanço, fluxo de caixa; montagem da base de dados.
3. Valuation (checklist V): DCF com premissas explícitas, múltiplos vs. comparáveis, cenários (base, otimista, pessimista), margem de segurança, perda estimada se a tese falhar.
4. Tese (checklist III): 3 a 4 pilares, cada um com evidência quantitativa; divergência explícita em relação ao consenso.
5. Riscos (checklist IV): riscos à tese e perguntas sem resposta com dados públicos.
6. Redação do texto de 10 páginas e dos 10 slides; slides devem ser autoexplicativos e persuasivos, não cópia do texto.
7. Participação nas reuniões coletivas de Q&A e incorporação do que for dito.

Entregáveis: `etapa2_tese/entrega/etapa2_texto.pdf` e `etapa2_tese/entrega/etapa2_slides.pdf`.

### Fase D – Etapas 3 e 4: apresentação final (24/10 a 09/12)
Condicionada à classificação.
1. Expandir para 15 slides incorporando feedback da mentoria.
2. Roteiro de fala com tempo por slide.
3. Banco de perguntas prováveis da banca e respostas preparadas.
4. Ensaios cronometrados.

---

## 4. Princípios de trabalho (extraídos das orientações)

- Cada argumento qualitativo vem acompanhado de um número que o sustente.
- O texto é holístico: cada seção alimenta a hipótese de investimento final.
- Não descrever o checklist item a item; usar o histórico para pensar o futuro.
- Toda afirmação factual tem fonte rastreável em `empresa/fontes.md`.
- Concisão é critério de avaliação: limite de páginas é teto, não meta.

---

## 5. Próximos passos imediatos

1. Você informa grupo e idioma. Empresa: Netflix. Roteiro detalhado da Etapa 1 em `etapa1_setor/ROTEIRO_ETAPA1.md`.
2. Eu crio `CONTEXTO_IA.md` (Fase A).
3. Iniciamos a Fase B pelo D0: delimitação do mercado relevante e lista de fontes.
