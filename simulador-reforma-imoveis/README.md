# Simulador da Reforma Tributária — Incorporação Imobiliária (v4)

Modelo em Excel para medir o impacto do IBS/CBS (LC 214/2025) num empreendimento de incorporação,
partindo da viabilidade econômica do projeto: VGV, permuta, cronograma de recebimentos, custo de obra e despesas.

## Estrutura

| Aba | Conteúdo |
|---|---|
| Resumo Executivo | Painel do cenário ativo, comparação de cenários e checks de integridade |
| Premissas & Cenários | Entradas editáveis, cenários (otimista, base, pessimista) e premissas da v4 |
| Fluxo_Incorporacao | Cronograma mensal de 60 meses: recebimentos, débito, créditos e saldo credor |
| DRE Empreendimento | DRE por cenário, DRE anualizada e visão societária da permuta (OCPC 01) |
| IRPJ_CSLL Trimestral | Lucro Presumido por trimestre, com a majoração da LC 224/2025 |
| Comparativo RET | Regime regular × RET de transição (art. 485) |
| Transição Tributária | Alíquotas de 2026 a 2033 e fator de crédito por ano |
| Cadastro Unidades / Créditos & RAJ | Base unitária e registro documental de créditos e RAJ |
| Matriz Normativa & Governança | Dispositivos, fontes e o controle que libera ou bloqueia o uso |

## O que mudou na v4

- **Crédito de obra por composição do custo:** materiais à alíquota padrão e serviços de construção e mão de obra
  terceirizados com a redução de 50% do art. 261, ponderando fornecedores do Simples. Folha própria de obra, se houver, não gera crédito.
- **Cenários no mesmo modo de cálculo:** as colunas Otimista, Base e Pessimista seguem o modo selecionado
  (plena ou transição), e a coluna Ativo sempre bate com o cenário escolhido.
- **Crédito de despesas por categoria:** alíquota do fornecedor × parcela da base com crédito.
- **Tributo embutido nos valores:** débito e créditos calculados por fora, `a ÷ (1 + a)`.
- **Transição completa e como modo padrão:** 2026 com PIS/Cofins e ano-teste dispensado, CBS a partir de 2027 e IBS gradual até 2033.
- **IRPJ/CSLL trimestral com a LC 224/2025**, com parâmetro para desligar (há liminares suspendendo a majoração).
- **Comparativo com o RET de transição (art. 485):** 4% da receita recebida, sem créditos, para opção feita antes de 01/01/2029.
- **Visão societária da permuta física** na DRE (OCPC 01).

## Leitura do cenário pessimista (premissas ilustrativas)

| | v3 | v4 (alíquota plena) |
|---|---|---|
| Débito IBS + CBS | R$ 27,7 mi | R$ 24,4 mi |
| Créditos (obra + despesas) | R$ 22,7 mi | R$ 13,3 mi |
| Imposto líquido | R$ 5,0 mi | R$ 11,1 mi |

No modo transição, o mesmo projeto recolhe R$ 14,8 mi no regime regular contra R$ 9,9 mi no RET.

As conclusões completas (RET × regime regular e CBS × PIS/Cofins) estão em [CONCLUSOES.md](CONCLUSOES.md).

> Uso consultivo. Os dados são fictícios e as premissas (composição do custo, parcela com crédito, alíquota de referência)
> são ilustrativas. Não substitui apuração fiscal nem parecer.
