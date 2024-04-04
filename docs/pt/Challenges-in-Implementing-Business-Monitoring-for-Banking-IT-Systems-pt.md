# Desafios na Implementação de Monitoramento de Negócios para Sistemas Bancários de TI

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-ru.md)

Em nossa discussão prévia, exploramos os principais indicadores de negócios e as regras para seu monitoramento. Contudo, ao implementar essas medidas, enfrentamos obstáculos significativos, especialmente em áreas como:

**1. Coleta de Informações Básicas das Transações**

Para um monitoramento eficaz, é crucial que o sistema colete com precisão detalhes de cada transação. Isso inclui identificar o sistema requisitante, o código da transação, informações chave, o sistema e o nó de serviço envolvidos, além dos momentos de início e término, o número de série, a instituição financeira, o valor, e os códigos de resposta dos sistemas envolvidos. No entanto, muitos sistemas falham em fornecer todos esses dados essenciais, dificultando, por exemplo, a obtenção do código de resposta do sistema de serviço. Se o sistema de produção não foi desenhado para capturar essa informação desde o início, adaptá-lo para isso se torna um grande desafio. A ausência desses dados impede o cálculo preciso da taxa de sucesso das transações de serviços. Adicionalmente, a transmissão de dados detalhados de transação para o sistema de monitoramento acarreta um volume massivo de informações, pressionando o desempenho do sistema.

**2. Especificações de Desenvolvimento para Sistemas de Produção**

Regras de monitoramento são aplicáveis a todos os sistemas de produção, tornando a padronização do desenvolvimento desses sistemas fundamental. Por exemplo, é crucial uma grande dependência do parâmetro de código de transação. Esse parâmetro deve abranger o sistema requisitante, código de transação, nome da transação, sistema de serviço, flags financeiro, de ocupado e de inativo, entre outros detalhes. Idealmente, cada código de transação deve executar uma única função. Vejamos o código A009: sua decomposição funcional não segue um padrão, fazendo com que ele use um campo tipo sub_type para ramificações funcionais internas. Isso leva um único código de transação a implementar várias funções empresariais, complicando a descrição clara de suas funcionalidades.

Um outro desafio significativo é a padronização do código de desenvolvimento. A exatidão dos alertas de monitoramento é diretamente afetada pelo código de resposta e pelos registros de log do sistema de produção. Durante um projeto no sistema central de compensações do Banco X, enfrentou-se um código de resposta emblemático: 201999-Erro do sistema, indicando falhas graves que o programa não consegue processar ou cuja causa não pode determinar. Esse código de erro era retornado cerca de 800.000 vezes por dia, com uma taxa de sucesso das transações diárias abaixo de 90%. Além disso, os códigos de retorno frequentemente têm múltiplas interpretações. Por exemplo, o código R00001, que deveria indicar "Nenhum registro encontrado", pode ser adaptado para significar desde "Saldo insuficiente" até "Consulta retornou xxx registros". Nessas situações, torna-se impossível determinar o sucesso de uma transação pelo código de retorno. Este problema é ampliado na monitoração empresarial focada em códigos de transação, onde o volume de transações é menor e a precisão na interpretação dos retornos, mais crítica. A padronização urgente dos códigos de retorno se faz necessária.

A padronização dos registros de log, incluindo os de erro, é igualmente crucial. A confiabilidade dos alertas de monitoramento de logs depende da uniformidade desses registros para evitar alarmes falsos ou não detectados.

**3. Ajuste de uma miríade de parâmetros operacionais**

Ao superar os desafios mencionados, os profissionais de operação devem constantemente refinar uma ampla gama de parâmetros operacionais. Para um monitoramento de ponta, é necessário definir parâmetros específicos para cada código de transação. Isso inclui a taxa de sucesso comercial, a taxa de sucesso do sistema, a proporção de picos, a taxa de redução, a relação da linha de base de desvio de indicadores e a quantidade de transações fora do padrão. Estes parâmetros oferecem uma visão detalhada do desempenho dos códigos de transação. Em sistemas de grande escala, com numerosos códigos de transação, ajusta-se a longo prazo dezenas de milhares de parâmetros operacionais, especificamente para os parâmetros dos códigos de transação. Contudo, com regras de configuração de parâmetros bem definidas, é possível desenvolver algoritmos capazes de ajustar automaticamente esses parâmetros operacionais, levando em consideração o desempenho padrão.

Desenvolver um sistema de monitoramento apresenta seus desafios, não pela complexidade de sua criação, mas por torná-lo integralmente alinhado aos objetivos comerciais, maximizando o valor do monitoramento para o negócio e facilitando a evolução de manutenção para operações de TI.

[Artigo original](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
