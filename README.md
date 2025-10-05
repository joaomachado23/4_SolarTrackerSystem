# 4_SolarTrackerSystem

Um dos projetos de que mais me orgulho em ter concretizado! O objetivo deste trabalho era a conceção de um protótipo funcional a apresentar no final do semestre, à escolha de cada grupo, tendo obrigatoriamente de integrar conteúdos lecionados em 4 das 5 UC do mesmo semestre: Controlo Automático, Eletrónica de Potência, Instrumentação e Sensores, Máquinas Elétricas e Processamento de Sinal. Não era permitido utilizar componentes "digitais", como microcontroladores — era apenas o mundo analógico!

O nosso grupo decidiu desenvolver um Solar Tracker System (STS) que, basicamente, é um sistema constituído por um conjunto de painéis fotovoltaicos montados num braço com 2 eixos de liberdade, permitindo que estes acompanhassem a luz solar ao longo do dia e se mantivessem sempre a 90º (perpendiculares) à mesma, maximizando a incidência da luz e, consequentemente, a produção de energia.

Este projeto passou por várias etapas, sendo as tarefas distribuídas de forma equilibrada entre os membros do grupo, mas sempre em colaboração. Primeiramente, foi definida toda a sensorização necessária, bem como o respetivo acondicionamento de sinal. Os sensores utilizados foram LDRs (Light Dependent Resistors) que, como o nome indica, variavam a sua resistência consoante a luz recebida. Essa variação era medida, condicionada e enviada para o sistema de controlo, baseado em lógica ON-OFF com histerese. As saídas do controlador eram sinais de "Enable" e "Direção". Estes eram enviados para o sistema de atuação dos motores responsáveis pelo movimento dos painéis. Com o sinal de "Enable" e os interruptores de fim de curso acoplados ao protótipo, era criada uma lógica que permitia ao atuador decidir se deveria ou não acionar o motor. Adicionalmente, foi gerado um clock com um NE555 que, em conjunto com os sinais "Enable" e "Direção", comandava um integrado responsável por alimentar os enrolamentos do motor de acordo com o datasheet. Os motores incluíam ainda proteção contra sobrecorrente, para evitar danos.

Dado o uso de painéis fotovoltaicos, o grupo considerou interessante desenvolver também um conversor para aproveitar parte da energia gerada e, assim, aprofundar o conhecimento. Foi então projetado um conversor CC-CC boost, com controlo de tensão em malha fechada por PWM. O duty-cycle era ajustado de forma a obter a tensão de referência na saída, independentemente da entrada.

Toda a estrutura de suporte dos painéis foi desenvolvida pelo grupo. A base principal em ferro, que sustenta todo o sistema, foi soldada e pintada. Os componentes que requeriam movimento foram impressos em PLA (3D), excetuando a polia, a correia, os rolamentos, o veio do suporte dos painéis, bem como as porcas e parafusos.

Foi também desenvolvida a PCB, feita a montagem na íntegra e realizados os testes, debug e validação. O conversor foi montado e soldado em protoboard, com um LCD na saída que fornecia informação de tensão e corrente.

Neste repositório, é possível encontrar quatro ficheiros:

 1. Um PDF que contém toda a informação do projeto: design, simulação, conceção, testes e resultados.

 2. Um vídeo que mostra o resultado geral do projeto.

 3. Um vídeo que mostra o funcionamento do boost: variando a entrada da fonte, o duty-cycle era ajustado e a tensão média de saída estabilizava nos 24 V, como esperado.

 4. Um vídeo que mostra o STS a orientar-se para onde havia mais luz e o boost a converter a energia.

Este trabalho foi excelente para consolidar conhecimentos em diversas áreas da eletrónica, nomeadamente a analógica. Muito desafiante, mas, no fim, extremamente gratificante. Um grande obrigado aos colegas que me acompanharam nesta jornada: Diego Brandão, Francisco Costa, Henrique Magalhães, Rui Pedroso e Tiago Pereira.
