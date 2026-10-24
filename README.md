# Miniprojeto_PauloRodrigoZanin_T8
Mini-Projeto Avaliativo - SCTECH Turma T8 - Paulo Rodrigo Zanin

# Objetivo
Desenvolver uma Análise Exploratória de Dados (AED) aplicada ao varejo, transformando dados brutos em informações que ajudem a compreender o negócio.

# Dados de origem
Dados brutos obtidos da plataforma Kaggle: 
https://www.kaggle.com/datasets/namespaiva/base-varejo/data

# Ambiente de desenvolvimento

Jupyter Notebook dentro do VS Code.

# Bibliotecas Python

Pandas

# Arquivos do repositório

notebook_relatorio.ipynb
dados_brutos.csv
varejo_limpo.csv

# Sprint 1 (Leitura e Diagnóstico)
Nesta etapa foi baixado manualmente o arquivo CSV com os dados brutos (renomeado para "dados_brutos.csv"), importados para o notebook, e feita uma verificação da estrutura dos dados brutos com registro de valores ausentes, duplicatas, e inconsistências de texto.

# Sprint 2 (Limpeza e Padronização)
Nesta etapa foram corrigidos os problemas encontrados no SPRINT 1, justificadas as escolhas do tratamento dos problemas encontrados e feita uma comparação entre os dados brutos e os dados tratados nesta etapa (pré-processados).

# Sprint 3 (Funções e Organização)
Nesta etapa foram criadas e usadas uma função de tratamento e outra de resumo dos dados, com parâmetro e retorno (é repetido o que foi feito no SPRINT 2, mas usando funções).

# Sprint 4 (Análise)
Nesta etapa são gerados dois agrupamentos e posteriormente são calculadas as estatísticas básicas destes agrupamentos. Também é aplicado um filtro, feito um agrupamento e calculadas suas estatísticas básicas. 

# Sprint 5 (Exportação e Comunicação)
Nesta etapa é salvo um CSV com os dados tratados e apresentadas as conclusões finais deste notebook/relatório.

# Sprint 6 (Revisão e Entrega)

O notebook foi executado novamente, revisado, corrigido em pequenos detalhes, executado novamente e enviado para avaliação.

# Conclusões Finais

A análise exploratória partiu de 830.000 registros brutos de vendas de um comércio varejista do tipo mercado e resultou em uma base tratada com 826.350 registros e 10 colunas, salva em “varejo_limpo.csv”. 

Os principais resultados foram:

-Qualidade dos dados: foram removidas 4 colunas vazias e 3.650 linhas com “#N/D” (0,44% da base), e a coluna de datas foi convertida para o tipo data. Não havia inconsistências de texto.

-Concentração por categoria: ALIMENTOS responde por 434.767 registros de vendas (53% do total), seguida de HIGIENE (155.574) e LIMPEZA (145.754). Juntas, essas três categorias representam 89% das vendas. PET (32.399) e ACESSÓRIOS (14.557) têm as menores participações.

-Desempenho por tipo de produto: ACESSÓRIOS tem a maior média de vendas por tipo de produto (7.278,50), mas com apenas 2 tipos de produtos. ALIMENTOS, com 61 tipos de produtos, tem média de 7.127,33.

-Gênero: as mulheres respondem por 430.658 registros e os homens por 395.692, com os mesmos 117 tipos de produtos para ambos.

-Padrão entre as mulheres: ao filtrar o gênero feminino, a distribuição por categoria se manteve (ALIMENTOS com 226.575 registros e ACESSÓRIOS com 7.700). A única diferença foi o menor valor por tipo de produto, que passou de ALIMENTOS (3.574) para PET (1.861).

Recomendação: como ALIMENTOS, HIGIENE e LIMPEZA concentram quase 90% das vendas, e esse padrão se repete entre as mulheres, sugere-se priorizar nessas categorias o estoque e as ações promocionais, inclusive as voltadas ao público feminino. Como ACESSÓRIOS e BEBIDAS têm poucos tipos de produtos, mas médias por produto altas (7.278,50 e 7.216,50), vale testar a ampliação do tipo de produtos dessas categorias, com acompanhamento posterior dos resultados.

Limitação: a base não possui coluna de quantidade ou valor monetário (ou está indefinido no nome abreviado das colunas). Por isso, cada registro foi tratado como uma venda, sem considerar preço, receita ou quantidade por item. Os resultados indicam a frequência de itens vendidos, e não o faturamento. Além disso, as linhas totalmente duplicadas (96.553 na base bruta) foram mantidas por se supor que são vendas legítimas, o que não pôde ser confirmado.

