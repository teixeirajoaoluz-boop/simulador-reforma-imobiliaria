# Simulador da Reforma Tributária — Incorporação Imobiliária

Modelo em Excel que mede o impacto do IBS e da CBS (LC 214/2025) num empreendimento de incorporação imobiliária,
a partir da viabilidade econômica do projeto: VGV, permuta de terreno, cronograma de recebimentos, custo de obra e despesas.

Ele responde às duas perguntas que uma incorporadora faz hoje:

1. **Quanto o projeto vai pagar de IBS/CBS**, ano a ano, durante a transição de 2026 a 2033?
2. **Vale mais a pena o regime regular ou o RET de transição (art. 485)?**

📄 **Conclusões do caso analisado:** [CONCLUSOES.md](CONCLUSOES.md)

## Principais resultados (caso ilustrativo, VGV de R$ 280 mi)

| | Regime regular | RET de transição |
|---|---|---|
| Tributos no ciclo, cenário pessimista | R$ 14,8 mi | **R$ 9,9 mi** |
| Tributos no ciclo, cenário base | R$ 12,0 mi | **R$ 9,9 mi** |
| Tributos no ciclo, cenário otimista | R$ 10,0 mi | R$ 9,9 mi |

- O RET tem a menor carga, mas cerca de **70% da vantagem vem do IRPJ/CSLL**, não do IBS/CBS.
- **A CBS sai mais barata que o PIS/Cofins atual** em todos os cenários. O aumento de carga, quando ocorre, vem do IBS,
  que é um tributo novo para a incorporadora.
- O fator que mais muda o resultado é a **participação de fornecedores do Simples Nacional** na cadeia da obra.

## Como usar

1. Abra `simulador_reforma_tributaria_imoveis_v4.xlsx` no Excel. As fórmulas são recalculadas ao abrir.
2. Preencha as células azuis da aba **Premissas & Cenários**.
3. Use os seletores:

| Seletor | Onde | Opções |
|---|---|---|
| Cenário | Premissas & Cenários, B6 | Otimista, Base, Pessimista |
| Modo de cálculo | Matriz Normativa & Governança, C8 | Transição temporal (padrão) ou Alíquota plena |
| Majoração da LC 224/2025 | Premissas & Cenários, B105 | Sim / Não |
| Interesse social (RET de 1%) | Premissas & Cenários, B111 | Sim / Não |

4. Confira o **Resumo Executivo**: o check de integridade precisa mostrar **OK**.

## Estrutura da planilha

| Aba | Conteúdo |
|---|---|
| Resumo Executivo | Painel do cenário ativo, comparação de cenários e check de integridade |
| Premissas & Cenários | Entradas, cenários, composição do custo de obra e crédito por categoria de despesa |
| Fluxo_Incorporacao | Cronograma mensal de 60 meses: recebimentos, débito, créditos e saldo credor |
| DRE Empreendimento | DRE por cenário, DRE anualizada e visão societária da permuta (OCPC 01) |
| IRPJ_CSLL Trimestral | Lucro Presumido por trimestre, com a majoração da LC 224/2025 |
| Comparativo RET | Regime regular × RET de transição, ano a ano e em valor presente |
| Transição Tributária | Alíquotas de CBS e IBS de 2026 a 2033 e fator de crédito por ano |
| Cadastro Unidades | Preço, permuta, redutor social e RAJ por unidade |
| Créditos & RAJ | Registro documental dos créditos e memória do RAJ |
| Matriz Normativa & Governança | Dispositivos legais, fontes e o controle que libera ou bloqueia o uso |

## O que o modelo considera

- **Regime específico de imóveis:** redução de 50% (art. 261), redutor de ajuste do terreno (RAJ) e redutor social por unidade.
- **Permuta física:** fora da base de IBS/CBS, que só incide sobre a torna (art. 252, §2º).
- **Regime de caixa:** o tributo incide a cada recebimento (art. 262).
- **Créditos:**
  - na obra, por composição do custo (materiais a 27% e serviços de construção a 13,5%), ponderados pela parcela do Simples;
  - nas despesas, por categoria.
- **Tributo embutido nos valores:** débito e créditos calculados por fora, `a ÷ (1 + a)`.
- **Transição:**
  - 2026: ano-teste dispensado e PIS/Cofins ainda devidos;
  - a partir de 2027: CBS;
  - de 2029 a 2033: IBS gradual.
- **Lucro Presumido trimestral** com a LC 224/2025 e **RET de transição** (4%, ou 1% para interesse social, sem créditos).
- **Provas de fechamento:** IVA, imposto pago, recebimentos e DRE precisam fechar em zero.

## Limitações

- A composição do custo, a parcela das despesas que gera crédito e a participação do Simples são premissas ilustrativas.
- A alíquota de referência da CBS (8,8%) é estimativa.
- A DRE anualizada reconhece a receita pelo recebimento, e não pelo avanço da obra (POC, CPC 47).
- Lucro Real e eventual repasse de preço pelos fornecedores não estão modelados.
- Os dispositivos legais estão marcados como pendentes de validação na matriz normativa.

## Autor

**João Teixeira**: contador (bacharel em Ciências Contábeis), com pós-graduação em Business Intelligence e Controladoria.

---

*Dados fictícios. Uso consultivo; não substitui apuração fiscal nem parecer tributário.*
