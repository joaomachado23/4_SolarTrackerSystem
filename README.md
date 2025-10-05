# 4_SolarTrackerSystem

Um dos projetos que mais orgulho tenho de ter concretizado! O objetivo deste trabalho era a conceção de um projeto final de semestre à escolha de cada grupo, tendo obrigatoriamente de apresentar conteúdos lecionados em 4 das 5 UC lecionadas no mesmo semestre, sendo elas Controlo Automático, Eletrónica de Potência, Instrumentação e Sensores, Máquinas Elétricas e Processamento de Sinal. Não era permitido utilizar componentes "digitais", tais como microcontroladores: era só mundo analógico!

O nosso grupo decidiu fazer um Solar Tracker System (STS) que, basicamente, é um sistema constituído por um grupo de painéis fotovoltaicos montados num braço com 2 eixos de liberdade, permitindo que os mesmos acompanhassem a luz solar ao longo do dia e estivessem sempre a 90º (perpendiculares) com a mesma, maximizando a incidência da luz e, consequentemente, a produção de energia ao longo do dia.

Este projeto teve bastantes etapas, sendo as tarefas distribuídas uniformemente pelos membros do grupo, mas sem que ninguém trabalhasse sozinho. Primeiramente, foi escolhida toda a sensorização necessária, bem como o acondicionamento de sinal da mesma. Os sensores eram LDR (Light Dependent Resistors) que, como o nome indica, variavam a sua resistência de acordo com a luz recebida. Essa variação era medida, condicionada e enviada para o sistema de controlo de todo o processo, baseado em controlo ON-OFF com histerese. A saída do controlador são sinais de "Enable" e "Direção". Estas são enviadas para o sistema de atuação dos motores responsáveis pelo movimento dos painéis. Juntamente com interruptores de fim de curso acoplados ao protótipo e o sinal de "Enable", é gerada uma lógica que permite ao atuador saber se deve ou não atuar o motor. Adicionalmente, é gerado um clock com um NE555, que junto com os sinais "Enable" e "Direção", permite atuar um integrado que, com a lógica necessária para alimentar os enrolamentos do motor de acordo com o datasheet, atua os motores.
Para além disso, os motores também contemplam proteção contra sobrecorrentes para evitar danos.

Dado o uso de painéis fotovoltaicos, o grupo considerou interessante realizar um conversor para aproveitar alguma da energia gerada pelo grupo de painéis e, assim, desenvolver ainda mais o seu conhecimento. Foi então desenhado um conversor CC-CC boost, com controlo de tensão em malha fechada por PWM. O duty-cycle era variado para obter a tensão de referência na saída, independentemente da entrada.

Toda a estrutura da base que segura os painéis foi desenvolvida pelo grupo. A base principal em ferro que suporta tudo foi soldada e pintada. Todos os componentes que requerem movimento foram impressos em PLA (3D), excetuando polia, correia, rolamentos, veio do suporte dos painéis e porcas e parafusos.

Foi feita a PCB e a montagem na íntegra, bem como os testes, debug e validação. O conversor ficou montado e soldado em protoboard, com um LCD na saída que dava informação de tensão e corrente.

Neste repositório, é possível encontrar quatro ficheiros:

 1. Um PDF que contém toda a informação do projeto: design, simulação, conceção, testes e resultados.

 2. Um vídeo que mostra o resultado geral do projeto.
 
 3. Um vídeo que mostra o funcionamento do boost: variando a entrada na fonte, o duty-cycle era ajustado e a tensão média de saída era de 24V, como esperado.
 
 4. Um vídeo que mostra o STS a orientar-se para onde havia mais luz e o boost a converter a energia.

Este trabalho foi excelente para aprender e assimilar conhecimentos em diversas áreas da eletrónica, nomeadamente a analógica! Muito desafiante, mas, no fim, muito gratificante. Um grande obrigado aos companheiros que me acompanharam na jornada deste projeto: Diego Brandão, Francisco Costa, Henrique Magalhães, Rui Pedroso e Tiago Pereira. 
