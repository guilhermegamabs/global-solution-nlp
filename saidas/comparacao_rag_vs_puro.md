# Comparação RAG vs LLM puro

## P01 — O que caracteriza um edificio Net Zero Energy e como se calcula o balanco energetico anual?

### Com RAG
Um edifício é considerado Net Zero Energy (NZEB) quando seu potencial de geração de energia (PG) obtido for igual ou maior a 50%. Este potencial é calculado usando a fórmula fornecida na fonte [fonte, 2025], onde o potencial de geração é então calculado a partir da Equação D.1 da INI-C e INI-R.

O balanço energético anual do edifício NZEB é caracterizado pela igualdade entre as quantidades de energia gerada (EE) e consumida (ET). Portanto, o potencial de geração de energia deve ser maior ou igual a 50% para classificar um edifício como Net Zero Energy.

**Fontes:** USGBC (2014) - LEED v4 para Projeto e Construção de Edifícios.pdf; orgao (2025) - Manual Geração Local de Energia Renovável e Informativos.pdf

### Sem RAG (LLM puro)
Um edifício "Net Zero Energy" (NZE) é aquele que produz energia suficiente para suprir suas próprias necessidades durante todo o ano. Isso geralmente ocorre através da geração de energia renovável, como solar ou eólica, combinada com uma eficiência energética muito alta.

Características principais de um edifício NZE:

1. **Eficiência Energética**: O edifício deve ser projetado para minimizar a necessidade de energia elétrica.
2. **Geração de Energia Renovável**: A geração de energia solar, eólica ou outra fonte renovável deve ser suficiente para suprir as demandas do edifício.
3. **Balanceamento Anual**: O edifício deve gerar mais energia que sua demanda anual durante pelo menos 12 meses em um ano.

O balanço energético anual é uma medida importante de eficiência energética e geração de energia renovável. Ele se refere ao excesso ou déficit de energia produzida por um sistema de geração de energia contra a demanda total do edifício durante um período específico, geralmente um ano.

Para calcular o balanço energético anual:

1. **Geração de Energia**: Total da energia gerada pelo sistema de geração de energia (por exemplo, solar ou eólica).
2. **Demanda Energética**: Total da energia consumida pelo edifício durante o mesmo período.
3. **Balanceamento Anual**: Geração - Demanda.

Se a geração for maior que a demanda, temos um balanço positivo de energia (o edifício produziu mais do que consumiu). Se a demanda for maior, teremos um balanço negativo ou zero. Um NZE deve ter um balanceamento anual positivo durante pelo menos 12 meses em um ano.

É importante notar que o conceito de NZE pode variar dependendo da região e do tipo específico de edifício (residencial, comercial, industrial). Além disso, a eficiência energética é uma parte crucial para atingir esse status.

**Análise:** precisao / rastreabilidade / alucinacao

---

## P05 — Quais parametros de desempenho termico a ABNT NBR 15575 estabelece para a envoltoria?

### Com RAG
Não encontrei essa informação no corpus.

**Fontes:** ENCAC (2019) - AUTOMAÇÃO PREDIAL TECNOLOGIA E GESTÃO EM PROL DA.pdf; USGBC (2014) - LEED v4 para Projeto e Construção de Edifícios.pdf

### Sem RAG (LLM puro)
A ABNT (Associação Brasileira de Normas Técnicas) NBR 15575 não é diretamente relacionada à especificação dos parâmetros de desempenho térmico da envolta ou envoltória de edifícios. Essa norma geralmente aborda aspectos como a segurança e o funcionamento de sistemas elétricos em edifícios residenciais, não focando especificamente nos parâmetros térmicos.

Para os parâmetros de desempenho térmico da envolta ou envoltória de edifícios, você deve consultar normas específicas como a ABNT NBR 6890 (para edifícios residenciais) e ABNT NBR 15742 (para edifícios comerciais). Essas normas estabelecem parâmetros de desempenho térmico, como o coeficiente de transmissão térmica (CTT), a taxa de perda de calor por convecção convectiva e radiativa (TCR) e outros, que devem ser atendidos para garantir um bom desempenho térmico do edifício.

**Análise:** precisao / rastreabilidade / alucinacao

---

## P08 — Quais sao os criterios para dimensionar um sistema de captacao de agua pluvial em edificacoes?

### Com RAG
Os critérios para dimensionar um sistema de captura de água pluvial em edificações são apresentados no Manual do Dimensionamento de sistemas de aproveitamento de águas pluviais, que pode ser encontrado na referência [SABESP, 2015]. Segundo este manual, os principais critérios para dimensionar um sistema de captura de água pluvial incluem:

1. Determinação da demanda: O empreendedor deve mapear e estimar o consumo de água que pode ser atendido com a água de chuva.

2. Determinação da área de captação: A área de captação é a projeção do telhado na horizontal, dando-se preferência aos telhados que possibilitem a captura de água com melhor qualidade.

3. Determinação do índice pluviométrico: Este critério considera os índices pluviométricos da localidade e influencia na determinação da vazão diária ou mensal demandada.

4. Calhas e condutores: A instalação adequada de calhas e condutores é fundamental para a captura eficaz da água de chuva.

5. Filtro autolimpante: O sistema deve incluir um filtro autolimpante para remover partículas e impurezas da água de chuva.

6. Água de limpeza do telhado (água da primeira chuva): A água coletada na primeira chuva, antes que a água seja liberada para o sistema de drenagem, deve ser tratada adequadamente.

7. Reservatório de armazenamento: O dimensionamento adequado do reservatório é crucial para garantir uma capacidade suficiente de armazenamento da água coletada.

8. Tratamento da água pluvial: O manual sugere que o sistema de aproveitamento de águas pluviais deve ser acompanhado por um tratamento adequado, conforme as normas técnicas vigentes e as especificações do projeto.

Fonte: [SABESP, 2015]

**Fontes:** AQUA-HQE/GBC Brasil (2020) - Avaliação das Práticas Sustentáveis Aplicadas as Certificações Água-HQE e GBC Brasil Casa.pdf; SABESP (2015) - Aproveitamento de Água Pluvial.pdf; periodico (2020) - REÚSO DE ÁGUAS CINZAS EM EDIFICAÇÕES URBANAS VISANDO A.pdf

### Sem RAG (LLM puro)
Para dimensionar um sistema de captação de água pluvial em edificações, é importante considerar vários fatores que afetam a eficiência e o desempenho do sistema. Aqui estão alguns dos principais critérios:

1. **Volume de Água Pluvial**: O volume de água que pode ser capturada depende da área coberta pela captação (por exemplo, telhado) e da taxa de precipitação local.

2. **Taxa de Precipitação**: Essa é uma medida do quanto a chuva cai em determinado período de tempo. É importante considerar as condições climáticas locais para dimensionar o sistema adequadamente.

3. **Capacidade de Armazenamento**: Dependendo da necessidade, pode ser necessário armazenar água pluvial para uso posterior, como irrigação ou regeneração de filtros de esgoto. O volume de armazenamento deve ser suficiente para atender às demandas do sistema.

4. **Reutilização e Reciclagem**: Se o objetivo é reutilizar a água capturada (por exemplo, para uso doméstico), é importante dimensionar o sistema para atender à quantidade necessária de água por pessoa ou por área da edificação.

5. **Filtragem e Purificação**: Em muitos casos, a água pluvial pode precisar ser filtrada e purificada antes de ser utilizada. O sistema deve ser projetado para lidar com as impurezas presentes na água pluvial.

6. **Condições Climáticas Locais**: As condições climáticas locais podem influenciar o volume de água que é capaz de ser capturada e armazenada, bem como a necessidade de tratamento da água.

7. **Regulamentações Ambientais**: Em muitos países, existem leis e regulamentos ambientais que determinam as capacidades mínimas de captação e reutilização de água pluvial em edificações.

8. **Eficiência Energética**: O sistema deve ser projetado para minimizar o consumo de energia durante a operação (por exemplo, através da filtragem ou purificação).

9. **Sustentabilidade**: É importante dimensionar o sistema de maneira que ele seja sustentável e não cause impactos negativos no meio ambiente.

10. **Manutenção**: O sistema deve ser projetado para facilitar a manutenção preventiva, garantindo sua eficiência ao longo do tempo.

É essencial consultar especialistas em engenharia ambiental ou de água para dimensionar adequadamente um sistema de captação de água pluvial.

**Análise:** precisao / rastreabilidade / alucinacao

---
