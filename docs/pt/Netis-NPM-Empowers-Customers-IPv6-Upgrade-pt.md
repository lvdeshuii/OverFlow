# Netis NPM impulsiona a transição dos clientes para IPv6

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Netis-NPM-Empowers-Customers-IPv6-Upgrade-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Netis-NPM-Empowers-Customers-IPv6-Upgrade-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Netis-NPM-Empowers-Customers-IPv6-Upgrade-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Netis-NPM-Empowers-Customers-IPv6-Upgrade-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Netis-NPM-Empowers-Customers-IPv6-Upgrade-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Netis-NPM-Empowers-Customers-IPv6-Upgrade-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ru.md)

**Contexto**

Em julho de 2021, autoridades chinesas, incluindo o Escritório Central de Ciberespaço, lançaram um aviso para acelerar a adoção do IPv6, a mais recente versão do Protocolo de Internet. Este aviso enfatiza a importância de atualizar as instituições financeiras para suportar IPv6, melhorando assim os sistemas de internet voltados ao público e reforçando a monitoração e operação de redes IPv6.

**Estudo de caso**

Um banco tomou a iniciativa de seguir esta orientação, empenhando-se na transição para IPv6. Até o início de 2022, conseguiu implementar uma rede que suporta tanto IPv4 quanto IPv6, garantindo que aplicações como seu portal online, serviços de banco pela internet, móvel e até mesmo pelo WeChat estejam acessíveis via IPv6. Para garantir uma operação eficiente dessa rede híbrida, o banco adotou o Netis NPM, um sistema avançado de análise de tráfego de rede, permitindo o monitoramento contínuo do tráfego para aplicações web e segmentos de rede críticos.

**A importância do caso**

- **Visualização do Tráfego de Rede**: Facilita a compreensão da estrutura e fluxo da rede de forma rápida, criando uma base sólida para descobrir potenciais valores comerciais escondidos na rede.
- **Mapa de Serviço com Perspectiva de Negócios**: Supera as limitações das operações de rede e aplicações separadas, oferecendo uma visão integrada.
- **Visão Comparativa entre IPv4 e IPv6**: Monitora o volume de acesso e performance das aplicações sob ambos os protocolos, permitindo ajustes ágeis nos recursos de rede para atender demandas de aplicativos de forma eficaz.
- **Detecção e Alerta Rápido de Anomalias de Rede**: Minimiza o tempo de resposta a falhas, elevando a qualidade do serviço de rede.

**1. Netis NPM: Plataforma Unificada para Gestão de Tráfego**

Utilizando tecnologia de ponta para espelhamento de rede, o Netis NPM replica o tráfego de rede em tempo real para um dispositivo de divisão de tráfego (TAP). Este, por sua vez, organiza, marca e redistribui o tráfego para dispositivos de análise específicos. Após a análise, uma gestão coesa e apresentação dos dados são realizadas através de uma plataforma unificada, proporcionando uma visão clara e controlada do tráfego de rede.
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdmOY8s0Zx1QLXLJAwZPCTCVweXBzFohlQVec4ZWSD75iafRL0nuxPedQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 1: Estrutura Lógica do Netis NPM*

Ao analisar integralmente o tráfego das linhas dedicadas de saída para a internet e dos switches posicionados antes e depois dos dispositivos de segurança, criamos visualizações específicas para IPv4 e IPv6. Essa estratégia permite um monitoramento constante do estado da rede, oferecendo aos técnicos de rede a habilidade de acompanhar o status diário da rede de forma rápida e eficiente.
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdzV9UeJb7j2j2MdKqialiaWyAg8aaWdNAnxxkH5ibOpcL3mykCg1G68bPA/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 2: Visão do Link de Saída Especializado em IPv4 - Métricas de Desempenho da Aplicação*
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdLebyqoTAYIJEwomHz2EAtVUYrickXjJ57I8POcGUIXDL3wg7TzyibD6w/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 3: Visão do Link de Saída Especializado em IPv4 - Carga da Rede*
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdNd5IJZE9kThvyGBOKXnLbicb8h9yHh7gQZXriboIntLgvIXEjXSFLUrQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 4: Visão do Link de Saída Especializado em IPv6 - Carga da Rede*

**2. A inovação do SPV, observando a rede pela ótica da aplicação**

Na rotina de operação e manutenção, a gestão de redes e aplicações é frequentemente dividida entre diferentes equipes. Esta separação pode complicar a rápida identificação e resolução de problemas. O Netis NPM inova com sua tecnologia exclusiva de Mapa de Caminho de Serviço (SPV), criando um sistema de monitoramento completo que analisa a rede sob a perspectiva das necessidades comerciais e das aplicações. O SPV avalia o estado da rede de uma aplicação em quatro aspectos principais: volume de tráfego, desempenho da rede, eficiência da aplicação e disponibilidade, facilitando a identificação e correção ágil de quaisquer problemas que possam surgir.
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrd7ibZGpAdR6x5s4JPYOrSQqgibTXTVoK53cRxPSawqYnplztwXVAiaNIFQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 5: Mapa de Caminho de Serviço do Netis NPM, com foco na perspectiva comercial*

**3. Tudo em Uma Tela: Comparando Indicadores de Rede IPv4 e IPv6**

Num ponto de acesso crucial à internet, um banco inovou com o uso do grande ecrã do Netis NPM para criar uma visualização comparativa entre os indicadores de rede IPv4 e IPv6. Esta ferramenta permite uma gestão em tempo real do tráfego de saída, contribuindo significativamente para aprimorar a experiência dos utilizadores.
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrd0icN9vsmAf2Tp1gks2V2Z3nx266D6ia02XqbTP9Jvu1srs0ve7xFa2Dw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 6: Visão Geral no Grande Ecrã do Netis NPM*

Para os sistemas de serviços críticos ao público, o banco desenvolveu um sistema de relatórios personalizados - diários, semanais e mensais - que são enviados aos reguladores conforme a necessidade surge, garantindo assim transparência e conformidade.
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdIngXzdI72uJ9mrwpx0LHnmpWslsam5qu2s1R5ADQDcTos941Xz4vXg/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*Figura 7: Exemplo de Relatório Semanal para Serviços Críticos*

A gama de produtos da Netis está totalmente equipada para suportar a análise de serviços IPv6, assegurando que os negócios dos clientes se mantenham estáveis e eficientes sob este novo protocolo.
***
At Netis, we're at the forefront of analyzing business(APM) and network performance(NPM), ensuring that over thirty billion transactions run smoothly every day. Our commitment to system and data security is paramount, and we pride ourselves on our ability to conduct real-time analysis through network traffic mirroring. This means we can get the job done without the need for any agents or disruptions to your existing operations. Based in Shanghai, China, Netis is a global software company known for its high-performance products and cost-effective solutions. Interested in what we offer? Don't hesitate to get in touch. We're excited about the possibility of working together and welcoming new partners.  
Discover more at: www.netis.com/en/  
Or drop me a line directly: dennis.li@netis.com
