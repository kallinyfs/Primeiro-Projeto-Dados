# Brasa & Pão Hamburgeria

Dashboard interativo de análise de vendas para a disciplina de Fundamentos de IA e Análise de Dados. A interface foi feita com HTML, CSS e JavaScript puro, com gráficos em Chart.js e importação de arquivos em Papa Parse.

## Como executar

Abra [`public/index.html`](public/index.html) no navegador. A base demonstrativa já aparece na abertura e não depende de `fetch`, servidor local ou etapa de compilação. Os gráficos usam CDNs com versões fixadas; por isso, é preciso ter acesso à internet quando a página for aberta.

Para usar uma base própria, clique em **Importar CSV**. O arquivo é lido localmente no navegador e não é enviado para um servidor. As colunas obrigatórias são:

| Coluna | Descrição |
| --- | --- |
| `id_venda` | Identificador da venda; IDs repetidos são contados uma vez no indicador de vendas. |
| `data` | Data no formato `AAAA-MM-DD`. |
| `produto` | Nome do produto. |
| `categoria` | Categoria do produto. |
| `regiao` | Região da venda. |
| `quantidade` | Número de unidades. |
| `preco_unitario` | Preço de uma unidade, sem símbolo de moeda. |

`dados-exemplo.csv` contém 200 registros fictícios distribuídos por 12 meses. Ele é identificado na interface como base demonstrativa. O arquivo original `vendas_hamburgueria.csv` foi preservado. Ele possui colunas adicionais e não possui `regiao`; ao importá-lo, o dashboard informa essa limitação e agrupa a análise regional como “Não informado”.

## Regras da análise

- Faturamento da linha = `quantidade × preco_unitario`.
- Faturamento total = soma do faturamento das linhas após os filtros.
- Quantidade de vendas = quantidade de `id_venda` únicos.
- Unidades vendidas = soma de `quantidade`.
- Ticket médio = faturamento total ÷ quantidade de vendas; quando não há vendas, o resultado é `R$ 0,00`.

Datas inválidas, números ausentes ou inválidos e campos obrigatórios vazios são descartados. A quantidade descartada é informada após a importação. Valores zero são preservados como números válidos. Nenhuma duplicata é removida automaticamente, porque uma linha pode representar uma venda distinta mesmo quando outros campos coincidem.

## Publicar no Render pelo GitHub

1. Suba este projeto para um repositório no GitHub, incluindo a branch que deseja publicar.
2. No Render, crie um novo serviço do tipo **Static Site** e conecte o repositório.
3. Configure a branch que contém o projeto.
4. Deixe **Root Directory** vazio.
5. Use `echo "Site pronto"` em **Build Command**.
6. Use `public` em **Publish Directory**.
7. Crie o serviço. O Render publicará `public/index.html` como página inicial.

## Verificação

Foi conferido que a base inicial tem 200 registros, que os cálculos usam faturamento por linha, que filtros combinados atualizam cartões, gráficos e tabela, que limpar filtros restaura a visão completa, que a pesquisa e a ordenação funcionam, que a exportação gera CSV e que a tela de nenhum resultado é exibida. Também foram revisados os estilos para telas largas e pequenas.

Como a execução do navegador não está disponível neste ambiente, não foi possível inspecionar o console nem clicar na interface em um navegador real. Ao abrir o arquivo, confirme que a rede está disponível para carregar Chart.js, Papa Parse e a fonte externa; sem CDN, a página mantém a estrutura, mas os gráficos e a importação não funcionarão.
