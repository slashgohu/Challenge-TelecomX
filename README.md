# Relatório Final: Análise de Evasão de Clientes - TelecomX

### Introdução

Este relatório apresenta os resultados da análise de evasão de clientes na empresa TelecomX. O objetivo principal foi identificar padrões e fatores que contribuem para que os clientes cancelem seus serviços, fornecendo insights para a formulação de estratégias de retenção.

### Limpeza e Tratamento de Dados

A etapa inicial da análise envolveu a importação e o tratamento de dados. Os dados foram carregados a partir de um arquivo JSON online e normalizados de forma adequada, incluindo:

* **Importação de Dados**: Os dados foram importados de uma URL via `requests` e `json`, e posteriormente convertidos para DataFrame.
* **Normalização**: A estrutura do arquivo JSON foi "normalizada" para criar um DataFrame (`dados_normalizados`), onde cada linha representa um cliente e suas respectivas características.
* **Verificação de Valores Ausentes**: Foi realizada uma inspeção para identificar e tratar possíveis valores ausentes, garantindo a integridade dos dados para análises subsequentes.
* **Verificação de Duplicados**: Foi verificada a presença de registros duplicados para assegurar a integridade dos dados.
* **Criação de Novas Features**: Uma nova coluna `Gasto_Diario` foi criada a partir dos dados existentes no DataFrame, enriquecendo o conjunto de dados para futuras análises.

### Análise Exploratória de Dados

A Análise Exploratória de Dados revelou diversos padrões e correlações importantes, utilizando visualizações gráficas para melhor compreensão.

**Insights Visuais Chave:**

A partir das análises visuais, podemos destacar os seguintes pontos:

* **Taxa de Cancelamento Geral**: A taxa de cancelamento é uma métrica crítica que indica a porcentagem de clientes que descontinuam seus serviços.
* **Serviço de Internet e Contrato**: Clientes com serviço de internet de `Fiber optic` (Fibra Óptica) e contratos `Month-to-month` (Mês a Mês) apresentaram um risco de cancelamento significativamente mais alto. Isso sugere que a qualidade da conexão e a flexibilidade do contrato são fatores determinantes para tal ato.
* **Período de Permanência**: Foi observado que os primeiros 12 meses de contrato são um período crítico, com uma maior probabilidade de cancelamento. Isso indica a necessidade de estratégias de engajamento e fidelização mais intensivas nos estágios iniciais do relacionamento com o cliente.
* **Impacto Financeiro**: Clientes que cancelam tendem a ter um valor médio de `Cobranças Mensais` que impacta a receita.

### Conclusões e Insights

A análise de churn da TelecomX revelou que a evasão de clientes não é um problema isolado, mas sim um resultado da interação de diversos fatores. Os clientes com serviços de fibra óptica e contratos mensais representam o maior grupo de risco, indicando que a percepção de valor e a flexibilidade contratual são cruciais. Além disso, o período inicial de uso (até 12 meses) é crítico, sugerindo que muitos clientes podem estar testando o serviço ou enfrentando dificuldades de adaptação. O que reforça a necessidade de ações preventivas.

### Recomendações
Com base na análise, recomendamos as seguintes ações reduzir a taxa de cancelamentos:

Foco nos Clientes de Fibra Óptica com Contrato Mensal: Desenvolver programas de fidelidade, ofertas especiais ou melhorias no suporte técnico.

Análise de Satisfação do Cliente: Realizar pesquisas regulares para medir a satisfação e a probabilidade de recomendação. Utilizar o feedback para identificar pontos de melhoria nos serviços e no atendimento.

Monitoramento Contínuo: Implementar um sistema de monitoramento contínuo para identificar clientes com alto risco de cancelamento antes que eles decidam cancelar. Isso pode ser feito através de indicadores como uso de serviço, histórico de reclamações e uso dos canais de suporte.

Ofertas Personalizadas: Utilizar os dados de perfil do cliente para criar ofertas de retenção personalizadas que abordem suas necessidades específicas e preocupações, como upgrades, descontos ou pacotes adicionais.
