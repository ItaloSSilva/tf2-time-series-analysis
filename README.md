# tf2-time-series-analysis
Análise de séries temporais sobre a crise dos bots no Team Fortress 2 e o impacto das ações da comunidade (#SaveTF2) na retenção orgânica de jogadores.

# O Impacto da Comunidade e a Crise dos Bots no Team Fortress 2 📊

Uma análise de séries temporais sobre a retenção de jogadores e as intervenções da desenvolvedora em resposta à comunidade.

## Sobre o Projeto
O Team Fortress 2 (TF2) sofreu nos últimos anos com uma infestação massiva de contas automatizadas (bots), prejudicando a integridade dos servidores casuais. Este projeto de análise de dados tem como objetivo investigar o impacto real dessa crise e validar, através de dados numéricos, a correlação entre as campanhas online da comunidade (como os movimentos `#SaveTF2` e `#FixTF2`) e as grandes ondas de banimento executadas pela Valve.

O projeto foi estruturado seguindo o framework completo de análise de dados: **Perguntar, Preparar, Processar, Analisar, Compartilhar e Agir**.

## Tecnologias Utilizadas
* **Linguagem:** Python
* **Ambiente:** Jupyter Notebook / Google Colab
* **Manipulação de Dados:** Pandas
* **Visualização:** Matplotlib, Seaborn
* **Fontes de Dados:** SteamDB, Tabela dimensional de marcos temporais (criada manualmente)

## Metodologia e Estrutura dos Dados

### 1. Preparação e Limpeza
Os dados brutos extraídos do SteamDB continham ruídos de variações de tráfego dia/noite. O processamento incluiu:
* Conversão de variáveis do formato `String` para `Datetime`.
* Indexação temporal (`Index`) para facilitar o fatiamento analítico.
* Aplicação de Média Móvel (*Rolling Average*) de 7 dias para expor a tendência isolada da variação normal diária.

### 2. Análise Exploratória
Cruzamento da série temporal de jogadores simultâneos com os eventos históricos delimitados na tabela dimensional `tf2_eventos.csv`. A análise focou no isolamento de perfis robóticos através da observação de quedas antinaturais nas curvas de retenção.

## Principais Insights e Conclusões
1. **A Verdadeira Escala dos Bots:** A queda vertical drástica logo após o "Banimento de Verão" (Junho/Julho de 2024) revela a verdadeira proporção de contas automatizadas que inflavam a contagem. 
2. **Causalidade entre Comunidade e Empresa:** A análise gráfica demonstra uma forte correlação temporal entre as manifestações na internet e as ações da desenvolvedora. Grandes banimentos (linhas azuis) ocorreram consistentemente semanas após massivas mobilizações nas redes sociais (linhas vermelhas).
3. **Estabilização da Retenção Orgânica:** Após as limpezas de servidores no meio de 2024, a média de jogadores encontrou um platô que, apesar de ser inferior ao de 2023, representa fielmente a retenção humana e orgânica do jogo.

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone [https://github.com/SEU-USUARIO/tf2-time-series-analysis.git](https://github.com/SEU-USUARIO/tf2-time-series-analysis.git)
