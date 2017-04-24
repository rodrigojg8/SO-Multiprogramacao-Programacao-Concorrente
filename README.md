# SO-Multiprogramacao-Programacao-Concorrente

Tipos de Sistemas Operacionais

Sistemas Batch

Os sistemas batch ou sistemas em lote foram os primeiros sistemas multiprogramáveis a serem implementados (primeira fase da computação), caracterizando-se por programas armazenados em disco ou fita, que uma vez iniciados, exigem pouca ou nenhuma interação do usuário, processando de forma sequencial e contínua até o fim do serviço (job), quando então é devolvido o resultado final do processamento, o tempo de execução da tarefa é conhecido como turnaround.

Sistemas multiprogramados

Nos sistemas monoprogramados o que temos é a existência de um único processo sendo executado de cada vez na memória, com a multiprogramação existem vários processos na memória aptos à executar e um em execução, sem dúvida, o conceito de multiprogramação é um dos mais importantes nos sistemas operacionais modernos, se existirem vários programas carregados na memória ao mesmo tempo, a CPU pode ser compartilhada entre eles, aumentando a eficiência da máquina e produzindo mais resultados em menos tempo.

A ideia por detrás da multiprogramação é bastante simples., quando um programa libera a CPU, seja para realizar alguma operação de E/S ou por outro motivo, ela fica parada. Enquanto espera que o programa volte para executar, a CPU não realiza nenhum trabalho útil.

Para acabar com a ociosidade deste tempo vários programas são mantidos ao mesmo tempo na memória e o sistema operacional se encarrega de escolher um deles para executar, assim, sempre que um programa é interrompido, um outro é escolhido para ser executado em seu lugar, com isso, a CPU estará durante grande parte do tempo ocupada processando instruções de programas.

Os benefícios da multiprogramação são vários: aumento da utilização da CPU e da taxa de saída do sistema computacional, isto é, da quantidade de trabalho realizada dentro de um intervalo de tempo (throughput).

Sistemas de Tempo Compartilhado (Time Sharing)

São sistemas que compartilham o tempo de uso da CPU entre diversos programas, também conhecido como time-sharing, consegue executar diversas tarefas simultaneamente, pois existe a divisão do tempo do processador em pequenos intervalos, denominados fatia de tempo, caso a tarefa não termine durante a fatia a ela determinada, há uma interrupção e ela volta para a fila de escalonamento, aguardando novamente sua vez.

Diferente do sistema batch, esse tipo de sistema operacional permite a interação do usuário. Dessa maneira, os terminais possuem teclado, vídeo e mouse.

Sistemas de Tempo Real

São sistemas no qual o tempo tem uma função essencial, em geral, um ou mais dispositivos físicos externos geram estímulos, e o computador deve reagir apropriadamente a eles dentro de um dado intervalo de tempo.

Sistemas multiprocessados

Sistemas multiprocessados são sistemas construídos sobre máquinas computacionais que possuem mais de um processador para propósitos gerais. Entre suas vantagens estão:

•	Maior produção (throughput) •	Reconfiguração •	Balanceamento •	Simetria

Estruturas de Sistemas Operacionais

Sistemas monolíticos

Também conhecida como estrutura simples, esta é a estrutura dos primeiros SO’s, eram constituídas basicamente, por um programa dividido em sub-rotinas, na estrutura monolítica é permitido a qualquer uma dessas sub-rotinas em qualquer parte do programa chamar outra(s) sub-rotina(s).

A construção do programa final é dada com base nos módulos compilados separadamente, unidos através de um linker, uma boa definição de parâmetros de ligação entre as diferentes rotinas existentes aumenta e muito o desempenho, porém o sistema pode parar devido a algum erro ocasionado por uma dessas rotinas, a exemplo temos o próprio UNIX, o MS DOS, o FreeBSD, entre outros.

Sistemas em camadas

Devido ao crescimento das necessidades dos utilizadores e o aperfeiçoamento dos sistemas, foi-se necessário a modularização da organização do sw e do SO, na abordagem em camadas, o SO é particionado em níveis, onde o nível mais “baixo” é o hw, e o nível mais “alto” é a interface com o usuário.

A principal vantagem dessa estrutura é justamente a modularização, facilitando sua alteração e depuração de cada camada, além de criar uma hierarquia de níveis de acesso que permite proteger as camadas mais internas, as camadas são selecionadas de tal modo q/ue cada uma delas opere diretamente com a camada seguinte de nível mais baixo, foi originado na Holanda por **Edsger Dijkstra**, que utilizou o algoritmo de busca de menor caminho, também de sua própria autoria, para percorrer dentre as várias camadas, as que atenderão as solicitações de **“cima”**, de maneira mais eficiente.

Uma desvantagem desta estrutura é o tempo de resposta ao usuário, pois numa requisição sua, uma camada irá se comunicar com a outra diretamente seguinte, e assim por diante, possibilitando a modificação de parâmetros a cada camada, necessidade de dados e ainda o acréscimo de overhead à chamada do sistema, levando, contudo, ao consumo maior de tempo do que nos SO’s não estruturados em camadas.

Por sua vez, tal estrutura tem uma vantagem maior do ponto de vista tanto do projeto quanto da implementação, pois a impossibilidade de comunicação direta das aplicações de cima com as de baixo, leva a um controle maior do SO sobre o hw.

A exemplo temos o Windows NT, o THE e o MULTICS.

Sistemas Cliente-Servidor

Sistemas Cliente-Servidor são modelos de computação que distinguem dois tipos básicos de equipamentos computacionais: servidores e clientes, sendo interligados entre si geralmente utilizando-se uma rede de computadores. Neste modelo, geralmente os servidores agregam as funções mais importantes do sistema, deixando aos clientes apenas o processamento de aplicações mais básicas.

As principais características deste tipo de sistema são: •	Elevar a camada onde são implementadas as funções normalmente efetuadas pelo sistema operacional •	Reduzir as funções do sistema operacional •	Tornar menor e de mais fácil a manutenção cada parte do sistema operacional

Monoprogramação ou monotarefa

Em computação, chama-se monotarefa um sistema operacional que permite a realização de apenas uma tarefa (job) de cada vez, o processador, memória e periféricos ficam dedicados a um único usuário, e cada tarefa para ser executada, deve aguardar o encerramento da tarefa atual, nos sistemas monoprogramados, enquanto uma aplicação aguarda um evento, o processador pode permanecer ocioso, sem realizar qualquer tipo de processamento, a memória pode acabar sendo sub-utilizada quando o programa não a utiliza totalmente e os periféricos são dedicados a um único usuário, desta forma, os sistemas monoprogramáveis acabam sendo por sua natureza de fácil implementação e com pouca preocupação com proteção.

Multiprogramação

Um conceito fundamental em sistemas operacionais é o conceito de processo, um processo é basicamente um programa em execução, ele consiste em um programa executável, os seus dados e pilha, o seu stack pointer e registradores, enfim todas as informações necessárias para executar o programa.

Periodicamente o sistema operacional decide se a execução de um processo deve ser interrompida e a execução de um outro processo deve ser iniciada--pela razão do primeiro já ter tido mais do que a sua `fatia' de tempo de CPU, em um sistema de multiprogramação a CPU fica se alternando entre a execução de vários processos, cada um por dezenas ou centenas de milissegundos.

Um processo pode estar em um dos seguintes estados:

Running: usando a CPU naquele instante;
Ready: pronto para ser executado, temporariamente parado para que outro processo possa ser executado; e
Blocked: impossibilitado de ser executado até que algum evento externo ocorra.
Em um sistema de multiprogramação temos frequentemente a situação onde vários processos estão prontos para serem executados, quando mais de um processo está ready, o sistema operacional deve decider qual processo deve ser executado primeiro, a parte do sistema operacional que toma esta decisão é chamada de scheduler.

O algoritmo que é usado é chamado de scheduler algorithm, a cada interrupção do relógio, o sistema operacional toma o controle e decide se o processo que está sendo executado deve continuar a ser executado ou deve ser suspenso para que outro processo passe a ser executado, a estratégia que permite que um processo que está sendo executado seja suspenso temporariamente é chamada de preemptive schedule.

Existem scheduling algoritms que assumem que todos os processos que são iguais, entretanto, existem muitas pessoas que possuem e administram centros de computação que discordam disto. Por exemplo, em um centro de computação de uma universidade pode ser dada a mais alta prioridade aos processos de diretores, depois aos de professores, depois aos de secretarias, depois aos de porteiros, ...e finalmente aos de alunos. Isto é chamado de um priority schedule (alguns podem chamar isto de injustiça).

Para evitar que processos que têm alta prioridade fiquem sendo executados indefinidamente o scheduler pode baixar a prioridade do processo que está sendo executado a cada interrupção do relógio.

Alguns priority schedulers fazem uso de classes de prioridade, os processos na classe de prioridade mais baixa podem ser executados sem serem suspensos por no máximo uma QUANTA (uma quantidade de tempo de CPU). Processos na próxima classe de prioridade pode ser executado por no máximo duas QUANTAS, e assim por diante. Sempre que um processo usa toda as QUANTAS alocadas para ele este processo é rebaixado de classe.

Quando um processo deseja imprimir um arquivo, ele coloca o nome do arquivo em um diretório especial chamado de spooler directory. Um outro processo, o printer daemon, periodicamente verifica se existe algum arquivo a ser impresso, se existir ele imprime o arquivo e remove o nome do arquivo do diretório spooler.

PROGRAMAÇÃO CONCORRENTE

A programação concorrente foi usada inicialmente na construção de sistemas operacionais, ela é usada para desenvolver aplicações em todas as áreas da computação, este tipo de programação tornou-se ainda mais importante nos sistemas distribuídos, e com máquinas de arquitetura paralela.

A grande maioria dos programas escritos são programas seqüenciais. Nesse caso, existe somente um fluxo de controle (fluxo de execução, linha de execução, thread) no programa. Isso permite, por exemplo, que o programador realize uma "execução imaginária" de seu programa apontando com o dedo, a cada instante, o comando que está sendo executada no momento.

Um programa concorrente pode ser visto como se tivesse vários fluxos de execução, para o programador realizar agora uma "execução imaginária", ele vai necessitar de vários dedos, um para cada fluxo de controle, o termo "programação concorrente" vem do inglês concurrent programming, onde concurrent significa "acontecendo ao mesmo tempo". Uma tradução mais adequada seria programação concomitante.

Entretanto, o termo programação concorrente já está solidamente estabelecido no Brasil. Algumas vezes é usado o termo programação paralela com o mesmo sentido, é comum em sistemas multiusuário que um mesmo programa seja executado simultaneamente por vários usuários.

Por exemplo, um editor de texto. Entretanto, ter 10 execuções simultâneas do editor de texto não faz dele um programa concorrente. O que se tem são 10 processos independentes executando o mesmo programa seqüencial (compartilhando o mesmo código). Cada processo tem a sua área de dados e ignora a existência das outras execuções do programa. Esses processos não interagem entre si (não trocam informações). Um programa é considerado concorrente quando ele (o próprio programa, durante a sua execução) origina diferentes processos. Esses processos, em geral, irão interagir entre si.

Referêrencias https://www.ime.usp.br/~gold/cursos/2002/mac2301/ep2/ep2/node3.html https://pt.wikibooks.org/wiki/Sistemas_operacionais/Estruturas_dos_sistemas_operacionais www.inf.pucrs.br/~ramos/sop_progconctext.doc
