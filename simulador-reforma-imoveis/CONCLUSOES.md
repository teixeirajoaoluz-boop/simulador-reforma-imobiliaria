# Conclusões — Reforma Tributária na Incorporação Imobiliária

Análise feita com o simulador v4 (`simulador_reforma_tributaria_imoveis_v4.xlsx`) para uma SPE de incorporação residencial
no Lucro Presumido, com obra terceirizada e vendas de 2026 a 2030.

## Premissas do caso

| Item | Valor |
|---|---|
| VGV total / VGV tributável (sem permuta física) | R$ 280 mi / R$ 247 mi |
| Unidades | 100, sendo 12 em permuta física do terreno |
| Custo de obra | R$ 150 mi: 45% materiais e 55% serviços e mão de obra terceirizados |
| Despesas operacionais e de vendas | R$ 38 mi |
| Recebimentos | 12% na entrada, 43% em parcelas mensais e 45% nas chaves (mês 60) |
| Alíquota de referência IBS + CBS | 27% (CBS 8,8%), com redução de 50% para imóveis (art. 261) |
| RAJ do terreno por cenário | Otimista R$ 58 mi · Base R$ 45 mi · Pessimista R$ 33 mi |
| Fornecedores do Simples por cenário | Otimista 0% · Base 40% · Pessimista 80% |

Valores com tributo embutido; débito e créditos calculados por fora. Modo de cálculo: transição 2026-2033, salvo indicação.

---

## 1. Regime regular × RET de transição (art. 485)

### Resultado

Com essas premissas, **o RET de transição é a opção de menor carga**. No cenário pessimista:

| | Regime regular | RET | Diferença |
|---|---|---|---|
| Tributos sobre consumo (PIS/Cofins 2026 + IBS/CBS) | R$ 6,6 mi | R$ 5,1 mi | R$ 1,5 mi |
| IRPJ + CSLL | R$ 8,1 mi | R$ 4,7 mi | **R$ 3,4 mi** |
| **Total no ciclo** | **R$ 14,8 mi** | **R$ 9,9 mi** | **R$ 4,9 mi** |
| Total em valor presente (12% a.a.) | R$ 10,4 mi | R$ 7,0 mi | R$ 3,3 mi |

### A vantagem do RET vem principalmente do IRPJ/CSLL

- Cerca de **70% da diferença é imposto de renda**. No RET ele é 1,92% da receita recebida. No Lucro Presumido, com a majoração da LC 224/2025, passa de 3% da receita.
- No consumo, o regime específico de imóveis (RAJ, redutor social e redução de 50%) **chega perto do RET**. Dos R$ 1,5 mi de diferença, R$ 0,8 mi vêm de 2026, quando ainda vale o PIS/Cofins de 3,65% sobre a entrada de 12%. De 2027 a 2030 a diferença no IBS/CBS é de cerca de R$ 0,7 mi.

### O resultado depende das premissas de crédito

| Cenário | Regime regular | RET | Melhor opção |
|---|---|---|---|
| Otimista | R$ 10,0 mi | R$ 9,9 mi | Praticamente empate |
| Base | R$ 12,0 mi | R$ 9,9 mi | RET (R$ 2,2 mi) |
| Pessimista | R$ 14,8 mi | R$ 9,9 mi | RET (R$ 4,9 mi) |

O que decide são a participação de fornecedores do Simples e o valor do RAJ do terreno. No otimista, o IBS/CBS a pagar é zero e ainda sobra crédito acumulado.

### Onde a conclusão não se aplica

- **Projetos lançados a partir de 2029:** a opção pelo RET de transição precisa ser efetivada antes de 01/01/2029.
- **Loteamento, locação e empreitada:** o RET é exclusivo da incorporação com patrimônio de afetação.
- **Venda para empresa que toma crédito** (salas comerciais, galpões): no RET o comprador não aproveita crédito de IBS/CBS.
- **Lucro Real com margem baixa:** o IRPJ/CSLL passa a depender do lucro efetivo, e a comparação muda.
- **Custos do próprio RET:** patrimônio de afetação, contabilidade segregada e irreversibilidade da opção não estão no modelo.

### Conclusão

> Para incorporação residencial vendida a pessoa física, no Lucro Presumido e lançada até 2028, o RET de transição tende
> a ser a melhor opção, principalmente por causa do IRPJ/CSLL. No IBS/CBS, o regime específico com RAJ e redutor social
> chega perto do RET e pode empatar quando a cadeia de fornecedores gera muito crédito.

---

## 2. CBS × PIS/Cofins

### Resultado

**A CBS reduz a carga em relação ao PIS/Cofins em todos os cenários.**

| | Otimista | Base | Pessimista |
|---|---|---|---|
| **Hoje: PIS/Cofins cumulativo (Lucro Presumido, 3,65%)** | R$ 9,0 mi | R$ 9,0 mi | R$ 9,0 mi |
| Hoje: parcela de PIS/Cofins do RET (2,08%) | R$ 5,1 mi | R$ 5,1 mi | R$ 5,1 mi |
| **CBS líquida, alíquota plena (2033+)** | 0 (sobra R$ 2,1 mi de crédito) | R$ 0,8 mi | R$ 3,6 mi |
| CBS líquida na transição + PIS/Cofins de 2026 | R$ 0,5 mi | R$ 2,8 mi | R$ 5,1 mi |

### Por que a CBS sai mais barata

1. **Redução de 50%** na alíquota das operações com imóveis (art. 261).
2. **Base menor:** RAJ do terreno e redutor social de R$ 100 mil por unidade. O PIS/Cofins cumulativo incide sobre a receita inteira.
3. **Créditos:** o PIS/Cofins cumulativo não dá crédito. Na CBS, materiais e obra terceirizada geram crédito. É o efeito mais forte.

### Onde aparece o aumento: o IBS

O IBS substitui o ICMS e o ISS, que hoje **não incidem na venda de unidade própria**. Para a incorporadora, é um custo novo.
Somando todo o consumo com alíquota plena:

| | Otimista | Base | Pessimista |
|---|---|---|---|
| CBS + IBS líquidos | 0 (crédito acumulado) | R$ 2,4 mi (0,96%) | **R$ 11,1 mi (4,48%)** |
| PIS/Cofins atual (Presumido) | R$ 9,0 mi (3,65%) | R$ 9,0 mi (3,65%) | R$ 9,0 mi (3,65%) |

A carga sobre consumo **só aumenta no cenário pessimista com alíquota plena**, quando 80% dos fornecedores são do Simples.
Na transição, com o IBS ainda baixo, a carga cai em todos os cenários.

### Conclusão

> Neste projeto, a substituição do PIS/Cofins pela CBS reduz a carga. O risco está no IBS, que é novo para a incorporadora,
> e na qualidade da cadeia de fornecedores. A soma de IBS e CBS só supera o PIS/Cofins atual com fornecedores
> majoritariamente do Simples e com a alíquota plena.

---

## Ressalvas gerais

- **Custo de obra igual nos dois regimes:** o modelo não captura um eventual repasse de preço pelos fornecedores. Se eles
  baixarem os preços com o fim dos tributos cumulativos, o custo cai; se mantiverem, os créditos ajudam menos.
- **Crédito acumulado** só tem valor econômico se houver ressarcimento ou uso em outras operações.
- **Alíquota de referência da CBS (8,8%)** é estimativa; ainda não foi fixada oficialmente.
- **LC 224/2025** está sendo questionada judicialmente. Sem a majoração, o IRPJ/CSLL do regime regular cai cerca de
  R$ 0,6 mi, e o RET continua com menor carga.
- **Composição do custo, parcela de despesas com crédito e participação do Simples** são premissas ilustrativas e devem vir do orçamento real.
- Os dispositivos legais (LC 214/2025, arts. 252, 261, 262, 348 e 485; LC 224/2025; ADCT, art. 125) foram conferidos por
  fontes secundárias e estão marcados como pendentes de validação na aba Matriz Normativa & Governança.

*Dados fictícios. Uso consultivo; não substitui apuração fiscal nem parecer.*
