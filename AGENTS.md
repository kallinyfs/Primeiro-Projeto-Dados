# Orientações do projeto

## Objetivo
Criar dashboards interativos para análise exploratória de dados, com visual profissional e ferramentas simples. O projeto será usado por alunos iniciantes e deve ser fácil de entender, executar e modificar.

## Tecnologias
- Use HTML, CSS e JavaScript puro.
- Use Chart.js para os gráficos e Papa Parse para importar CSV.
- Carregue essas bibliotecas por CDN, com versões fixadas, e explique que isso exige acesso à internet.
- Não utilize React, backend, banco de dados ou ferramentas de compilação.
- O dashboard deve funcionar ao abrir o arquivo index.html no navegador.
- Para arquivos CSV, use um seletor de arquivo e leitura local no navegador.

## Organização
- index.html: estrutura da página.
- styles.css: aparência e adaptação para diferentes telas.
- script.js: importação, tratamento, filtros, cálculos e gráficos.
- dados-exemplo.csv: base fictícia para a atividade.
- README.md: instruções de uso, descrição das colunas e fórmulas dos indicadores.
- Preserve os arquivos originais fornecidos pelo usuário.

## Interface e apresentação
- Escreva os textos em português do Brasil.
- Use fundo claro, cores consistentes, bom contraste e tipografia legível.
- Organize a página com título, filtros, cartões de indicadores, gráficos e tabela.
- Use espaçamento confortável e destaque visual para as informações principais.
- Adapte o layout para computador e celular.
- Inclua títulos, unidades e legendas nos gráficos.
- Use rótulos nos controles e permita navegação por teclado.
- Evite elementos decorativos que atrapalhem a leitura dos dados.

## Interatividade
- Todos os filtros devem atualizar indicadores, gráficos e tabela de forma consistente.
- Inclua um botão para limpar os filtros.
- Exiba a quantidade de registros após a filtragem.
- Mostre uma mensagem clara quando nenhum registro corresponder aos filtros.
- Permita pesquisar e ordenar a tabela.
- Disponibilize a exportação dos dados filtrados em CSV.

## Qualidade da análise
- Examine as colunas e os tipos de dados antes de escolher indicadores e gráficos.
- Diferencie valores ausentes de valores iguais a zero.
- Valide datas e números; informe quantos registros foram descartados e por quê.
- Não remova duplicatas sem verificar o significado de cada linha.
- Não invente dados, resultados ou relações de causa e efeito.
- Identifique claramente qualquer base fictícia usada para demonstração.
- Calcule os indicadores a partir dos dados e documente suas fórmulas.
- Use linhas para evolução temporal e barras para comparações entre categorias.
- Formate números, datas e moedas conforme o padrão brasileiro.

## Simplicidade e aprendizado
- Escreva código legível, com funções pequenas e nomes claros.
- Comente as partes que ajudam a entender os cálculos e as interações.
- Explique decisões importantes em linguagem acessível.
- Se faltar uma informação indispensável, faça uma pergunta objetiva.
- Para escolhas visuais comuns, adote uma solução coerente e prossiga.

## Verificação e entrega
- Confira os cálculos usando uma pequena amostra com resultados conhecidos.
- Verifique importação de CSV, filtros combinados, limpeza dos filtros e ausência de resultados.
- Confira a aparência em telas grandes e pequenas.
- Verifique se há erros no navegador, quando essa ferramenta estiver disponível.
- Informe o que foi verificado e qualquer limitação que permaneça.
- Entregue os arquivos funcionando e explique como abrir e publicar como site