# Relatório de Análise de Saúde Financeira Highway

## 1. Visão Geral do Problema

Lorenzzo, como proprietário de quatro lojas da franquia Highway, você enfrenta o desafio de gerenciar elas. Atualmente, sua tomada de decisão muitas vezes é baseada na intuição, dessa, forma, pode gerar insights incertos sobre seus negócios.

Para resolver este problema, esta análise foca em responder a duas perguntas:
1.  **Como medir e comparar a saúde financeira das lojas de forma objetiva e consistente?**
2.  **Quais lojas precisam de atenção imediata e em quais áreas específicas elas precisam melhorar para o próximo mês?**

## 2. Fonte e Preparação dos Dados

Para realizar esta análise, utilizei cinco fontes de dados fornecidas, que cobrem o período de 01/01/2024 a 30/06/2025. Os arquivos utilizados foram:
* `receipts-000000000000.csv`: Dados de cupons fiscais.
* `items-000000000000.csv`: Produtos vendidos em cada cupom.
* `payments-000000000000.csv`: Métodos de pagamento.
* `discounts-000000000000.csv`: Descontos aplicados.
* `torque.csv`: Métrica de desempenho financeiro diário da franquia.

Os dados foram limpos, processados e agregados para uma melhor análise.

## 3. Construção do Índice de Saúde Financeira (ISF)

Para substituir a intuição, criei o **Índice de Saúde Financeira (ISF)**. Esta é uma métrica que pontua de 0 a 100 e que resume a performance de cada loja de forma diária. Ele é composto por três pilares:

* **Receita Líquida (`net_revenue`):** A métrica mais direta de **volume** de vendas. Representa o motor principal do negócio.
* **Torque (`net_torque`):** Um indicador referente a **eficiência** da venda. Um torque alto significa que a loja vende produtos conjuntos com valores mais altos, e não apenas produtos de baixa margem.
* **Percentual de Descontos (`discount_perc`):** Uma métrica que ajuda de duas formas: a **sustentabilidade** do lucro e se há uma clientela fiel. Descontos são importantes, claro, mas em excesso, podem diminual o seu lucro. Um percentual baixo é ideal.

Essas três métricas combinadas, fornecem uma boa visão do negócio, combinando **volume**, **eficiência** e **sustentabilidade**.

## 4. Principais Insights

A análise, consolidada no dashboard interativo, revelou descobertas importantes para o próximo mês.

* **Ranking Geral de Performance:** A análise do período completo revelou que existe uma pequena diferença na consistência da performance entre as lojas. **A loja highway-adidas-shopping apresentou uma melhor perfomance, enquanto a highway-praca-ekin obteve a pior**.

* **Descoberta 1 - Eficiência vs. Volume:** A loja com o pior desempenho médio não é necessariamente a que menos fatura, mas sim a que apresenta o **menor 'Torque Médio'**. Isso mostra uma dependência da venda de itens de baixo valor, o que prejudica a saúde financeira geral, mesmo com um número razoável de transações.

* **Descoberta 2 - O Custo dos Descontos:** O dashboard mostra que algumas lojas, embora apresentem alta receita, também usam um percentual de descontos alto. Isso pode ser uma fragilidade, pois a alta receita pode estar vindo à custa de uma lucratividade reduzida. Como exemplo, temos a **highway-rua-bens-perdidos**, que apresenta a segunda maior receita, mas apresenta a maior porcentagem de descontos.

## 5. Recomendações para Julho de 2025

Com base nos insights, sugiro as seguintes ações de curto prazo:

1.  **Ação para a Loja de Pior Performance:** Focar na venda de combos e itens adicionais de maior valor.

2.  **Otimização de Promoções:** Para a loja com o maior percentual de descontos, rever as promoções ativas, com o intuito de verificar o impacto no lucro.

3.  **Replicar o Sucesso:** Investigar as práticas da loja com o melhor ISF. O que ela faz de diferente? Seu mix de produtos é mais rentável? Sua equipe é mais eficiente? Ela deve servir como modelo.

## 6. Limitações e Próximos Passos

Para evolução da análise, pois sempre há espaço para melhorias, penso em 4 pontos:

* **Próximos Passos (com mais tempo):**
    * **Melhora no ISF:** Utilizar outras métricas que sejam relevantes (uso de modelos de IA e estatística para definir relevância) para a incrementação do índice atual, o deixando mais robusto.
    * **Análise Preditiva:** Utilizar o histórico de dados diários para construir um modelo de previsão que possa estimar a receita e o ISF para os próximos meses, ajudando no planejamento.
    * **Análise de Produtos:** Aprofundar a análise dos itens para entender quais produtos são frequentemente comprados juntos e otimizar a criação de novos combos e ofertas.
    * **Análise de Pagamentos:** Realizar uma análise das formas de pagamento mais comuns, a fim de indentificar a forma menos utilizada, e, se viável, aplicar descontos se for pago nesse formato.