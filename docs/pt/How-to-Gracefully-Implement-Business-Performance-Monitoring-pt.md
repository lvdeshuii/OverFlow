# Como Simplificar o Monitoramento de Desempenho Empresarial

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/How-to-Gracefully-Implement-Business-Performance-Monitoring-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/How-to-Gracefully-Implement-Business-Performance-Monitoring-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/How-to-Gracefully-Implement-Business-Performance-Monitoring-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/How-to-Gracefully-Implement-Business-Performance-Monitoring-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/How-to-Gracefully-Implement-Business-Performance-Monitoring-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/How-to-Gracefully-Implement-Business-Performance-Monitoring-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/How-to-Gracefully-Implement-Business-Performance-Monitoring-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/How-to-Gracefully-Implement-Business-Performance-Monitoring-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/How-to-Gracefully-Implement-Business-Performance-Monitoring-ru.md)


Com tantas ferramentas de monitoramento disponíveis hoje, como podemos tornar o processo de monitoramento de desempenho empresarial mais simples e elegante para os usuários?

### **1. Uma Visão de Monitoramento com Foco no Negócio**

Considerando a variação entre os indicadores de monitoramento e os objetivos por trás deles, os sistemas de alerta dos produtos de monitoramento de desempenho de aplicações variam bastante. Eles geralmente se dividem em duas abordagens: uma é o alerta "do detalhe para o geral", que começa com pontos de alerta em informações básicas, como cabeçalhos de pacotes, avançando para análises de uso de aplicativos e serviços, até identificar problemas específicos nos negócios, como erros de DNS ou lentidão nas respostas. A outra abordagem é o alerta "do geral para o detalhe", que começa no nível dos processos de negócios, monitorando nós específicos do aplicativo e da rede, e estabelecendo critérios de alerta para dados agregados, partindo de problemas comerciais amplos para chegar aos dados mais granulares. A primeira abordagem pode ser lenta e imprecisa devido à grande quantidade de falsos positivos nos dados detalhados, enquanto a segunda permite alertas rápidos em caso de falhas, sendo crucial em uma arquitetura operacional focada no negócio.
![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*Figura 1: Diagrama Hierárquico de Conhecimento*

A Netis BPC utiliza uma abordagem de monitoramento "do geral para o detalhe", proporcionando uma visão completa que vai do macro ao micro, centrada nos processos empresariais, removendo obstáculos entre a gestão operacional e estratégica, integrando monitoramento e perspectiva de negócios, e assegurando análises precisas e compreensíveis dos alertas.

### **2. Uma Abordagem Centrada no Usuário**

A ideia de usar teclas de piano para representar o tempo e um quadrante para destacar os principais indicadores de negócios é uma inovação da Netis BPC.
![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figura 2: Aplicação de teclas de piano e quadrantes na Netis BPC para alertas e diagnósticos de falhas*

**Por que uma tecla de piano simboliza um minuto?**

A Netis escolheu as teclas de piano para representar o tempo com o objetivo de tornar a experiência de monitoramento não apenas informativa, mas também intuitiva e até relaxante. Com o BPC, o tempo é visualizado como uma série de segmentos de um minuto, cada um codificado por cores para indicar diferentes estados operacionais. Interagir com esse sistema é semelhante a tocar piano, onde cada tecla, ao ser 'tocada' pelo cursor do mouse, revela detalhes específicos do tempo. Esse design meticuloso é pensado para assegurar uma leitura precisa das informações.

A decisão de configurar alertas com precisão de um minuto equilibra a necessidade de respostas rápidas com a gestão eficiente dos recursos. A experiência com clientes do setor financeiro mostrou à Netis que alertas muito frequentes podem sobrecarregar o sistema com redundâncias, enquanto uma frequência muito baixa pode comprometer a agilidade da resposta. Por isso, a granularidade de um minuto foi escolhida, representada simbolicamente por uma tecla de piano.

No entanto, reconhece-se que essa configuração pode não ser suficiente para todas as indústrias, como no caso das corretoras de valores, onde a demanda por monitoramento em tempo real é ainda mais crítica. Em situações como essas, a Netis BPC implementou um sistema de alertas baseado em segundos, ativado por padrões específicos de eventos, para garantir a detecção e ação imediatas diante de irregularidades.

**Desvendando os Indicadores de Ouro**

A equipe da Netis descobriu uma correlação direta entre o volume de transações e a carga nos serviços das aplicações, a taxa de resposta e a saúde do sistema, a taxa de sucesso e o bem-estar do negócio, enquanto o tempo de resposta das transações mostrou-se inversamente proporcional à qualidade da experiência do cliente. Após uma análise meticulosa, que incluiu a comparação dos Four Golden Signals, RED e USE, os indicadores de volume de transações, taxa de resposta, tempo de resposta e taxa de sucesso emergiram como os pilares para a Netis BPC.

A chave para um design que coloca o usuário em primeiro lugar é como esses pilares são apresentados de forma que sejam imediatamente compreensíveis, elevando assim a experiência do usuário. Após uma série de análises, experimentações e testes, nasceu o inovador quadrante da Netis, uma primazia no setor.

Essa ideia inovadora surgiu de uma visita ao Museu de Arte Moderna de Nova York feita por Wizard, cofundador e CPO da Netis. Lá, um mapa que delineava informações geográficas e populacionais dos EUA, disposto em uma grade simples, inspirou a criação do quadrante. Este formato não só facilitava a compreensão das informações, mas também se alinhava perfeitamente com a estrutura de componentes de aplicativos e redes. O insight foi que a eficácia na transmissão de informações cruciais reside na precisão, não na quantidade. Essa perspectiva foi reforçada pela observação de placas de sinalização e orientação comuns no cotidiano, culminando na concepção do emblemático quadrante.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*Figura 3: O Quadrante Icônico do Museu de Arte Moderna de Nova York:*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figura 4: O Quadrante Icônico da Netis BPC:*

A essência dos produtos BPC reside na captura precisa das necessidades dos usuários e na sua materialização através de um design inovador. Com um olhar atento às necessidades de alertas dos clientes, a Netis projeta seus produtos pensando na experiência do usuário, utilizando elementos como as teclas de piano e o quadrante, sempre com o foco nas pessoas e nos serviços. Esta abordagem não só soluciona as dificuldades dos usuários como também facilita a interação com o produto, harmonizando o valor prático com o apreço do usuário.

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
