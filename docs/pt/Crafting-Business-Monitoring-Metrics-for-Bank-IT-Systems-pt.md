# Criando Métricas de Monitoramento para Sistemas de TI em Bancos

Com o avanço do setor financeiro, os serviços oferecidos pelos bancos se tornaram mais complexos, assim como a variedade nas arquiteturas dos seus sistemas de informação. Surge, então, um grande desafio: como identificar falhas apenas com monitoramento técnico? É evidente a necessidade de estratégias de monitoramento voltadas para o negócio, que independam das tecnologias utilizadas e se concentrem em representar as operações empresariais. Utilizando uma vasta experiência operacional e conhecimento aprofundado em monitoramento empresarial, o autor explora quais são as métricas e regras fundamentais para um monitoramento eficiente do negócio.

### Como as Práticas de Monitoramento Evoluíram

**Primeira Fase:** A equipe de TI define manualmente as métricas, regras e parâmetros de monitoramento. Isso geralmente inclui a configuração de scripts em sistemas como o Zabbix, criando condições específicas de alerta baseadas em limites que, ao serem ultrapassados, emitem um aviso.

**Segunda Fase:** As métricas e regras de monitoramento são padronizadas. A equipe de TI fica encarregada de manter os parâmetros operacionais atualizados. Esta etapa avança a anterior ao organizar e uniformizar os critérios de monitoramento, assegurando compatibilidade e consistência entre diferentes sistemas.

**Terceira Fase:** O próprio sistema de monitoramento passa a determinar automaticamente as melhores métricas, regras e parâmetros operacionais, analisando seu desempenho e o dos sistemas em produção. Isso reduz significativamente a necessidade de intervenções manuais pela equipe de TI.

Neste texto, damos atenção especial à segunda fase, sugerindo um conjunto de métricas e regras de alerta universais, baseadas em conhecimentos práticos sobre as operações do negócio.

### Métricas Principais e Regras de Alerta para o Monitoramento de Serviços Bancários

Os sistemas bancários se baseiam em seus códigos de transação ou interfaces, que são definidos por códigos de retorno, volume de transações e tempos de resposta. Este guia apresenta métricas de monitoramento cruciais e regras de alerta com base nessas características, fornecendo um ponto de referência para um monitoramento empresarial efetivo.

**1. Taxa de Sucesso nas Transações**

A taxa de sucesso nas transações é uma métrica fundamental para monitorar a saúde básica de um sistema. Normalmente, considera-se que uma transação foi bem-sucedida se não foram identificados erros sistêmicos, como falhas na rede ou problemas de acesso a arquivos. Contudo, a ausência de erros sistêmicos não significa necessariamente que não há falhas nos processos operacionais. Por exemplo, na transação A001, denominada "consulta de postagens", que usualmente retorna "nenhum registro encontrado", um aumento inesperado no número de postagens pode indicar uma falha. Isso demonstra a importância de distinguir entre as taxas de sucesso do sistema, que focam em falhas técnicas, e as taxas de sucesso empresarial, que avaliam os resultados das transações com base nos códigos de retorno esperados pelos processos de negócios. Essa abordagem detalhada permite um monitoramento mais acurado, indo além das simples taxas de sucesso para analisar os resultados esperados para cada transação.

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Figura 1: Página da Taxa de Sucesso nas Transações

**2. Taxa de Sucesso de Transação no Sistema de Serviços**

Nos sistemas bancários, é crucial distinguir entre os sistemas que realizam as chamadas e os sistemas que prestam os serviços em cada transação. Compreender o desempenho destes últimos é essencial para localizar falhas. Para isso, identifica-se se uma transação aciona um sistema de serviço e qual é ele. A análise das taxas de sucesso das transações associadas a um sistema de serviço específico oferece uma visão da sua confiabilidade. Adicionalmente, examinar os códigos de transação individualmente dentro do sistema pode proporcionar um diagnóstico mais detalhado.

**3. Quando os Nós Silenciam: O Alarme da Ausência de Transações**

No agitado universo do trading de alta frequência, há uma estratégia astuta: ativar um alarme para quando, contra todas as expectativas, nada ocorre. Imagine um mercado efervescente que subitamente se cala. Este alarme dispara quando uma transação específica não se realiza dentro de um intervalo determinado em um ponto específico da rede - é como um alerta para uma "ação faltante". Parecido com esperar uma chamada diária de um amigo e ficar preocupado quando ela não acontece. No entanto, prever quando esperar essa chamada (ou transação) é complicado, já que existem momentos de maior ou menor movimento, similares à diferença entre fins de semana e dias úteis. O desafio é monitorar o vai e vem das transações, identificando aquelas que deveriam estar ocorrendo. Introduzimos, então, a noção de "horários de pico" e "momentos de calmaria", por exemplo, considerando os dias de semana das 8h às 19h como os mais movimentados. Se a transação A002 está ativa o dia inteiro, fica sob vigilância constante. Mas se A003 só aparece nos momentos de maior fluxo, ela tem um descanso nos períodos mais tranquilos. E A004? Se quase não dá sinal de vida durante o dia, fica fora do radar.

**4. Oscilações Bruscas: Monitorando Ondas de Transações**

Diariamente, as transações percorrem seu curso naturalmente, como um rio que flui. Contudo, ao enfrentar um impedimento, esse fluxo pode virar uma enchente ou uma estiagem. Identificar esses extremos é essencial. Pense em acompanhar uma transação, A005, no ápice da tarde. Ao comparar sua atividade com a de um dia típico, mensuramos a variação. Se esta se mantiver dentro de uma faixa de flutuação normal (por exemplo, de 0,8 a 1,2 vezes o habitual), está tudo em ordem. Porém, se despencar para 0,4 ou escalar até 1,6, é momento de ativar o alarme. Esse procedimento, entretanto, encontra dificuldades com transações menos frequentes, nas quais variações mínimas podem parecer grandes turbulências.

**5. Monitorando o Pulso: Rastreando Volumes de Transações Anormais**

Ao examinar detalhadamente as taxas de sucesso das transações, especialmente nos códigos individuais, nos deparamos com um desafio: essa metodologia encontra dificuldades nos extremos das transações de baixíssima e altíssima frequência. Veja só: transações raras acionam alarmes em uma cadência frenética, enquanto aquelas de altíssima frequência podem escapar despercebidas, sem sinalizar que algo está errado.

Considere a transação A006, com seus impressionantes 10.000 registros em apenas 10 minutos, dos quais 50 apresentam problemas. Isso diminui a taxa de sucesso em apenas 0,5% — uma diferença que parece pequena, mas que pode ser crítica. Por outro lado, A007 tem apenas duas transações no mesmo período, mas devido à sua importância financeira, um único problema já é motivo de grande preocupação. A chave? Ajustar os thresholds de alerta personalizados — mais de 10 falhas para A006 e apenas uma para A007 — alinhando-se ao ritmo específico de cada transação, evitando o problema com eficácia. Imagine, então, um painel detalhado que mostra tudo o que deu errado nas transações, desde o nó de processamento até o sistema de serviço, facilitando imensamente o diagnóstico e a resolução de emergências.

**6. O Desafio do Tempo: Ultrapassando os Limites do Tempo de Resposta**

Os sistemas bancários, assim como qualquer sistema eficiente, podem enfrentar dificuldades, desacelerando ou até mesmo parando. O monitoramento convencional pode até notar variações nas taxas de resposta, mas e quando os atrasos se mantêm discretamente abaixo do limite de alerta? Especialmente em transações com grande volume, um pequeno atraso nem sempre implica em uma emergência.

A solução? Monitorar atentamente as transações que apresentam tempos de resposta fora do comum, analisando ciclo a ciclo. Por exemplo, se o A008 normalmente é concluído em 300ms, ultrapassar 600ms ou 900ms pode indicar um problema. Observar três desses casos atípicos dentro de um ciclo é um sinal para acionar o alerta.

**7. Encerrando o Dia, Organizando os Registros**

O encerramento do dia em um sistema bancário, e os processos de finalização, são cruciais para garantir um início tranquilo no dia seguinte. O monitoramento é simples: é necessário que as transações designadas para o fechamento do dia sejam iniciadas e concluídas dentro dos prazos estabelecidos, finalizando com uma confirmação de sucesso. No que tange à organização dos registros, a palavra-chave é regularidade — pequenas variações são normais e não comprometem a rotina.

Concluímos assim nossa jornada pelos bastidores na elaboração de ferramentas de monitoramento empresarial inteligentes e precisas. Aguarde por mais insights sobre os desafios tecnológicos envolvidos nesse processo.

Link para o artigo original: https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
