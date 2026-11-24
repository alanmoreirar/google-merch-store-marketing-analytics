# Marketing Analytics na Google Merchandise Store: diagnóstico de tráfego, funil e plano de ação (nov/2025)

Nov 23, 2026 · @Alan

## Resumo executivo

Em novembro de 2025, a Google Merchandise Store teve 63.424 usuários ativos e 102.632 sessões, mas perdeu 46,5% das sessões com carrinho já na entrada do checkout e outros 24,9% entre o envio e o pagamento. Este relatório analisa os dados do Google Analytics 4 (GA4) para identificar onde a loja ganha e onde perde audiência e conversão.

**Quatro achados**

1. **A audiência caiu, e a queda é quase toda dos EUA.** Na comparação com novembro de 2024, os usuários ativos recuaram 24,0% e as sessões 16,9%. Os EUA respondem por 97% da perda de sessões (20.220 de 20.813).
2. **O engajamento melhorou.** A taxa de rejeição foi de 40,9%, contra 44,4% um ano antes e 42,7% no período anterior.
3. **A aquisição depende de tráfego direto e orgânico.** Direto (31,2% das sessões) e busca orgânica do Google (28,3%) somam quase 60%. A mídia paga (google / cpc) responde por 11,7%.
4. **O gargalo está no checkout.** De cada 100 sessões com item no carrinho, 46 não iniciam o checkout e, das que chegam ao envio, 25 não informam o pagamento.

**Três recomendações, em ordem de prioridade**

1. Extrair compras, receita e taxa de conversão e segmentar o funil por país e dispositivo, para saber onde o abandono ocorre.
2. Reduzir o atrito no checkout: compra como convidado e custo total (frete e impostos) visível antes do pagamento.
3. Testar e-mails de recuperação de carrinho com metas e grupo de controle.

A seção de limitações explica por que os dados permitem diagnosticar, mas não provar as causas.

## Introdução e metodologia

Este relatório usa o GA4 para diagnosticar o desempenho da Google Merchandise Store em novembro de 2025 e propor ações priorizadas. Marketing analytics, aqui, é o uso sistemático de dados para decidir onde investir, o que corrigir e como medir o resultado (MICELI; CORRÊA, 2025).

A loja vende vestuário, acessórios, brindes e itens corporativos com a marca de produtos do ecossistema Google, como YouTube, Drive e Gemini. Ela funciona como vitrine institucional e como ambiente de testes para coleta de dados (ART+SCIENCE, 2024) e atende consumidores de várias regiões, com envio internacional em categorias específicas (ROBERTSON, 2025). A compra ocorre apenas pelo site, sem aplicativo próprio.

O GA4 é a plataforma do Google que coleta, organiza e apresenta dados de navegação para apoiar decisões de marketing (COSTA, 2023). Ele é indicado para jornadas complexas (DOURADO, 2025) e para identificar tendências e problemas de experiência do usuário (KINGHOST, 2025).

**Recorte e comparações.** O período principal é 1 a 30 de novembro de 2025. Ele foi comparado com o período anterior de mesma duração do GA4 (4 de outubro a 2 de novembro de 2025, que não coincide com outubro fechado) e com 1 a 30 de novembro de 2024.

**Definições usadas.**

| Métrica | Como o GA4 conta | Fonte |
| --- | --- | --- |
| Sessão | Período em que o usuário está ativo no site | GOOGLE (2025) |
| Usuários ativos | Usuários com ao menos uma sessão engajada no período | FORMAGGIO (2024) |
| Novos usuários | Usuários cuja primeira visita (evento first\_visit) ocorreu no período | FORMAGGIO (2024) |
| Sessão engajada | Sessão com mais de 10 s, ao menos um evento principal ou duas ou mais visualizações de página | REPORTEI (s.d.) |
| Taxa de rejeição | Sessões não engajadas ÷ sessões; equivale a 100% − taxa de engajamento | REPORTEI (s.d.) |

No GA4 a rejeição não significa mais "sessão de uma página", definição do Universal Analytics (REPORTEI, s.d.).

**Limitações.** Elas afetam como cada conclusão deve ser lida:

- Os dados vêm da conta de demonstração do GA4 da loja, usada também em cursos. Parte do tráfego pode ser de estudantes, como sugere a origem art-analytics.appspot, e os resultados não representam a operação comercial real.
- Os relatórios consultados não exibem compras, receita nem taxa de conversão. O diagnóstico de funil termina na etapa de pagamento.
- Os eventos do funil são contados em sessões com o evento, não em usuários únicos em sequência. Para uma leitura rigorosa, o ideal é uma exploração de funil do GA4.
- Os cartões demográficos exibem alertas de dados parciais, então gênero e idade são indicativos.
- Associação não é causa: as explicações apresentadas são hipóteses a testar.

## Diagnóstico: volume, comparações e audiência

O engajamento cresceu e o volume recuou, e o recuo vem de um único mercado: os EUA. A tabela compara novembro de 2025 com o período anterior do GA4 e com novembro de 2024.

| Métrica | Nov/2025 | Período anterior (4 out–2 nov/2025) | Variação | Nov/2024 | Variação |
| --- | --- | --- | --- | --- | --- |
| Sessões | 102.632 | 90.391 | +13,5% | 123.445 | −16,9% |
| Usuários ativos | 63.424 | 61.233 | +3,6% | 83.456 | −24,0% |
| Taxa de rejeição | 40,9% | 42,7% | −1,8 p.p. | 44,4% | −3,5 p.p. |

Fonte: Google Analytics 4, conta de demonstração da Google Merchandise Store.

A taxa de engajamento foi de 59,1%: 60.608 das 102.632 sessões foram engajadas. Como a rejeição é o complemento do engajamento no GA4 (REPORTEI, s.d.), a queda de 1,8 ponto percentual sobre o período anterior indica sessões de melhor qualidade mínima, não necessariamente mais compras.

**A queda anual está concentrada nos EUA.**

| Recorte | Sessões 2025 | Sessões 2024 | Variação | Usuários ativos 2025 | Usuários ativos 2024 | Variação |
| --- | --- | --- | --- | --- | --- | --- |
| Total | 102.632 | 123.445 | −16,9% | 63.424 | 83.456 | −24,0% |
| EUA | 56.019 | 76.239 | −26,5% | 33.614 | 51.244 | −34,4% |
| Índia | 8.286 | 6.274 | +32,1% | 6.522 | 4.500 | +44,9% |
| Demais países (total − EUA) | 46.613 | 47.206 | −1,3% | 29.810 | 32.212 | −7,5% |

Os EUA perderam 20.220 sessões de um total de 20.813 perdidas, ou 97%. Sem os EUA, as sessões ficaram praticamente estáveis (−1,3%). O Canadá também recuou (−41,9% em sessões e −49,9% em usuários ativos), enquanto a Índia cresceu. A causa da queda nos EUA não aparece nos dados; as hipóteses estão na seção correspondente.

**Perfil da audiência.** Os EUA concentram 53% dos usuários ativos (33.614 de 63.424), seguidos por Índia (6.522), Canadá (3.158), China (1.946) e Singapura (1.522). O público é predominantemente masculino (61,1% contra 38,9% feminino), de língua inglesa, com maior concentração nas faixas de 18–24 e 25–34 anos e interesse principal em tecnologia, coerente com a marca. Como os cartões demográficos têm alertas de dados parciais, esses percentuais são indicativos.

**Perfil tecnológico.** A loja é 100% web. Desktop responde por 68,1% dos usuários ativos, celular por 30,9% e tablet por 1,1%. Os sistemas mais usados são macOS (20 mil), Windows (16 mil), Android (13 mil) e iOS (7,3 mil), com o Chrome como navegador dominante. Há duas implicações práticas: o checkout deve ser otimizado primeiro para desktop, mas quase um terço do público acessa pelo celular, e a conversão por dispositivo precisa ser medida antes de se decidir onde investir.

## Aquisição de tráfego e funil de compra

Direto e busca orgânica trazem a maior parte do público, a mídia paga contribui com cerca de um oitavo, e o funil perde 61% das sessões com carrinho antes da etapa de pagamento.

**Origem do tráfego.** Segundo a Mailchimp (2025), origens de tráfego são os canais de marketing pelos quais o visitante descobre o site. A tabela usa valores arredondados lidos do relatório de aquisição do GA4.

| Origem / mídia | Sessões | % das sessões | Usuários ativos (primeira origem) |
| --- | --- | --- | --- |
| (direct) / (none) | 32 mil | 31,2% | 29 mil |
| google / organic | 29 mil | 28,3% | 17 mil |
| google / cpc | 12 mil | 11,7% | 7,9 mil |
| art-analytics.appspot | 5 mil | 4,9% | 2,2 mil |
| Newsletter\_October | 4,3 mil | 4,2% | 711 |

Três leituras merecem atenção:

1. **Os novos usuários vêm sobretudo de direto e orgânico, não da mídia paga.** Pela primeira origem, direto e Google orgânico somam cerca de 73% dos usuários ativos, contra cerca de 12% do google / cpc. A mídia paga, que é o investimento em anúncios para atrair visitantes (SEBRAE, 2025), contribui, mas não explica sozinha os 75,7% de usuários novos.
2. **"Direto" não significa só quem digita o endereço.** No GA4 ele também reúne visitas sem origem identificada, como links sem parâmetros UTM e acessos vindos de aplicativos. Isso limita a atribuição e pode esconder o retorno real dos canais.
3. **A newsletter gerou 4,3 mil sessões, mas só 711 usuários**, cerca de 6 sessões por usuário. Isso indica visitas repetidas de uma base pequena (ou tráfego de teste), e não alcance amplo. Sem dados de compra, não se pode avaliar a eficácia do e-mail.

O tráfego de art-analytics.appspot (5 mil sessões) reforça a limitação da conta de demonstração: parte da audiência pode ter origem educacional.

**Funil de compra.** A tabela de eventos do GA4 mostra quantas sessões tiveram cada etapa. Os números abaixo usam sessões com o evento e as quedas entre etapas consecutivas.

&#91;embedded content: Google Analytics 4 · eventos de e-commerce, sessões com o evento, 1–30 nov. 2025\]

A segunda maior perda ocorre, portanto, entre envio e pagamento. É a etapa em que o usuário costuma ver o custo total com frete e impostos, o que é compatível com a hipótese de barreira de custo, mas não a prova. A compra concluída não aparece nos relatórios consultados, então a conversão final não pôde ser calculada.

## Hipóteses e o que os dados não permitem concluir

Os dados descrevem o que aconteceu, não por quê. Cada explicação abaixo é uma hipótese com a evidência disponível e o teste que a confirmaria ou derrubaria. Parte do abandono é natural: nem todo visitante está pronto para comprar, pode comparar alternativas ou precisar de aprovação de terceiros (ASH et al., 2012).

| Hipótese | O que sustenta | O que falta ou contraria | Como testar |
| --- | --- | --- | --- |
| Consumidores norte-americanos mais cautelosos explicam a queda anual | Queda de 34,4% nos usuários ativos dos EUA | A reportagem citada trata de expectativas de inflação e não de tráfego da loja (BARRON'S, 2025); os demais países ficaram estáveis | Comparar sessões por canal nos EUA, nov/2024 vs nov/2025 |
| Menos aquisição (paga ou por e-mail) nos EUA em 2025 | A queda se concentra em um país | Não há dados de investimento | Cruzar sessões por origem / mídia e gasto de mídia |
| A Black Friday impulsionou o mês | A promoção ocorre em novembro | Ela caiu em 28/11/2025 e em 29/11/2024, ambas no recorte, então não explica a queda anual; o gráfico diário do relatório não mostra pico claro em 28/11 | Analisar sessões e compras por dia, de 21 a 30/11 |
| Frete e impostos de importação elevam o abandono no pagamento | A maior queda após o carrinho de compra ocorre entre envio e pagamento (24,9%) | Os EUA são 53% dos usuários, então o efeito de importação pode ser pequeno; não há funil por país | Funil por país e custo total exibido em cada etapa |
| Exigir cadastro ou conta antes de pagar afasta compradores | O custo de tarefas supérfluas no checkout é um argumento recorrente (ASH et al., 2012) | Não foi verificado se a loja exige conta | Teste A/B de checkout como convidado |
| Campanhas atraíram usuários mais qualificados e reduziram a rejeição | A rejeição caiu 1,8 p.p. | Mudança no mix de canais e tráfego da conta demo também explicam; não há rejeição por canal | Rejeição e engajamento por origem / mídia |

Três limites merecem destaque: a conta é de demonstração, não há dados de compra e receita nos relatórios consultados, e os cartões demográficos têm dados parciais. Portanto, as conclusões de negócio valem como direção a validar, não como fato.

## Plano de ação priorizado

O primeiro passo é medir a conversão por país e dispositivo, porque sem ela as demais ações ficam sem linha de base. As metas abaixo são sugestões a calibrar depois dessa medição.

| # | Ação | Problema que ataca | KPI e meta sugerida | Como validar | Esforço / impacto |
| --- | --- | --- | --- | --- | --- |
| 1 | Extrair compras, receita, ticket médio e conversão; montar o funil por país, dispositivo e categoria de produto | Falta de linha de base; funil incompleto | Taxa de conversão por sessão; linha de base em 2 semanas | Exploração de funil do GA4 | Baixo / alto |
| 2 | Comparar as origens de tráfego dos EUA em nov/2024 e nov/2025 | Queda de 34,4% nos usuários ativos dos EUA | Identificar o canal responsável por mais de 50% da perda | Sessões por origem / mídia e gasto de mídia | Baixo / alto |
| 3 | Mostrar o custo total (frete e impostos) antes do pagamento e testar compra como convidado | Queda de 24,9% entre envio e pagamento | Queda envio → pagamento de 24,9% para menos de 20% | Teste A/B de 2 a 4 semanas, com amostra mínima definida antes | Médio / alto |
| 4 | Padronizar parâmetros UTM em e-mail, mídia paga e parcerias | 31,2% das sessões em direto, com origem oculta | Parcela de sessões em (direct) / (none) em queda, meta após a linha de base | Auditoria de links ativos | Baixo / médio |
| 5 | Disparar e-mails de recuperação de carrinho para quem informou o e-mail | 46,5% de queda entre carrinho e checkout | Taxa de recuperação: compras vindas de carrinhos abandonados ÷ carrinhos abandonados | Grupo de controle sem e-mail | Médio / médio |
| 6 | Testar campanhas direcionadas ao público feminino, depois de checar se a conversão difere por gênero | Público 38,9% feminino; Kotler, Kartajaya e Setiawan (2017) apontam o papel crescente das mulheres como decisoras | Conversão por gênero; ampliar a base feminina em direção a um aumento mensurável | Segmento de gênero no GA4 e teste de criativos | Médio / incerto |

A ordem segue o impacto esperado dividido pelo esforço. As ações 1 e 2 são análises, sem custo de mídia, e orientam onde as ações 3 a 6 devem ser aplicadas. A ação 6 vem por último porque a menor presença feminina pode refletir o perfil de interesse em tecnologia, e não uma oportunidade perdida.

## Conclusão

A loja atrai e engaja bem, mas converte mal e depende de um mercado em queda. Os dados de novembro de 2025 mostram engajamento melhor que o de 2024 (rejeição de 40,9% contra 44,4%), audiência concentrada nos EUA (53% dos usuários ativos) e um funil que perde 61% das sessões com carrinho antes do pagamento.

Três achados mudam a leitura habitual desses números. A queda anual de 24,0% em usuários ativos vem quase toda dos EUA; sem eles, as sessões ficaram estáveis. A mídia paga responde por cerca de um oitavo do tráfego, e não pelo crescimento da base. E o principal ponto de perda do checkout, depois do carrinho, ocorre entre envio e pagamento.

A recomendação é começar pela medição: extrair compras, receita e conversão por país e dispositivo e comparar as origens do tráfego dos EUA nos dois anos. Só então vale investir nas ações de checkout, recuperação de carrinho e segmentação, todas com KPI e teste. Como a base é uma conta de demonstração, as conclusões valem como método e direção a validar, não como diagnóstico da operação real.

O trabalho confirma que analytics vai além de coletar dados: os dados e a análise guiam a execução e avaliam o desempenho de um negócio (MICELI; CORRÊA, 2025), desde que se separe o que foi medido do que foi apenas suposto.

## Referências

ART+SCIENCE. **Find the data: Google Merchandise Store and data collection**. Chicago: Art+Science Analytics Institute, 2024. Disponível em: <https://www.artscience.school/blog/google-merch-case-study>. Acesso em: 25 nov. 2025.

ASH, T.; PAGE, R.; GINTY, M. **Landing page optimization: the definitive guide to testing and tuning for conversions**. Indianapolis: Sybex, 2012.

BARRON'S. **Americans see inflation stuck where it is now — and are still downbeat about the economy**. New York: Barron's, 2025. Disponível em: <https://www.barrons.com/articles/inflation-economy-ny-fed-consumer-expectations-bd43a53c>. Acesso em: 13 dez. 2025.

COSTA, D. **O que é Google Analytics? Guia explicativo sobre como usar essa ferramenta**. Belo Horizonte: Rockcontent, 2023. Disponível em: <https://rockcontent.com/br/blog/google-analytics/>. Acesso em: 25 nov. 2025.

DOURADO, B. **Google Analytics: o que é e como fazer a configuração inicial**. Florianópolis: RD Station, 2025. Disponível em: <https://www.rdstation.com/blog/marketing/o-que-e-google-analytics/>. Acesso em: 25 nov. 2025.

FORMAGGIO, E. **GA4: usuários novos e recorrentes**. \[S. l.\]: Diário da Ciência de Dados, 2024. Disponível em: <https://diariodacienciadedados.com.br/ga4-usuarios-novos-e-recorrentes/>. Acesso em: 29 nov. 2025.

GOOGLE. **Sobre as sessões do Google Analytics**. Mountain View: Google, 2025. Disponível em: <https://support.google.com/analytics/answer/9191807?hl=pt-br>. Acesso em: 29 nov. 2025.

KINGHOST. **Introdução ao Google Analytics 4: guia passo a passo para iniciantes**. Porto Alegre: Kinghost, 2025. Disponível em: <https://king.host/blog/tutoriais/como-usar-google-analytics/>. Acesso em: 25 nov. 2025.

KOTLER, P.; KARTAJAYA, H.; SETIAWAN, I. **Marketing 4.0: do tradicional ao digital**. Rio de Janeiro: Sextante, 2017.

MAILCHIMP. **Website traffic sources: o que são e como entender as origens de tráfego**. \[S. l.\]: Mailchimp, 2025. Disponível em: <https://mailchimp.com/pt-br/resources/website-traffic-sources/>. Acesso em: 13 dez. 2025.

MICELI, A.; CORRÊA, K. **Marketing analytics: estratégias e táticas para o crescimento**. Rio de Janeiro: FGV, 2025.

REPORTEI. **Taxa de rejeição**. \[S. l.\]: Reportei, \[s.d.\]. Disponível em: <https://reportei.com/glossary/taxa-de-rejeicao/>. Acesso em: 23 nov. 2026.

ROBERTSON. **Google online merch shop**. Salem: Robertson Marketing, 2025. Disponível em: <https://robertsonmarketing.com/casestudy_google.html>. Acesso em: 25 nov. 2025.

SEBRAE. **Tráfego pago: o que é, como funciona e principais ferramentas**. São Paulo: Sebrae, 2025. Disponível em: <https://sebrae.com.br/sites/PortalSebrae/ufs/sp/conteudo_uf/trafego-pago-o-que-e-como-funciona-e-principais-ferramentas,7e189fd861968810VgnVCM1000001b00320aRCRD>. Acesso em: 13 dez. 2025.
