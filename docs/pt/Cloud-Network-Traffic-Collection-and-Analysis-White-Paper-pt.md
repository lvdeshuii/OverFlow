# White Paper sobre Coleta e Análise de Tráfego em Redes Nuvem (2022)

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ru.md)

A pesquisa realizada pela IDC revela que, nos próximos dois anos, a maioria das empresas planeja adotar plataformas nativas da nuvem através de estratégias de nuvem híbrida e multicloud. Com a diversificação dos usos da nuvem pelas empresas, o volume de tráfego dentro da nuvem, conhecido como tráfego leste-oeste, superou as expectativas. O desafio comum entre as empresas é como coletar e gerenciar esse tráfego de forma precisa. Nesse contexto, a Gartner sugere que os gestores de TI das empresas repensem as estratégias de coleta e análise de tráfego, visando alcançar um nível de visibilidade que atenda às necessidades dos ambientes de nuvem híbrida, facilitando o monitoramento e a gestão de desempenho futuro.

A Netis considera que a análise da observabilidade do tráfego de redes na nuvem representa uma solução eficaz para superar os desafios de monitoramento e gestão de desempenho em ambientes de nuvem nativa e híbrida. Por meio do uso de tecnologias

 de coleta e processamento de tráfego de alta performance, abrangentes e que não interferem nas aplicações, é possível criar uma visualização detalhada do tráfego em diferentes ambientes e arquiteturas, alcançando uma observabilidade completa das redes na nuvem. Para auxiliar as empresas nesse processo, a Netis publicou o "White Paper sobre Coleta e Análise de Tráfego em Redes Nuvem (2022)". Este documento é dividido em seis seções, abordando os desafios da era da nuvem, o valor da observabilidade do tráfego, arquiteturas e tecnologias para coleta e análise, soluções de implementação, exemplos de casos de uso e práticas recomendadas do setor, oferecendo soluções ótimas para a transição para a nuvem para empresas de diversos ramos.

Os destaques do documento incluem:

**1. Principais Capacidades**

- Versatilidade de Ambientes:
  - Amplo Suporte: Oferece suporte aos principais sistemas operacionais, chips e às tecnologias de virtualização e containerização mais utilizadas.

  - Microserviços: Compatível com diversas formas de implementação em arquiteturas de microserviços e vários ambientes de execução de containers.

- Ampla Gama de Funcionalidades:

  - Processamento de Pacotes: Habilidade para coletar, filtrar, distribuir, ajustar e eliminar duplicidades em pacotes de dados, entre outras funções essenciais.

  - Flow e Telemetry: Para a visualização eficiente do tráfego de rede na nuvem, é essencial o pré-processamento de pacotes de dados coletados, a geração de registros de Flow e o suporte a Telemetry.

  - Marcação de Dados: Permite a inclusão de informações específicas de cenários de negócios, redes e segurança nos pacotes de dados coletados.

  - Transmissão TCP: Utiliza o protocolo TCP para a transmissão de dados, assegurando sua confiabilidade.

- Não Invasivo: Implementação que não requer alterações nos processos de negócios existentes, garantindo total integridade.

- Autogestão: Capacidade de integrar com painéis de controle, monitorar o estado de execução de coletores, realizar autodiagnósticos, implementar mecanismos de proteção e recuperação automática, além de oferecer recursos de visualização.

- Flexibilidade de Escala: Projetado para suportar ajustes de escala dinâmicos, adaptando-se facilmente a mudanças nas demandas.

**2. As Tecnologias Essenciais**

- Coleta de Dados:
  - Cenários Aplicáveis: Engloba tanto a nuvem pública quanto a privada, abrangendo as tecnologias de VM (Máquinas Virtuais) e Containers, destacando-se pela flexibilidade de aplicação em diversos contextos.

  - Habilidades de Suporte: A coleta de dados deve ser adaptável, capaz de ajustar-se a diferentes cenários com ferramentas específicas para cada um. Além disso, a gestão unificada se faz necessária após a coleta em ambientes híbridos, evidenciando a importância de uma plataforma centralizada para o controle.

- Processamento em Camadas/vTAP: Segundo a Netis, o método de "ascensão e descida" na nuvem permite um tratamento em camadas dos dados, desde a coleta até o gerenciamento, assegurando uma observabilidade completa e detalhada, mesmo em situações de grande volume de dados e amplo espectro de gestão.

- Tecnologias de Coleta Fundamentais: Dada a complexidade dos ambientes na base da nu

vem, selecionar a tecnologia de coleta mais eficaz para cada caso é crucial para maximizar a performance e a eficiência.

- Compatibilidade com Ambientes Autônomos: A análise de tráfego e observabilidade em redes na nuvem deve ser capaz de integrar-se a servidores autônomos, como os baseados em arquitetura ARM e sistemas operacionais customizados, ampliando suas possibilidades de aplicação.

- Suporte a Flow: A capacidade de realizar estatísticas de fluxo detalhadas, aplicáveis a diversos cenários como rede, aplicativos e segurança, permite uma análise eficaz dos dados, facilitando a tomada de decisões entre o custo e o benefício da operação na nuvem.

- Telemetria: A integração com Open Telemetry enriquece as funcionalidades de observabilidade, reduzindo significativamente o consumo de recursos, o que representa um avanço significativo na gestão eficiente de redes na nuvem.

**3. Estratégias de Implementação**

Este segmento abrange 5 estratégias principais: a implementação geral do coletor, coleta de tráfego em hosts, em máquinas virtuais, em ambientes de containers, e o uso de vTAP para redirecionamento de tráfego, todas detalhadas no documento.

**4. Casos de Uso**

- Segurança: Apenas com um sistema robusto de coleta de tráfego de rede é possível capturar com precisão o tráfego nas máquinas de negócios na nuvem.

  Consciência Situacional: Com cargas de trabalho movendo-se para a nuvem, é vital entender profundamente a segurança interna, o que depende da análise precisa do tráfego na nuvem através de sondas de segurança.

  Proteção Nível 2.0: Capturar de forma precisa e dinâmica o tráfego nas máquinas de negócios na nuvem é crucial para cumprir com os padrões de segurança na nuvem.

- BPM/APM: A Netis vê o BPM como uma ferramenta rápida para identificar problemas de experiência do usuário através do tráfego da rede, enquanto o APM oferece análise de código de aplicação para diagnóstico detalhado, apresentando uma abordagem inovadora para observabilidade na nuvem.

- NPMD: No contexto da nuvem, o monitoramento de rede exige informações adicionais como AZ, VPC, e serviços, bem como capacidades avançadas de análise de topologia e rastreamento de sessões em múltiplas camadas.

  Análise de Topologia na Nuvem: Manter a visibilidade da topologia da rede na nuvem requer monitoramento avançado, apoiado por tecnologia de coleta de tráfego capaz de adaptar-se a mudanças dinâmicas.

  Rastreamento de Sessões em Múltiplas Camadas: Análise de rede na nuvem demanda rastreamento de sessões através de múltiplas camadas, possibilitado pela tecnologia de coleta de tráfego com capacidades de marcação.

- Banco de Dados: A arquitetura distribuída coloca novos desafios para o monitoramento de bancos de dados, tornando a coleta de tráfego na nuvem uma solução preferencial para garantir operação e segurança eficientes.

[**Clique para Baixar**](https://open.netis.com/datacenter/white-papers/天旦云网流量采集分析白皮书（2022）)

***

Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
