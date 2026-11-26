# Saneamento Básico na Paraíba: Análise Geoespacial e Histórica (SNIS / IBGE)

Painel interativo desenvolvido em Power BI para monitorar a cobertura de abastecimento de água e esgotamento sanitário nos 223 municípios da Paraíba, comparando o desempenho estadual com a média nacional e evidenciando desigualdades territoriais.

---

## Objetivo

Construir um diagnóstico territorial e histórico do saneamento básico na Paraíba que permita:

- Identificar áreas críticas e bolsões de vulnerabilidade por município e mesorregião;
- Comparar a cobertura ponderada pela população com a distribuição de municípios por faixa de atendimento;
- Acompanhar a evolução histórica por década para distinguir déficits pontuais de problemas crônicos;
- Apoiar a priorização de ações e políticas públicas com base em critérios geoespaciais.

A abordagem metodológica reflete a prática de inteligência territorial aplicada ao mapeamento de indicadores regionais para identificação de zonas prioritárias.

---

## Demonstração

![Navegação do painel — Visão Resumo com alternância entre Água e Esgoto](assets/demo-resumo.gif)

*Alternância dinâmica entre os indicadores de Água e Esgoto via bookmarks, atualizando KPIs, mapa coroplético, textos analíticos e distribuição regional na mesma tela.*

![Exploração detalhada e tooltips históricos](assets/demo-detalhe.gif)

*Páginas analíticas com filtro por década, ranking de municípios mais vulneráveis e tooltips sob demanda com a evolução histórica de cada município.*

---

## Principais Achados

### 1. Estagnação histórica e déficit estrutural
- **Abastecimento de água:** 74,8% de cobertura estadual (2,97 milhões de atendidos; déficit de 1 milhão de habitantes), ficando 10,2 p.p. abaixo da média nacional (85%). Após avançar de 31% para 74% até 2010, o indicador estagnou na década seguinte.
- **Esgotamento sanitário:** apenas 39% de cobertura (1,54 milhão de atendidos; déficit de 2,43 milhões de habitantes), 17,1 p.p. abaixo da média nacional (56%). Depois de saltar de 19% (2010) para 37% (2015), o crescimento praticamente parou.
- **Assimetria entre serviços:** existe uma distância de quase 36 pontos percentuais entre o acesso à água e à coleta de esgoto no estado.

### 2. Concentração regional e desigualdade mascarada pela média
- **Mata Paraibana:** apresenta a maior cobertura populacional do estado tanto em água (85,9%) quanto em esgoto (51,4%), mas o agregado é puxado pela capital. Em água, 34,5% dos municípios com dados (10 de 29) estão em faixa crítica ou muito crítica.
- **Borborema (efeito de peso populacional):** em esgoto, lidera o estado em quantidade de municípios acima da média nacional (13 de 22 com dados, ou 59,1%), mas atende apenas 30,8% da população regional. O contraste evidencia que pequenos municípios atingem bons índices na sede urbana, enquanto os mais populosos puxam a cobertura agregada para baixo.
- **Sertão:** maior região em número de municípios (83), concentra em termos absolutos tanto os destaques positivos quanto os críticos em água (13 acima da média nacional e 19 críticos/muito críticos) e apresenta a menor cobertura populacional de esgoto do estado.

### 3. Apagão de dados como achado analítico
- A ausência de informações no SNIS atinge 22 municípios em água (9,9%) e salta para 144 municípios em esgotamento sanitário (64,6% do estado).
- Entre os municípios com registro em esgoto, mais da metade (43 de 78) encontra-se em situação crítica ou muito crítica. A própria lacuna de reporte indica fragilidade na gestão local e sugere que o déficit real pode ser ainda maior.

### 4. Priorização territorial
O cruzamento entre mapa coroplético, histórico por década e ranking de vulnerabilidade evidencia duas frentes distintas de atenção:
- **Alto impacto populacional:** municípios populosos próximos a grandes centros com baixíssima coleta de esgoto (ex.: Santa Rita com 4% e Queimadas com 2%);
- **Vulnerabilidade crônica no interior:** municípios em faixa crítica de forma persistente desde os anos 2000 (ex.: Barra de Santana com 7% em água e Conceição com 0% em esgoto).

---

## Recursos Técnicos do Projeto

- **Navegação e Interatividade:** menu lateral fixo (Resumo, Água, Esgoto e Sobre) e alternância entre indicadores na página de Resumo usando Bookmarks e seleção de visuais.
- **Visualização Geoespacial:** mapa coroplético municipal construído com shapefile oficial da Paraíba (UFPB) e classificação dinâmica por faixas de cobertura.
- **Tooltips Analíticos:** páginas de tooltip configuradas para exibir a série histórica e KPIs individuais ao passar o mouse sobre cada município no mapa.
- **Modelagem e DAX:** tabelas desconectadas para classificação dinâmica de municípios por faixa de cobertura, cálculo de diferença em pontos percentuais (p.p.) frente à média nacional e tratamento explícito de municípios sem reporte.

---

## Limitações Metodológicas

- **Ano de referência:** 2022 (última consolidação disponível na base utilizada).
- **Subnotificação no SNIS:** municípios classificados como "Sem dados" não possuem registro para o ano de referência. Como a cobertura estadual e regional é ponderada pela população total (IBGE), a ausência de reporte em 144 municípios no esgotamento sanitário impacta os percentuais agregados e limita a visibilidade completa do território.

---

## Fontes de Dados

- **Saneamento:** Sistema Nacional de Informações sobre Saneamento (SNIS)
- **População:** Instituto Brasileiro de Geografia e Estatística (IBGE)
- **Malha Geográfica:** Shapefile dos municípios da Paraíba (UFPB)
- **Divisão Regional:** Mesorregiões da Paraíba (IBGE / Wikipedia)
